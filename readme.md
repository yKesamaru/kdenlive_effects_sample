# `kdenlive`の`Effects`の例
## はじめに
`kdenlive`はたいへん高機能なゆえに学習曲線の問題があります。
また慣れてくると「決まったエフェクトしか使わない」という問題が生じます。
ここでは一度腰を据えて、全エフェクトの例を記載し、整理したいと思います。
なおエフェクトにはオーディオと映像がありますが、この記事では映像のみを扱います。

![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/example.png)

## 環境
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/2024-06-15-09-18-48.png)
```bash
# kdenlive
# 24.02.2 (Flatpak版)

$ inxi -Sxxx --filter
System:
  Kernel: 6.5.0-35-generic x86_64 bits: 64 compiler: N/A Desktop: Unity
    wm: gnome-shell dm: GDM3 42.0 Distro: Ubuntu 22.04.4 LTS (Jammy Jellyfish)
```

## 参考
[Kdenlive Manual](https://docs.kdenlive.org/en/index.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/2024-06-15-14-04-03.png)
[Effects and Compositions](https://docs.kdenlive.org/en/effects_and_compositions.html)

## カテゴリー
- Grain and Noise
  - ノイズ加算
    - [Dust](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/dust.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Dust.gif)
    - [Median](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/median.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Median.gif)
    - [Video Noise Generator](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/video_noise_generator.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Video_Noise_generator.gif)
  - デノイズ
    - 3D FFT Denoiser
    - Chroma Noise Reduction
    - Denoiser
    - [Gradfun](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/gradfun.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Gradfun.gif)
- Image adjustment
  - Color Matrix
  - [Color Space](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/image_adjustment/color_space.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Color_Space.gif)
  - [Deband](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/image_adjustment/deband.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Deband.gif)
  - Dilation
  - EPX Scaler
  - Erosion
  - Hq*x Interpolator
  - Interlace field order
  - Interleave - Deinterleave
  - Kernel Deinterlacer
  - Motion compensation Deinterlacer
  - Phase
  - Set Range
  - Super2xsai
  - xBR Interpolator
- Transform, Distort and Perspective
  - [Corners](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/corners.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Corners.gif)
  - [Crop by padding](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/crop_padding.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Crop_by_padding.gif)
  - [Crop Scale and Tilt](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/crop_scale_tilt.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Crop_Scale_and_Tilt.gif)
  - [Defish](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/defish.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Defish.gif)
  - [Distort](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/distort.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Distort.gif)
  - [Edge Crop](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/edge_crop.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Edge_Crop.gif)
  - [Elastic scale filter](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/elastic_scale_filter.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Elastic_scale_filter.gif)
  - [Fill borders](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/fill_borders.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Fill_borders.gif)
  - [Flip Horizontally](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/flip_horizontally.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Flip_Horizontally.gif)
  - Flip Vertically
  - [Flippo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/flippo.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Flippo.gif)
  - [Lens correction](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/lens_correction.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Lens_correction.gif)
  - [Lens correction(keyframable)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/lens_correction_keyframe.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Lens_correction(keyframable).gif)
  - [LetterB0xed](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/letterb0xed.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/LetterB0xed.gif)
  - [Mirror](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/mirror.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Mirror.gif)
  - [nosync0r(Broken TV)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/nosync0r.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/nosync0r.gif)
  - [Pillar Echo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/pillar_echo.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Pillar_Echo.gif)
  - [Position and Zoom](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/position_and_zoom.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Position_and_Zoom.gif)
  - [Rotate(keyframable)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/rotate_keyframable.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Rotate(keyframable).gif)
  - [Rotate and Shear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/rotate_and_shear.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Rotate_and_Shear.gif)
  - [Scroll](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/scroll.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Scroll.gif)
  - [Shear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/shear.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Shear.gif)
  - [Transform](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/transform.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Transform.gif)
  - [Transpose](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/transpose.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Transpose.gif)
  - [Zoom Pan](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/zoom_pan.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Zoom_Pan.gif)
- VR360と3D
  - [Stereoscopic 3D](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/stereoscopic_3d.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Stereoscopic_3D.gif)
  - [VR360 Equirectangular Mask](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi_mask.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_Mask.gif)
  - [VR360 Equirectangular to Rectilinear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi2rect.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_to_Rectilinear.gif)
  - [VR360 Equirectangular to Stereo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi2stereo.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_to_Stereo.gif)
  - [VR360 Hemispherical to Equirectangular](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_hemi2equi.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Hemispherical_to_Equirectangular.gif)
  - [VR360 Rectilinear to Equirectangular](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_rect2equi.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Rectilinear_to_Equirectangular.gif)
  - [VR360 Stabilize](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_stabilize.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Stabilize.gif)
  - [VR360 Transform](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_transform.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Transform.gif)
- アルファ、マスク、キー
  - [Alpha gradient](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_gradient.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_gradient.gif)
  - [Alpha operations](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_operations.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_operations.gif)
  - [Alpha shapes](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_shapes.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_shapes.gif)
  - [Alpha shapes(Mask)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_shapes_mask.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_shapes(Mask).gif)
  - [Alpha strobing](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_strobing.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_strobing.gif)
  - [Bluescreen0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/bluescreen0r.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Bluescreen0r.gif)
  - [Chroma Key: Advanced(Color Selection)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/chroma_key_advanced.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Chroma_Key:_Advanced(Color_Selection).gif)
  - [Chroma Key: Basic](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/chroma_key.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Chroma_Key:_Basic.gif)
  - [Despill](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/despill.html)
    - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Despill.gif)
- スタイル
- その他
- ぼかしとシャープネス
- マスター上
- モーション
- ユーティリティ
- 色と画像の補正
- 生成
- 非推奨


