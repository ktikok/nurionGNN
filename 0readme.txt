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


conda create --prefix -n py39 python=3.9 -y
conda activate py39
conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cpuonly -c pytorch -y ; conda install pyg -c pyg -y
# pyg=2.0.4

https://github.com/conda/conda/issues/5551
package cache problem


[4498 rows x 7 columns]
Traceback (most recent call last):
  File "/home01/hpc22a06/0me/nurionGNN/hepgnn_4top_resampling/train_4top_QCD_cla_resam.py", line 93, in <module>
    dset.initialize()
  File "/home01/hpc22a06/0me/nurionGNN/hepgnn_4top_resampling/./python/dataset/HEPGNNDataset_pt_classify_fourfeature_v6.py", line 139, in initialize
    btag_list.append(f[j].x[:,4][0])
  File "/home01/hpc22a06/miniconda3/envs/py39/lib/python3.9/site-packages/torch_geometric/data/data.py", line 642, in x
    return self['x'] if 'x' in self._store else None
  File "/home01/hpc22a06/miniconda3/envs/py39/lib/python3.9/site-packages/torch_geometric/data/data.py", line 357, in __getattr__
    raise RuntimeError(
RuntimeError: The 'data' object was created by an older version of PyG. If this error occurred while loading an already existing dataset, remove the 'processed/' directory in the dataset's root folder and try again.

conda create --prefix /home01/hpc22a06/miniconda3/envs/pyg16
conda activate pyg16
conda install pytorch==1.7.0 torchvision==0.8.0 torchaudio==0.7.0 cpuonly -c pytorch
#pip install torch-geometric
#pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-1.7.0+cpu.html
# error
# Your compiler (g++ 4.8.5) may be ABI-incompatible with PyTorch!
#       Please use a compiler that is ABI-compatible with GCC 5.0 and above.
#pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
#pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
#pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
pip install torch-geometric

conda create --prefix /home01/hpc22a06/miniconda3/envs/py3.7
conda activate py3.7
# cannot install pytorch by pip. So, I used conda. and same problem with torch-~~

conda create --prefix /home01/hpc22a06/miniconda3/envs/py37 python=3.7
conda install pytorch==1.7.1 torchvision==0.8.2 torchaudio==0.7.2 cpuonly -c pytorch
conda install -c conda-forge pytorch_geometric=1.6
# pyg=1.6.1, can read tensor.pt but not 1.6.3 data file. It's different error.

conda create --name py37pip_pytorch python=3.7
conda activate py37pip_pytorch
pip install torch==1.7.1+cpu torchvision==0.8.2+cpu torchaudio==0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-1.7.1+cpu.html
# here is an error, gcc version4.8.5..
#pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
#pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
#pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-${TORCH}+${CUDA}.html
#pip install torch-geometric
conda install gcc_linux-64
conda install gxx_linux-64
conda install gfortran_linux-64

