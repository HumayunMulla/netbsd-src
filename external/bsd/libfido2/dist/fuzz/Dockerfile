# Copyright (c) 2019 Yubico AB. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

FROM ubuntu:bionic
RUN apt-get update
RUN apt-get install -y clang-9 cmake git libssl-dev libudev-dev make pkg-config
RUN git clone --branch v0.5.0 https://github.com/PJK/libcbor
RUN git clone https://github.com/yubico/libfido2
RUN CC=clang-9 /libfido2/fuzz/build-coverage /libcbor /libfido2
