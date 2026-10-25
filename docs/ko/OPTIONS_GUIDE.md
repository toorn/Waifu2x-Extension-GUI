# Waifu2x-Extension-GUI — 한국어 옵션 매뉴얼

> 비공식 한국어 설명서 / 작성 2026-10-25  
> **기준:** [공식 README](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/README.md), [공개된 Qt UI 정의 파일(v3.41.01-beta)](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/SRC_v3.41.01-beta/Waifu2x-Extension-QT/mainwindow.ui)의 메뉴 문구와 툴팁. 실제 최신 릴리스에는 다른 항목이나 기본값이 있을 수 있습니다.  
> **자료 성격:** 화면 문구를 한국어로 해설한 사용 설명서. 프로그램 자체 UI의 한국어 번역을 설치하는 패치는 아닙니다.

## 목차

1. [기본 사용](#1-기본-사용)
2. [Home 옵션](#2-home-옵션)
3. [Engine settings](#3-engine-settings)
4. [Video settings](#4-video-settings)
5. [Additional settings](#5-additional-settings)
6. [실사용 예시](#6-실사용-예시)
7. [고장·오류 해결](#7-고장오류-해결)

## 1. 기본 사용

Waifu2x-Extension-GUI는 이미지·애니메이션 GIF·동영상 **초해상도 확대, 노이즈 제거, 동영상 프레임 보간**을 하나의 그래픽 인터페이스에서 관리하는 Windows x64용 프로그램입니다. NVIDIA·AMD·Intel GPU 및 여러 엔진을 지원하지만, 실제 기능은 GPU/프로그램 버전에 따라 다릅니다.

- [공식 최신 배포본](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/releases/latest) / [공식 변경 이력](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Change_log.md)
- 설정 화면: [Home](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Screenshot/mainwindow.jpg) · [Engine](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Screenshot/Engine_Settings_EN.jpg) · [Video](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Screenshot/VideoSettings_EN.jpg) · [Additional](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Screenshot/Additional_Settings_EN.jpg)

**실행 순서:** Additional settings에서 호환성 테스트 → Home에서 파일·배율·출력 폴더 → Engine settings에서 엔진 → 동영상이면 Video settings → 짧은 샘플 처리 후 결과 확인.

**원본 보호:** 처음에는 `Replace original file`, `Delete original files`, `Overwrite`를 전부 끄고 결과를 별도 폴더로 저장하는 것이 안전합니다.

## 2. Home 옵션

| 영문 표시 | 한국어 의미 · 사용 시 주의 |
|---|---|
| **Files List** | 입력 파일 목록. 파일이나 폴더를 끌어 놓거나 추가 버튼 사용. |
| **Start / Pause** | 작업 시작 / 일시정지. |
| **Force retry** | 엔진 처리 중 멈췄을 때 엔진 프로세스를 재시작하여 다시 시도. |
| **Custom resolution (Width / Height)** | 선택한 파일에 출력 가로·세로 픽셀 수를 직접 지정. 해당 파일에는 일반 확대 비율 설정을 적용하지 않음. |
| **Ignore Aspect Ratio** | 비율을 무시하고 지정 크기로 맞춤. 원본이 늘어나거나 찌그러질 수 있음. |
| **Keep Aspect Ratio** | 원본 종횡비를 유지하며 크기 맞춤. |
| **Keep Aspect Ratio By Expanding** | 비율을 유지하면서 지정 영역을 채우도록 확대. 가장자리 처리 결과 확인 필요. |
| **Apply / Cancel** | 선택한 파일에 사용자 해상도 적용 / 해제. |
| **Apply to all** | 설정을 목록의 모든 대상에 적용. |
| **Auto Skip** | 조건에서 지정한 해상도보다 큰 파일은 건너뜀. |
| **Scale ratio** | 확대 배율. 배율이 클수록 처리 픽셀 수와 요구 자원 증가. |
| **Image Style: 2D Anime** | 애니메이션·선화·일러스트용 모델 선택. |
| **Image Style: 3D Real-life** | 실사 사진·동영상용 모델 선택. |
| **Save image as** | 정지 이미지 결과 형식(PNG/JPG/WebP 등). 비디오 인코딩 설정과 별개. |
| **Image quality** | 손실 압축 이미지 저장 품질. 큰 값은 파일 용량 증가 가능. |
| **Optimize GIF** | 결과 GIF 최적화로 파일 크기 감소. 약간의 화질 저하 가능. |
| **Delete original files** | 처리 후 입력 원본 삭제. 백업 전 활성화 금지 권장. |
| **Replace original file** | 출력으로 기존 입력을 대체. 원본이 삭제되므로 특히 주의. |
| **Output path(Folder) / Enabled** | 결과 저장 폴더를 지정하고 활성화. 비활성화 시 기본 출력 위치 사용. |
| **Overwrite** | 출력 폴더에 같은 이름의 파일이 존재할 때 덮어씀. |
| **Keep original file name** | 원본 파일명을 결과에도 가능한 한 유지. |
| **Keep parent folder** | 결과 저장 시 원본 상위 폴더 구조 유지. |
| **Auto-open after finished** | 작업 후 결과 폴더 자동 열기. |
| **Video Frame Interpolation** | 동영상 프레임 보간 실행. 세부 보간 엔진은 Video settings에서 설정. |
| **Frame Interpolation only(Video)** | 초해상도 확대 없이 프레임 보간만 실행. |
| **Re-process finished files** | 이미 완료된 목록 항목을 재실행 때 다시 처리. |
| **Do nothing / Shut down / Sleep / Hibernate / Restart** | 작업 종료 후 PC 동작 지정. |
| **Save Files List / Read Files List** | 파일 목록을 저장하고 다시 불러오기. |
| **Turn off screen** | 프로그램 내 화면 끄기 기능. 자동 절전으로 작업이 중단되지 않도록 별도 점검. |

## 3. Engine settings

엔진은 확대 방식을 결정합니다. 결과는 모델 버전·원본 화질·기기 성능에 따라 크게 달라지므로 **동일한 샘플을 비교**해야 합니다.

### 3.1 엔진 종류와 적합한 용도

| 엔진 | 주요 용도와 특성 |
|---|---|
| **Waifu2x-ncnn-vulkan** | 2D 애니메이션·그림 계열 초해상도, Vulkan GPU 기반. |
| **Waifu2x-caffe** | 애니/실사 모델 선택, CPU/GPU/cuDNN 처리 모드 지원 여부 확인 필요. |
| **Waifu2x-converter** | Waifu2x 계열 별도 구현. Processor·Block 설정 확인. |
| **SRMD-ncnn-vulkan** | 실사·압축 잡음이 있는 영상 등. Tile size로 메모리 제어. |
| **RealSR-ncnn-vulkan** | 사진·실사 확대에 초점. 모델별 노이즈 제거 지원 여부가 다름. |
| **Real-ESRGAN** | 딥러닝 초해상도 모델 계열. 지원 모델과 엔진은 설치 버전에서 확인. |
| **Real-CUGAN** | 애니메이션·일러스트 모델 계열. 원본 그림체 보존 여부를 비교. |
| **Anime4K / Anime4KCPP** | 선화·애니 중심의 빠른 영상 확대. GPU Mode와 필터를 조합. |
| **RTX Super Resolution** | 지원되는 NVIDIA RTX 환경에서만 작동하는 엔진. 앱·드라이버 지원 범위 확인. |

### 3.2 공통 엔진 옵션

| 옵션 | 역할 | 조정 요령 |
|---|---|---|
| **GPU ID / Processor ID** | 어느 처리 장치를 사용할지 지정하는 번호. | 자동 감지로 번호를 먼저 확인. |
| **Detect available GPU ID / Dump processor list** | 사용 가능한 그래픽 장치/연산 장치 목록 표시. | 멀티 GPU 구성 전 실행. |
| **Tile size** | 입력을 조각으로 나눌 때 조각 크기. | 값이 크면 VRAM 사용량이 증가할 수 있음. 메모리 오류 시 감소. |
| **Split size / Block size** | 엔진 내부 입력 분할 크기. | 큰 값은 메모리를 더 사용하지만 속도 이점 가능. |
| **Batch size** | 동시에 처리하는 묶음의 크기. | 메모리 오류 시 감소. |
| **Threads / Multithreading** | 동시 처리 작업 수. | 너무 높이면 오히려 느려지거나 메모리 오류 발생 가능. |
| **Multi-GPU / Multi-Processor** | 여러 장치에 연산 분산. | GPU/스레드 수와 엔진 지원 여부를 확인. |
| **TTA (Test-Time Augmentation)** | 변형 입력을 여러 번 추론 후 결과 통합. | 처리 시간·메모리 증가. 기본적으로 끄고 비교 권장. |
| **Denoise level** | 노이즈 제거 강도. | 과하게 적용하면 미세 디테일 손실. |
| **Process mode: CPU / GPU / cuDNN** | 연산 백엔드 선택. | cuDNN은 NVIDIA 및 적합한 엔진 빌드 필요. |
| **Model** | 선택된 엔진의 학습 모델. | 이미지 유형(애니/실사)과 노이즈 지원을 구분. |

### 3.3 Waifu2x-caffe

- **2D Anime Model**: UI 정의 파일에는 `anime_style_art_rgb`, `anime_style_art`, `cunet`, `upconv_7_anime_style_art_rgb`, `upresnet10` 등이 등장.
- **3D Real-life Model**: `upconv_7_photo`, `photo` 등.
- **Process mode**: CPU / GPU / cuDNN. CPU 처리 속도가 느릴 수 있음.
- **Batch size / Split size**: 배치와 분할 크기. VRAM 부족 시 줄이기.
- **Multi-GPU**: GPU ID·배치·분할 크기 조합을 UI에서 안내하는 형식에 맞춰 입력. 숫자 구문을 잘못 입력하면 오류 가능.

### 3.4 Anime4K

| 세부 옵션 | 의미 |
|---|---|
| **GPU Mode** | GPU 가속 활성화. 먼저 하드웨어 호환성 확인. |
| **OpenCL / CUDA** | 계산 백엔드 선택. CUDA는 NVIDIA용. |
| **ACNet** | 신경망 기반 보강 처리. |
| **HDN mode** | ACNet의 고급 노이즈 억제. ACNet이 켜져야 동작. |
| **Fast mode** | 속도 우선 처리. 디테일 저하 가능. |
| **OpenCL parallel IO** | OpenCL 병렬 입출력. 호환성 문제가 발생할 수 있음. |
| **OpenCL command queues** | OpenCL 명령 큐 개수 조정. |
| **Enable Pre-processing / Post-processing** | 초해상도 전 / 후 필터 적용. |
| **Mean / Median blur** | 평균 / 중간값 흐림 처리. |
| **Gaussian blur (weak)** | 가우시안 흐림(약한 버전 포함). |
| **Bilateral filter (faster)** | 경계 보존을 고려한 양방향 필터. |
| **CAS Sharpening** | 대비 적응형 선명화. 과한 테두리 강조 주의. |
| **Push color strength / count** | 색상 보정 강조 정도와 횟수. |
| **Push gradient strength** | 기울기·선명도 강조 강도. |
| **Passes** | 추가 처리 반복 횟수. |

### 3.5 SRMD / RealSR 계열

- **Tile size**: VRAM 사용량을 크게 좌우. 문제가 생기면 작은 값으로 재실행.
- **RealSR models-DF2K_JPEG**: 공개 UI 도움말 기준 노이즈 제거 지원.
- **RealSR models-DF2K**: 같은 설명 기준 노이즈 제거 미지원.
- **Multi-GPU 설정**: 여러 GPU가 있는 경우에만 사용하고, 먼저 사용 가능 GPU ID를 검색.

## 4. Video settings

### 4.1 Frame Interpolation

기존 프레임 사이의 움직임을 추정해 새 프레임을 생성하는 기능입니다. 장면 전환이나 빠른 움직임에서 왜곡 가능성이 있습니다.

| 옵션 | 의미·영향 |
|---|---|
| **Frame Interpolation Engine** | RIFE, CAIN, DAIN 등 프레임 보간 엔진 선택. 공식 README에는 IFRNet 계열도 표기. |
| **RIFE model** | RIFE 세부 모델: `rife`, `rife-anime`, `rife-HD`, `rife-UHD`, `rife-v2`, `rife-v2.4` 등. |
| **UHD Mode** | RIFE 고해상도 처리 모드. 공개 UI에서는 3840×2160 초과 입력 때 자동 활성화 가능하다고 설명. |
| **TTA Mode** | 반복 추론에 의한 개선. 공개 UI 도움말 기준 약 8배 시간 증가, 결과 차이는 작을 수 있어 일반적으로 비권장. |
| **After Upscale** | 확대 후 보간. 기본값은 확대 전 보간으로 설명되며, 켜면 더 큰 프레임을 보간하므로 VRAM 요구량 증가 가능. |
| **Multi GPU** | 보간 GPU ID를 지정. 공개 UI 예시는 `0,1`; `-1`은 CPU로 설명. |
| **Multithreading** | 병렬 보간 수행. 공개 UI에서는 안정성 문제로 사용 비권장. |
| **Number of threads** | 동시 보간 작업 수. |
| **Auto adjust** | 연속 실패 감지 시 스레드 수 자동 조정. |

### 4.2 Audio denoise(for video)

**Denoise level**: 공개 UI에서 설정 범위 `0.01~1`, 기본값 `0.20`으로 설명. 높은 값은 잡음을 더 제거하지만 필요한 소리까지 제거할 위험도 증가합니다.

### 4.3 Custom video settings

| 옵션 | 역할 |
|---|---|
| **Encoder(video)** | FFmpeg 영상 인코더 선택. 공개 UI 예: `libx264`. |
| **Bitrate(video)** | 영상 비트레이트. 공개 UI 기준 `0`은 자동 설정. |
| **Encoder(audio)** | 오디오 인코더. UI 예: `aac`. |
| **Bitrate(audio)** | 오디오 비트레이트. |
| **Pixel format** | 픽셀 포맷. 예: `yuv420p`. 재생 호환성에 영향. |
| **Extra command** | FFmpeg 추가 인자 직접 입력. 문법 오류에 주의. |
| **List Available Encoders** | 현재 엔진에서 사용 가능한 인코더 확인. |
| **Reset video settings** | 비디오 설정 초기화. |

**중요:** 출력 인코더가 지원된다는 것과 GPU 하드웨어 가속이 실제 활성화되는 것은 별개의 문제입니다. FFmpeg 로그·출력 파일 정보로 확인하세요.

### 4.4 MP4 변환·분할

| 옵션 | 역할 |
|---|---|
| **When convert source video to CFR mp4** | 가변 프레임 속도 입력 등을 고정 프레임 속도 MP4로 변환하는 단계의 설정. |
| **Copy audio stream** | 오디오 스트림 복사(`-acodec copy`). 컨테이너 및 입력 FPS 모드에 따라 적용되지 않거나 오류 가능. |
| **Copy video stream** | 영상 스트림 복사(`-vcodec copy`). 코덱 호환성 및 VFR 여부에 주의. |
| **Ignore frame rate mode** | 입력 프레임률 모드 감지 무시. 공개 UI에서 오류 가능성을 경고함. |
| **Process video by segment** | 영상을 구간별로 처리하여 임시 저장 공간 사용을 줄이는 방식. 처리 시간이 증가할 수 있음. |
| **Segment duration** | 각 구간 길이(초). 구간을 길게 잡으면 임시 저장 공간 사용도 증가 가능. |

## 5. Additional settings

| 옵션 | 의미 · 사용법 |
|---|---|
| **Input file extensions** | 허용 확장자 직접 추가. 확장자는 `:`로 구분하며 추가한다고 무조건 처리 가능한 것은 아님. |
| **Pre-process all images** | 모든 이미지 입력을 PNG로 사전 변환. 호환성 향상 가능하나 시간·디스크 사용 증가. |
| **Auto detect Alpha channel** | 투명도 감지 시 PNG 결과 저장 유도. |
| **Always pre-process images with Alpha Channel** | 투명도 보존 문제로 재처리가 잦은 경우 사전 변환을 우선 수행. |
| **Custom font / Custom font size** | UI 글꼴과 크기 지정. 재시작 필요. |
| **Save Custom Font Settings** | 글꼴 설정 저장. |
| **Save settings / Reset settings** | 설정 저장 / 기본값 초기화. |
| **Check update** | 업데이트 확인. |
| **Update channel: Stable / Beta** | 안정판과 시험판 업데이트 채널. |
| **Update popup** | 업데이트 알림 팝업. |
| **Auto save settings** | 종료 시 설정 자동 저장. |
| **Disable "-resize"** | ImageMagick 관련 호환성 오류에 대응하는 설정. |
| **Prompt when exit** | 종료 전 확인창. |
| **Minimize to taskbar** | 최소화 동작 설정. |
| **Always hide Text Browser** | 실행 시 로그 텍스트 창 자동 숨김. |
| **Always hide Settings** | 실행 시 설정 영역 자동 숨김. |
| **Scan sub-folders** | 폴더 추가 시 하위 폴더도 검색. |
| **Retry** | 이미지/프레임 처리 실패 시 재시도 횟수. |
| **Ban Gitee** | Gitee 서버에서 데이터 내려받기 금지. 원본 README에 업데이트 확인 영향이 있을 수 있다고 설명. |
| **Language** | UI 언어 설정. 공개 UI 기준 한국어는 확인되지 않음. |
| **Notification sound** | 처리 완료 등 알림음. |
| **Automatic file list scrolling** | 목록에서 처리 상태 변경 시 자동 스크롤. |
| **Keep video cache** | 처리 후 임시 비디오 캐시 유지. 저장 공간 증가. |
| **Interactive file list** | 파일 목록 상호작용 관련 옵션. 세부 동작은 버전별 확인 필요. |
| **Show internal progress** | GIF/동영상 내부 처리 진행률을 로그에 표시. |
| **Summary popup** | 전체 작업 완료 후 요약 팝업. |
| **Compatibility test** | PC에서 사용 가능한 엔진과 도구의 호환성 검사. |
| **Report issue / Official website / Wiki / About** | 오류 제보 / 공식 사이트 / 위키 / 프로그램 정보. |

## 6. 실사용 예시

### 애니메이션 선화 확대
1. `Image Style → 2D Anime`.
2. 호환성 검사에서 정상인 `Waifu2x`·`Real-CUGAN`·`Anime4K`를 비교.
3. 얇은 선, 텍스트 가장자리, 눈동자 등 디테일을 동일 부분에서 비교.
4. 가장 부작용이 적은 엔진으로 본 작업을 시작.

### 사진·실사 동영상 확대
1. `Image Style → 3D Real-life`.
2. `RealSR`, `SRMD`, 지원된다면 `Real-ESRGAN`의 결과를 짧은 테스트로 비교.
3. 지나치게 강한 노이즈 제거와 선명화는 피함.
4. 비디오의 FPS·길이가 중요하면 처리 후 `ffprobe` 등으로 확인.

### 프레임 보간만 수행
1. Home에서 `Frame Interpolation only(Video)` 선택.
2. Video settings에서 RIFE 등 호환 엔진 선택.
3. 속도 테스트는 우선 TTA를 끄고 진행.
4. 장면 전환과 빠른 동작 부분을 미리 확인.

### RTX 5070 Ti 16GB에서 시험할 출발점
- **Compatibility test부터 실행**. GPU 제품명만으로 특정 엔진 호환을 단정하지 않음.
- 타일 크기·작업 스레드는 일단 기본값을 사용.
- VRAM 부족 시 Tile/Split/Batch 값을 감소.
- 긴 영상은 구간별 처리를 시도하되 추가 처리시간·여유 디스크를 확인.
- 원본은 보관하고 출력은 별도 폴더에 저장.

## 7. 고장·오류 해결

| 현상 | 우선 확인 |
|---|---|
| 엔진이 GPU를 찾지 못함 | Compatibility test → 드라이버 → 엔진 호환성 → GPU ID 자동 감지. |
| VRAM 부족 | Tile size / Split size / Batch size / Threads 감소. |
| 진행률 멈춤 | 로그·오류 확인 → Force retry → 짧은 샘플 재현. |
| 질감이 뭉개짐 | Denoise 강도 축소, 이미지 유형·모델 재선택. |
| 원본과 결과 길이가 다름 | VFR/CFR, 구간 처리, 출력 FPS 및 영상 길이 검사. |
| 파일 드래그 불가 | Windows에서 프로그램 관리자 권한 실행 여부 확인. |
| 투명도가 사라짐 | Alpha channel 자동 감지와 PNG 전처리 비교. |
| 원본 파일이 없어짐 | Replace original file / Delete original files / Overwrite 설정 확인. |

---

**참조:** [공식 README](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/README.md) · [공식 UI 소스](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/SRC_v3.41.01-beta/Waifu2x-Extension-QT/mainwindow.ui) · [공식 Change log](https://github.com/AaronFeng753/Waifu2x-Extension-GUI/blob/master/Change_log.md)

**완성도:** 소스 코드와 툴팁으로 확인한 옵션 설명 중심의 초판입니다. 실행 중 표시되는 모든 동적 팝업, 숨은 메뉴, 최신 릴리스 변경점에 대한 전수 검증은 별도 후속 작업이 필요합니다.
