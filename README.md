# 머신러닝, 딥러닝을 공부하면서 실습한 코드 위주로 업로드<br/>

## 개발환경<br/>
Ubuntu 20.04<br/>
python 3.8.10<br/>
Tensorflow 2.3.0<br/>
cuda 10.1<br/>
cudnn <br/>

## 깃허브 관련 명령어 확인
1. 깃허브 Repository 다운<br/>
git clone (다운받고자하는 주소(https://github.com/ksch28/ ~ ))<br/>
2. 파일 업로드<br/>
git add * <br/>
git commit -m 'file_upload'<br/>
git push<br/>

3. 변경된 상태 확인
git status<br/>
추가적으로 천천히 명렁어들을 업데이트 하겠음.<br/>

## 딥러닝 관련<br/>
1. nvidia 확인<br/>
nvidia-smi<br/>
2. nvidia gpu 메모리 정리<br/>
sudo kill -9 (메모리 주소) <br/>
3. 실시간 gpu 메모리 확인<br/>
watch -n 1 nvidia-smi<br/>
4. Tensorflow GPU 사용 제한
```python
import tensorflow as tf
config = tf.compat.v1.ConfigProto(
gpu_options=tf.compat.v1.GPUOptions(
    per_process_gpu_memory_fraction=0.8
))
        
sess = tf.compat.v1.Session(config=config)
```
