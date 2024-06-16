# `kdenlive`の`Effects`のレンダリング一覧: List of kdenlive Effect Rendering Demos

## はじめに
Here are the rendering demos for all kdenlive effects.

`kdenlive`にはたいへん高機能な数多くのエフェクトが存在しますが、エフェクト名が特殊であったり数そのものが多いせいで敬遠されがちな印象です。
また慣れてくると「決まったエフェクトしか使わない」という問題が生じます。（主にわたし）
`kdenlive`には`KDE`の伝統なのか、しっかりしたドキュメントが存在します。この記事では可能な限り公式ドキュメントへのリンクを記述しました。
しかしながら、オプション引数の説明はあるものの、肝心の「このエフェクトはどのようなレンダリング結果になるか」が明瞭ではありません。
一応YouTubeのリンクが貼ってありますが`kdenlive`のバージョンが`0.7.5`、2009年にアップロードされている等、非常に古いデモになっています。
[Effects Demos](https://docs.kdenlive.org/en/effects_and_compositions.html#effects-demos)
    - https://youtu.be/C6oeu2Yc64I
    - https://youtu.be/jrC4F_G64jAg
    - https://youtu.be/XMoSgHHbA4k

ここでは一度腰を据えて、全エフェクトのレンダリング例を記載し、整理したいと思います。
なおエフェクトにはオーディオと映像がありますが、この記事では映像のみを扱います。

- [`kdenlive`の`Effects`のレンダリング一覧: List of kdenlive Effect Rendering Demos](#kdenliveのeffectsのレンダリング一覧-list-of-kdenlive-effect-rendering-demos)
  - [はじめに](#はじめに)
  - [注意事項](#注意事項)
  - [環境](#環境)
  - [参考](#参考)
  - [エフェクトデモ一覧: List of Effect Demos](#エフェクトデモ一覧-list-of-effect-demos)
    - [Grain and Noise](#grain-and-noise)
      - [ノイズ加算: Noise Addition](#ノイズ加算-noise-addition)
        - [Dust](#dust)
        - [Median](#median)
        - [Video Noise Generator](#video-noise-generator)
      - [デノイズ: Denoise](#デノイズ-denoise)
        - [3D FFT Denoiser](#3d-fft-denoiser)
        - [Chroma Noise Reduction](#chroma-noise-reduction)
        - [Denoiser](#denoiser)
        - [Gradfun](#gradfun)
    - [Image adjustment](#image-adjustment)
      - [Color Matrix](#color-matrix)
      - [Color Space](#color-space)
      - [Deband](#deband)
      - [Dilation](#dilation)
      - [EPX Scaler](#epx-scaler)
      - [Erosion](#erosion)
      - [Hq\*x Interpolator](#hqx-interpolator)
      - [Interlace field order](#interlace-field-order)
      - [Interleave - Deinterleave](#interleave---deinterleave)
      - [Kernel Deinterlacer](#kernel-deinterlacer)
      - [Motion compensation Deinterlacer](#motion-compensation-deinterlacer)
      - [Phase](#phase)
      - [Set Range](#set-range)
      - [Super2xsai](#super2xsai)
      - [xBR Interpolator](#xbr-interpolator)
    - [Transform, Distort and Perspective](#transform-distort-and-perspective)
      - [Corners](#corners)
      - [Crop by padding](#crop-by-padding)
      - [Crop Scale and Tilt](#crop-scale-and-tilt)
      - [Defish](#defish)
      - [Distort](#distort)
      - [Edge Crop](#edge-crop)
      - [Elastic scale filter](#elastic-scale-filter)
      - [Fill borders](#fill-borders)
      - [Flip Horizontally](#flip-horizontally)
      - [Flip Vertically](#flip-vertically)
      - [Flippo](#flippo)
      - [Lens correction](#lens-correction)
      - [Lens correction(keyframable)](#lens-correctionkeyframable)
      - [LetterB0xed](#letterb0xed)
      - [Mirror](#mirror)
      - [nosync0r(Broken TV)](#nosync0rbroken-tv)
      - [Pillar Echo](#pillar-echo)
      - [Position and Zoom](#position-and-zoom)
      - [Rotate(keyframable)](#rotatekeyframable)
      - [Rotate and Shear](#rotate-and-shear)
      - [Scroll](#scroll)
      - [Shear](#shear)
      - [Transform](#transform)
      - [Transpose](#transpose)
      - [Zoom Pan](#zoom-pan)
    - [VR360と3D: VR360 and 3D](#vr360と3d-vr360-and-3d)
      - [Stereoscopic 3D](#stereoscopic-3d)
      - [VR360 Equirectangular Mask](#vr360-equirectangular-mask)
      - [VR360 Equirectangular to Rectilinear](#vr360-equirectangular-to-rectilinear)
      - [VR360 Equirectangular to Stereo](#vr360-equirectangular-to-stereo)
      - [VR360 Hemispherical to Equirectangular](#vr360-hemispherical-to-equirectangular)
      - [VR360 Rectilinear to Equirectangular](#vr360-rectilinear-to-equirectangular)
      - [VR360 Stabilize](#vr360-stabilize)
      - [VR360 Transform](#vr360-transform)
    - [アルファ、マスク、キー: Alpha, Mask and Keying](#アルファマスクキー-alpha-mask-and-keying)
      - [Alpha gradient](#alpha-gradient)
      - [Alpha operations](#alpha-operations)
      - [Alpha shapes](#alpha-shapes)
      - [Alpha shapes(Mask)](#alpha-shapesmask)
      - [Alpha strobing](#alpha-strobing)
      - [Bluescreen0r](#bluescreen0r)
      - [Chroma Key: Advanced(Color Selection)](#chroma-key-advancedcolor-selection)
      - [Chroma Key: Basic](#chroma-key-basic)
      - [Despill](#despill)
    - [スタイル: Stylize](#スタイル-stylize)
      - [3-level\_Threshold](#3-level_threshold)
      - [Aech0r](#aech0r)
      - [Binarize](#binarize)
      - [Binarize\_dynamically](#binarize_dynamically)
      - [Cartoon](#cartoon)
      - [Charcoal](#charcoal)
      - [Chroma shift](#chroma-shift)
      - [Color\_Distance](#color_distance)
      - [Color\_Effect](#color_effect)
      - [Edge\_detection](#edge_detection)
      - [Edge\_glow](#edge_glow)
      - [ELBG\_Posterizer](#elbg_posterizer)
      - [Emboss](#emboss)
      - [Glow](#glow)
      - [Kirsch](#kirsch)
      - [NDVI\_filter](#ndvi_filter)
      - [Oldfilm](#oldfilm)
      - [Photosensitivity](#photosensitivity)
      - [Pixelize](#pixelize)
      - [Posterize](#posterize)
      - [Prewitt](#prewitt)
      - [Primaries](#primaries)
      - [RGBA\_Shift](#rgba_shift)
      - [rgbsplit0r](#rgbsplit0r)
      - [Roberts](#roberts)
      - [Sigmoidal\_Transfer](#sigmoidal_transfer)
      - [Sobel](#sobel)
      - [Sobel\_with\_planes](#sobel_with_planes)
      - [Soft\_Glow](#soft_glow)
      - [Threshold](#threshold)
    - [その他: Misc](#その他-misc)
      - [Alpha\_gradient](#alpha_gradient)
      - [Alpha\_shapes](#alpha_shapes)
      - [Alphaextract](#alphaextract)
      - [Backgroundkey](#backgroundkey)
      - [Basic\_Image\_Converter](#basic_image_converter)
      - [Bigsh0t\_eq\_cap](#bigsh0t_eq_cap)
      - [Bigsh0t\_eq\_wrap](#bigsh0t_eq_wrap)
      - [Bwdif\_cuda](#bwdif_cuda)
      - [Ccrepack](#ccrepack)
    - [ぼかしとシャープネス: Blur and Sharpen](#ぼかしとシャープネス-blur-and-sharpen)
      - [Average\_Blur](#average_blur)
      - [Bilateral](#bilateral)
      - [BoxBlur](#boxblur)
      - [Contrast\_Adaptive\_Sharpen](#contrast_adaptive_sharpen)
      - [DBlur](#dblur)
      - [Gaussian\_Blur](#gaussian_blur)
      - [Planes\_Blur](#planes_blur)
      - [Shape\_Adaptive\_Blur](#shape_adaptive_blur)
      - [Sharp\_unsharp](#sharp_unsharp)
      - [Smartblur](#smartblur)
      - [Square\_Blur](#square_blur)
    - [マスター上: On Master](#マスター上-on-master)
    - [モーション: Motion](#モーション-motion)
      - [Fade\_in](#fade_in)
      - [Fade\_out](#fade_out)
      - [Freeze](#freeze)
      - [Glitch0r](#glitch0r)
      - [Nervous](#nervous)
      - [Vertigo](#vertigo)
    - [ユーティリティ: Utility](#ユーティリティ-utility)
    - [色と画像の補正: Color and Image correction](#色と画像の補正-color-and-image-correction)
      - [3\_point\_balance](#3_point_balance)
      - [Apply\_LUT](#apply_lut)
      - [Bezier\_curves](#bezier_curves)
      - [Brightness](#brightness)
      - [Brightness\_keyframable](#brightness_keyframable)
      - [Bw0r](#bw0r)
    - [生成: Generate](#生成-generate)
      - [Cairogradient](#cairogradient)
      - [Draw\_Box](#draw_box)
      - [Draw\_Grid](#draw_grid)
      - [Dynamic\_Text](#dynamic_text)
      - [GPS\_Text](#gps_text)
      - [scanline0r](#scanline0r)
      - [Timer](#timer)
      - [Video\_grid](#video_grid)
      - [Vignette](#vignette)
      - [Vignette\_Effect](#vignette_effect)
    - [非推奨: Deprecated](#非推奨-deprecated)
      - [Wave](#wave)
  - [最後に](#最後に)


## 注意事項
- ~~膨大な数のエフェクトがあるため、随時追記を行います。ご了承ください。（このような追記スタイルが`Zenn`の記事執筆ポリシーに違反している場合、教えていただけると幸いです。その場合は後述の`GitHub`のリポジトリのみを公開いたします。）~~ 
全てのリストが完成しました。後述のとおり静止画以外のエフェクトデモを追加するかは未定です。
- 静止画に対してのレンダリング結果をGIF形式で表示します。そのため、素材が動画であることを前提としたエフェクト、例えばデノイズ系やモーションキャプチャーなどは（今の所）対象外とします。
- 後述の「環境」にて検証環境を記述しています。簡単には`Ubuntu 22.04, Kdenlive 24.02.2 (Flatpak ver.)`にて行っています。`Windows`や`MacOS`での`kdenlive`では動作が異なる可能性があります。各OSごとの対応表は[こちら](https://docs.kdenlive.org/en/effects_and_compositions/lists/video_effects_list.html)を参照してください。
  - ![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/2024-06-15-19-17-14.png)
- 全てのレンダリング結果 (gif images) は[GitHubのリポジトリ](https://github.com/yKesamaru/kdenlive_effects_sample)から引っ張ってきています。表示が遅い場合はそちらを参照してください。
- `mp4`から`gif`への変換は以下のコマンドラインを使用しました。
  ```bash
  for file in *.mp4; do ffmpeg -i "$file" "${file%.mp4}.gif"; done
  ```
  なにが言いたいかというと、`gif`の品質を考慮していない、ということです。その辺りについては[動画GIF変換コードの19種比較検証](https://zenn.dev/ykesamaru/articles/98640cadf3e476)をご参照ください。

![元画像](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/example.png)
元画像

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



## エフェクトデモ一覧: List of Effect Demos
### Grain and Noise
#### ノイズ加算: Noise Addition
##### [Dust](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/dust.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Dust.gif)
##### [Median](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/median.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Median.gif)
##### [Video Noise Generator](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/video_noise_generator.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Video_Noise_generator.gif)
#### デノイズ: Denoise
##### 3D FFT Denoiser
##### Chroma Noise Reduction
##### Denoiser
##### [Gradfun](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/grain_and_noise/gradfun.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Gradfun.gif)

### Image adjustment
#### Color Matrix
#### [Color Space](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/image_adjustment/color_space.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Color_Space.gif)
#### [Deband](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/image_adjustment/deband.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Deband.gif)
#### Dilation
#### EPX Scaler
#### Erosion
#### Hq*x Interpolator
#### Interlace field order
#### Interleave - Deinterleave
#### Kernel Deinterlacer
#### Motion compensation Deinterlacer
#### Phase
#### Set Range
#### Super2xsai
#### xBR Interpolator

### Transform, Distort and Perspective
#### [Corners](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/corners.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Corners.gif)
#### [Crop by padding](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/crop_padding.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Crop_by_padding.gif)
#### [Crop Scale and Tilt](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/crop_scale_tilt.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Crop_Scale_and_Tilt.gif)
#### [Defish](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/defish.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Defish.gif)
#### [Distort](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/distort.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Distort.gif)
#### [Edge Crop](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/edge_crop.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Edge_Crop.gif)
#### [Elastic scale filter](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/elastic_scale_filter.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Elastic_scale_filter.gif)
#### [Fill borders](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/fill_borders.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Fill_borders.gif)
#### [Flip Horizontally](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/flip_horizontally.html)
#### Flip Vertically
#### [Flippo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/flippo.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Flippo.gif)
#### [Lens correction](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/lens_correction.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Lens_correction.gif)
#### [Lens correction(keyframable)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/lens_correction_keyframe.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Lens_correction(keyframable).gif)
#### [LetterB0xed](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/letterb0xed.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/LetterB0xed.gif)
#### [Mirror](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/mirror.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Mirror.gif)
#### [nosync0r(Broken TV)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/nosync0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/nosync0r.gif)
#### [Pillar Echo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/pillar_echo.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Pillar_Echo.gif)
#### [Position and Zoom](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/position_and_zoom.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Position_and_Zoom.gif)
#### [Rotate(keyframable)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/rotate_keyframable.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Rotate(keyframable).gif)
#### [Rotate and Shear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/rotate_and_shear.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Rotate_and_Shear.gif)
#### [Scroll](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/scroll.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Scroll.gif)
#### [Shear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/shear.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Shear.gif)
#### [Transform](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/transform.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Transform.gif)
#### [Transpose](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/transpose.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Transpose.gif)
#### [Zoom Pan](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/transform_distort_perspective/zoom_pan.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Zoom_Pan.gif)

### VR360と3D: VR360 and 3D
#### [Stereoscopic 3D](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/stereoscopic_3d.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Stereoscopic_3D.gif)
#### [VR360 Equirectangular Mask](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi_mask.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_Mask.gif)
#### [VR360 Equirectangular to Rectilinear](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi2rect.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_to_Rectilinear.gif)
#### [VR360 Equirectangular to Stereo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_equi2stereo.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Equirectangular_to_Stereo.gif)
#### [VR360 Hemispherical to Equirectangular](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_hemi2equi.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Hemispherical_to_Equirectangular.gif)
#### [VR360 Rectilinear to Equirectangular](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_rect2equi.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Rectilinear_to_Equirectangular.gif)
#### [VR360 Stabilize](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_stabilize.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Stabilize.gif)
#### [VR360 Transform](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/vr360_and_3d/vr360_transform.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/VR360_Transform.gif)

### アルファ、マスク、キー: Alpha, Mask and Keying
#### [Alpha gradient](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_gradient.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_gradient.gif)
#### [Alpha operations](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_operations.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_operations.gif)
#### [Alpha shapes](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_shapes.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_shapes.gif)
#### [Alpha shapes(Mask)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_shapes_mask.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_shapes(Mask).gif)
#### [Alpha strobing](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/alpha_strobing.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Alpha_strobing.gif)
#### [Bluescreen0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/bluescreen0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Bluescreen0r.gif)
#### [Chroma Key: Advanced(Color Selection)](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/chroma_key_advanced.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Chroma_Key:_Advanced(Color_Selection).gif)
#### [Chroma Key: Basic](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/chroma_key.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Chroma_Key:_Basic.gif)
#### [Despill](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/alpha_mask_keying/despill.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Despill.gif)

### スタイル: Stylize
#### [3-level_Threshold](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/3-level_threshold.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/3-level_Threshold.gif)
#### [Aech0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/aech0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Aech0r.gif)
#### [Binarize](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/binarize.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Binarize.gif)
#### [Binarize_dynamically](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/binarize_dynamically.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Binarize_dynamically.gif)
#### [Cartoon](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/cartoon.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Cartoon.gif)
#### [Charcoal](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/charcoal.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Charcoal.gif)
#### Chroma shift
#### [Color_Distance](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/color_distance.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Color_Distance.gif)
#### [Color_Effect](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/color_effect.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Color_Effect.gif)
#### [Edge_detection](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/edge_detection.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Edge_detection.gif)
#### [Edge_glow](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/edge_glow.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Edge_glow.gif)
#### [ELBG_Posterizer](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/elbg_posterizer.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/ELBG_Posterizer.gif)
#### [Emboss](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/emboss.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Emboss.gif)
#### [Glow](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/glow.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Glow.gif)
#### [Kirsch](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/kirsch.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Kirsch.gif)
#### [NDVI_filter](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/ndvi_filter.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/NDVI_filter.gif)
#### [Oldfilm](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/oldfilm.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Oldfilm.gif)
#### Photosensitivity
#### [Pixelize](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/pixelize.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Pixelize.gif)
#### [Posterize](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/posterize.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Posterize.gif)
#### [Prewitt](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/prewitt.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Prewitt.gif)
#### [Primaries](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/primaries.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Primaries.gif)
#### [RGBA_Shift](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/rgba_shift.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/RGBA_Shift.gif)
#### [rgbsplit0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/rgbsplit0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/rgbsplit0r.gif)
#### [Roberts](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/roberts.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Roberts.gif)
#### [Sigmoidal_Transfer](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/sigmoidal_transfer.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Sigmoidal_Transfer.gif)
#### [Sobel](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/sobel.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Sigmoidal_Transfer.gif)
#### [Sobel_with_planes](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/sobel_planes.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Sobel_with_planes.gif)
#### [Soft_Glow](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/soft_glow.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Soft_Glow.gif)
#### [Threshold](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/stylize/threshold.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Threshold.gif)

### その他: Misc
`kdenlive`が強制終了されることが多いため、この項目は検証を中止。また、この項目の多くはドキュメント化されていない様子。
#### [Alpha_gradient]()
#### [Alpha_shapes]()
#### Alphaextract
#### [Backgroundkey](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/misc/backgroundkey.html#backgroundkey)
#### Basic_Image_Converter
#### [Bigsh0t_eq_cap]()
#### Bigsh0t_eq_wrap
#### Bwdif_cuda
#### Ccrepack

### ぼかしとシャープネス: Blur and Sharpen
#### [Average_Blur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/average_blur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Average_Blur.gif)
#### [Bilateral](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/bilateral.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Bilateral.gif)
#### [BoxBlur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/boxblur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/BoxBlur.gif)
#### [Contrast_Adaptive_Sharpen](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/contrast_adaptive_sharpen.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Contrast_Adaptive_Sharpen.gif)
#### [DBlur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/dblur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/DBlur.gif)
#### [Gaussian_Blur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/gaussian_blur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Gaussian_Blur.gif)
#### [Planes_Blur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/planes_blur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Planes_Blur.gif)
#### [Shape_Adaptive_Blur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/shape_adaptive_blur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Shape_Adaptive_Blur.gif)
#### [Sharp_unsharp](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/sharp_unsharp.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Sharp_unsharp.gif)
#### [Smartblur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/smartblur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Smartblur.gif)
#### [Square_Blur](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/blur_and_sharpen/square_blur.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Square_Blur.gif)

### マスター上: On Master

### モーション: Motion
#### Fade_in
#### Fade_out
#### Freeze
#### [Glitch0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/motion/glitch0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Glitch0r.gif)
#### Nervous
#### [Vertigo](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/motion/vertigo.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Vertigo.gif)

### ユーティリティ: Utility

### 色と画像の補正: Color and Image correction
#### 3_point_balance
#### Apply_LUT
#### [Bezier_curves](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/color_image_correction/bezier_curves.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Bezier_curves.gif)
#### [Brightness](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/color_image_correction/brightness.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Brightness.gif)
#### [Brightness_keyframable](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/color_image_correction/brightness_keyframable.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Brightness_keyframable.gif)
#### [Bw0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/color_image_correction/bw0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Bw0r.gif)

### 生成: Generate
#### [Cairogradient](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/cairogradient.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Cairogradient.gif)
#### [Draw_Box](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/drawbox.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Draw_Box.gif)
#### [Draw_Grid](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/drawgrid.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Draw_Grid.gif)
#### [Dynamic_Text](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/dynamic_text.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Dynamic_Text.gif)
#### GPS_Text
#### [scanline0r](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/scanline0r.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/scanline0r.gif)
#### [Timer](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/timer.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Timer.gif)
#### [Video_grid](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/video_grid.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Video_grid.gif)
#### [Vignette](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/vignette.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Vignette.gif)
#### [Vignette_Effect](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/generate/vignette_effect.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Vignette_Effect.gif)

### 非推奨: Deprecated
#### [Wave](https://docs.kdenlive.org/en/effects_and_compositions/video_effects/deprecated/wave.html)
![](https://raw.githubusercontent.com/yKesamaru/kdenlive_effects_sample/master/assets/Wave.gif)


## 最後に
映像系エフェクトは全てリストアップできました。
このようなデモ一覧がわたしの観測圏内では存在しませんでしたので作成した次第です。

`kdenlive`は最近色味の機能にも力を入れているような印象を受けます。
色味に関しては専門知識が必要なため、今回の記事では深く掘り下げていません。

以上です。ありがとうございました。