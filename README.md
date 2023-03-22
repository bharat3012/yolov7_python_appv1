# yolov7_python_appv1


1. Run Conatiner
docker run --net=host --ipc=host -it -v $pwd:/workspace/cdot --gpus all nvcr.io/nvidia/deepstream:6.2-triton

2. Install Python bindings

cd /opt/nvidia/deepstream/deepstream
bash user_deepstream_python_apps_install.sh --build-bindings -r master

3. Install pyds
pip3 install pyds

4. cd /workspace/cdot
git pull https://github.com/NVIDIA-AI-IOT/deepstream_python_apps.git

Copy this https://drive.google.com/drive/folders/1FK7alu_zxU65d8zKo9rS88g4Irp17KKq
and replace with deepstream-test1 app in deepstream_python_apps/apps

5. cd  nvdsinfer_custom_impl_Yolo

make

Note
A. dstest1_pgie_config.txt  --> from   config_infer_primary_yoloV7.txt  under  https://github.com/NVIDIA-AI-IOT/yolo_deepstream/tree/main/deepstream_yolo/

B. nvdsinfer_custom_impl_Yolo   --> from nvdsinfer_custom_impl_Yolo under https://github.com/NVIDIA-AI-IOT/yolo_deepstream/tree/main/deepstream_yolo/

C. Check labels.txt 

D. yolov7.onnx   --> from  yolov7.onnx under https://github.com/NVIDIA-AI-IOT/yolo_deepstream/tree/main/yolov7_qat
