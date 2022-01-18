FROM kunalg106/cuda100

RUN useradd -m -p c3dpwd -g sudo c3duser
RUN wget -P /home/c3duser 'https://sourceforge.net/projects/c3d/files/c3d/Nightly/c3d-nightly-Linux-gcc64.tar.gz'
RUN tar -xf /home/c3duser/c3d-nightly-Linux-gcc64.tar.gz
RUN cp -a /c3d-1.3.0-Linux-gcc64/bin/. /usr/local/bin


RUN conda create -n myenv python=3.6
RUN echo "source activate myenv" > ~/.bashrc
ENV PATH /opt/conda/envs/myenv/bin:$PATH



RUN pip install git+https://github.com/zhennongchen/dvpy.git#egg=dvpy
RUN pip install tensorflow-gpu==1.14.0
RUN pip install keras==2.2.4
RUN pip install tqdm sympy xlsxwriter
RUN pip install opencv-python
RUN apt-get update
RUN apt-get install ffmpeg libsm6 libxext6 -y
RUN pip uninstall h5py -y whatever
RUN pip install h5py==2.10.0
RUN conda install -c conda-forge scikit-image
RUN pip install sklearn

RUN wget http://mirrors.kernel.org/ubuntu/pool/main/b/boost1.58/libboost-program-options1.58.0_1.58.0+dfsg-5ubuntu3_amd64.deb
RUN sudo dpkg -i  libboost-program-options1.58.0_1.58.0+dfsg-5ubuntu3_amd64.deb

