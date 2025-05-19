# jetsoninstall

Jetson 보드 리눅스에서 설치확인 

$ nvcc --version 또는

$ find /usr -name '*cuda*' -> CUDA 버전확인

cuda 설치 후 환경변수 설정해야 함

윈도우즈의 경우 cuda 설치과정에서 path 설정을 해주지만 리눅스의 경우는 수동으로 해줘야함

아래 두문장을 ~/.bashrc파일 마지막부분에 추가한다. xx.x 대신에 위에서 확인한 버전을 적는다.

$ cd ~

$ vi .bashrc

.......

export PATH=/usr/local/cuda-xx.x/bin${PATH:+:${PATH}}

export LD_LIBRARY_PATH=/usr/local/cuda-xx.x/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

$ source .bashrc -> 변경내용 바로 적용

Jetson보드의 리눅스에서 cudnn 버전확인

$ find /usr -name '*cudnn_version*' -> cuDNN 버전확인

cudnn_version.h을 찾아서 define문에서 정의한 3개 기호상수(CUDNN_MAJOR, MINOR, PATCHLEVEL)가 버전 x.x.x을 의미함
