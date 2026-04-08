**ACE-Step-1.5-ROCM**

Generate music with AI using dual AMD cards!
**Important note:**
- This setup will not work under some circumstances.
- We used dual AMD cards (AMD Radeon RX 7600XT 16gb and AMD Radeon RX 9060XT 16gb) with **AMD ROCm 7.2.0**. Any earlier ROCM version will very likely not work.

**Here is how to set up:**

1. Install ROCm and PyTorch: 
   - Linux: use this link to install the latest ROCm version: https://rocm.docs.amd.com/projects/install-on-linux/en/latest/install/quick-start.html
   - Install PyTorch: pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm7.2
   - Windows: pip install --no-cache-dir ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/rocm_sdk_core-7.2.0.dev0-py3-none-win_amd64.whl ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/rocm_sdk_devel-7.2.0.dev0-py3-none-win_amd64.whl ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/rocm_sdk_libraries_custom-7.2.0.dev0-py3-none-win_amd64.whl ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/rocm-7.2.0.dev0.tar.gz
   - Installing PyTorch for ROCm on Windows:
     pip install --no-cache-dir ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/torch-2.9.1+rocmsdk20260116-cp312-cp312-win_amd64.whl ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/torchaudio-2.9.1+rocmsdk20260116-cp312-cp312-win_amd64.whl ^
     https://repo.radeon.com/rocm/windows/rocm-rel-7.2/torchvision-0.24.1+rocmsdk20260116-cp312-cp312-win_amd64.whl

2. Install other dependencies for Linux/Windows:
   - Linux: pip3 install -r requirements-rocm-linux.txt
   - Windows: pip3 install -r requirements-rocm.txt

3. Install UV:
   - Linux: pip3 install uv
   - Windows: pip install uv

4. Run gradio UI:
   - uv run gradio.py
