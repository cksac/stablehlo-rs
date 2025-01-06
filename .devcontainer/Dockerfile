FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

ARG LLVM_VERSION=19

RUN sudo apt update && sudo apt install -y lsb-release wget software-properties-common gnupg

# llvm
RUN wget https://apt.llvm.org/llvm.sh && chmod +x llvm.sh
RUN sudo ./llvm.sh ${LLVM_VERSION} all

# mlir
RUN sudo apt install -y libmlir-${LLVM_VERSION}-dev mlir-${LLVM_VERSION}-tools

# llvm-config symlink
RUN sudo ln -s /bin/llvm-config-${LLVM_VERSION} /bin/llvm-config
