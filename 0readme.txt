conda activate gnn # cannot install pyg, python=3.10xxxxxxxxxxxxxxx

conda activate py37 # python=3.7, did installed pyg(pytorch=1.10) but cannot importxxxxxxxxxxxxxxxxx

conda create --name py310 python=3.10
    conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cpuonly -c pytorch -y; conda install pyg -c pyg -y
    # # cannot install pyg,xxxxxxxxxxxxxxxxxx

conda create --name py310torch110 python=3.10
    conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cpuonly -c pytorch -y ; conda install pyg -c pyg -y
    # cannot install pytorchxxxxxxxxxxxxxxxxxx


conda create --name pytorch111
    conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cpuonly -c pytorch -y ; conda install pyg -c pyg -y
#    python=3.10 installed first and then... error

conda create --name pytorch1101
    conda install pytorch==1.10.1 torchvision==0.11.2 torchaudio==0.10.1 cpuonly -c pytorch -y ; conda install pyg -c pyg -y
# [Errno 2] No such file or directory: '/scratch/hpc22a06/.conda/pkgs/scikit-learn-1.0.2-py39h51133e4_1/.cph_tmpv16zg6tv'


conda create --name pytorch1100 -y
conda activate pytorch1100
conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cpuonly -c pytorch -y ; conda install pyg -c pyg -y

conda create --name pyg -y
conda activate pyg
conda install pyg -c pyg -y
# it install bellow... let's try them! but cpu only torch!
# pyg                pyg/linux-64::pyg-2.0.4-py39_torch_1.10.0_cu113
# python             pkgs/main/linux-64::python-3.9.12-h12debd9_1
# [Errno 2] No such file or directory: '/scratch/hpc22a06/.conda/pkgs/scikit-learn-1.0.2-py39h51133e4_1/.cph_tmpuuoaxj3c'


conda create -n py39 python=3.9 -y
conda activate py39
conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cpuonly -c pytorch -y ; conda install pyg -c pyg -y

https://github.com/conda/conda/issues/5551
package cache problem