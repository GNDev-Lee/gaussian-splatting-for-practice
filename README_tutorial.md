## Additional Dependency

Additioan dependencies which were not required for original 3DGS code but do for our tutorial

```sh
pip install vispy>=0.14.3 jupyter_rfb==0.4.3
```

vispy and jupyter_rfb 버전을 구체적으로 지정한 것은 [참고자료](https://github.com/KAIST-VCLAB/frame-free-polar-representation/blob/master/polarsh/requirements.txt)를 따랐음.


## Tutorial Files

`tutorial_convert_py.ipynb` - 가지고 있는 사진(input)에 해당하는 points3D.ply를 COLMAP을 통해 만들어내고 중간중간 생성되는 images.bin, points3D.bin, cameras.bin 데이터들의 차이점을 비교해본다.
`tutorial_train_py.ipynb` - train.py 내부에 있는 코드(training)를 line by line으로 분석한 내용을 보인다.
`tutorial_3DGS.ipynb` - convert.py를 한 번 진행한 뒤 train.py 내부에서 한 번의 iteration을 진행한 내용을 보인다.
`tutorial_3DGS_after_600_iter.ipynb` -  densify_and_prune 함수가 500번의 iteration 이후 100번마다 clone, split을 진행하는데 이를 보이기 위해 600번 iteration 이후에 어떤 식으로 clone, split이 진행되는지 보인다.
`tutorial_Vispy` - 시각화를 위한 Vispy 라이브러리를 사용하는 것을 다룬 파일이다.
`tutorial_SSIM` - SSIM이 무엇이며 어떤 식으로 진행하는지를 다룬 파일이다.
`tutorial_rasterization` - render 함수 내부에서 일어나는 일들(Forward라고 봐도 됨)과 train.py 내부에서 구해진 loss의 gradient가 어떤 방식으로 gaussians들의 각 멤버 변수에 적용되는지를 다룬 파일이다.