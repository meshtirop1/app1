FROM ubuntu:latest
LABEL authors="mtiro"

ENTRYPOINT ["top", "-b"]

# Use the official Python base image
FROM python:3.9

# Set environment variables
ENV ANDROID_HOME /opt/android-sdk
ENV PATH ${PATH}:${ANDROID_HOME}/tools:${ANDROID_HOME}/tools/bin:${ANDROID_HOME}/platform-tools

# Install required packages
RUN apt-get update && apt-get install -y \
    openjdk-11-jdk \
    unzip \
    wget \
    && rm -rf /var/lib/apt/lists/*

# Install Buildozer and dependencies
RUN pip install --upgrade pip
RUN pip install buildozer cython

# Download and install Android SDK
RUN wget https://dl.google.com/android/repository/commandlinetools-linux-6858069_latest.zip -O commandlinetools.zip
RUN mkdir -p ${ANDROID_HOME}/cmdline-tools
RUN unzip commandlinetools.zip -d ${ANDROID_HOME}/cmdline-tools
RUN rm commandlinetools.zip
RUN yes | ${ANDROID_HOME}/cmdline-tools/cmdline-tools/bin/sdkmanager --sdk_root=${ANDROID_HOME} "platform-tools" "platforms;android-30" "build-tools;30.0.3"

# Set the working directory
WORKDIR /build

# Copy the current directory contents into the container at /build
COPY . /build

# Run buildozer to build the APK
CMD ["buildozer", "-v", "android", "debug"]
