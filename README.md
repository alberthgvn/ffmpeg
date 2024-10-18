1. FFMPEG source
  git clone https://git.ffmpeg.org/ffmpeg.git ffmpeg
2. Build the FFMPEG with QNX
  source <QNXinstall>/qnxsdp-env.sh
  ./configure --prefix=./build --target-os=qnx --arch=aarch64 --cc=<QNXinstall>/qnx710/host/linux/x86_64/usr/bin/aarch64-unknown-nto-qnx7.1.0-gcc --cxx=<QNXinstall>/qnx710/host/linux/x86_64/usr/bin/aarch64-unknown-nto-qnx7.1.0-g++ --enable-cross-compile --enable-static --enable-shared --disable-doc --disable-asm --disable-ffmpeg --disable-ffplay --disable-ffprobe --enable-avdevice --enable-swscale --disable-postproc --enable-avfilter --enable-pthreads --disable-w32threads --disable-os2threads --disable-d3d11va --disable-dxva2 --disable-vaapi --disable-vdpau --disable-videotoolbox --disable-audiotoolbox --disable-securetransport --disable-amf --disable-cuda-llvm --disable-cuvid --disable-nvenc --disable-nvdec --disable-avisynth --enable-bzlib --disable-iconv --enable-zlib --enable-lzma --disable-sdl2 --enable-gpl --enable-version3 --enable-nonfree --disable-stripping --disable-indevs --disable-libxcb --enable-network --extra-cflags=-fPIC --extra-libs=-lc

  make VERBOSE=1 -j8

  make install
