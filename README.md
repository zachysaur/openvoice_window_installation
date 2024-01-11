# openvoice_window_installation

Conda create -n openvoice pytho=3.9

conda activate openvoice

conda install pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia

pip install torchaudio==0.10.0+cpu -f https://download.pytorch.org/whl/torch_stable.html

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco --version

choco install aria2

choco install aria2 --force

aria2c --version

aria2c --console-log-level=error -c -x 16 -s 16 -k 1M https://huggingface.co/camenduru/OpenVoice/resolve/main/checkpoints_1226.zip -d C:\Windows\System32\OpenVoice -o checkpoints_1226.zip

pip install webrtcvad

python openvoice_app.py --share
