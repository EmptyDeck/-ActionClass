### 프로젝트 시작 보고서

#### 프로젝트 제목:

**동영상 기반 범죄 행동 탐지 AI 시스템**

#### 목적과 배경

본 프로젝트는 CCTV를 이용한 실시간 범죄 행동 탐지를 목적으로 합니다. 이 시스템은 CCTV를 사용하는 일반 사용자들에게 제공되어 감시 효율을 높이는 것을 목표로 합니다.

#### 주요 기능 및 기술

-   **기술 스택**: PyTorch, LSTM, MediaPipe
-   **기능**: UCF-101 데이터셋을 이용한 동영상 분석, 스켈레톤 기반 행동 분석, 인식률이 높은 동영상을 사용한 모델 학습, 다중 인물 행동 분석

#### 예상 결과

완료 후, AI 시스템은 실시간으로 CCTV 동영상을 분석하여 범죄 행동을 식별하고 경보를 발생시킬 수 있을 것입니다.

### 진행 과정

#### 1. 데이터셋 준비 및 초기 활용

-   **UCF-101 데이터셋 사용**: 101개의 레이블로 구분된 사람 행동 동영상 데이터셋을 기반으로 합니다. 이 데이터셋에는 약 9000개의 동영상이 포함되어 있습니다.
-   **학습 코드 작성**: UCF-101 데이터셋을 효과적으로 학습시키기 위해 전용 학습 코드를 작성합니다.
-   **동영상 스켈레톤 변환**: 데이터셋의 모든 동영상을 스켈레톤 데이터로 변환하여 행동을 더 명확하게 분석할 수 있도록 합니다.

#### 2. 스켈레톤 적용 품질 검사

-   **스켈레톤 적용 동영상 제작**: 9000개 동영상에 스켈레톤 적용
    👈 <span style="color:red">**현재 여기 진행 중**</span>
-   **품질 검사**: 스켈레톤 적용 확인 및 부적합 동영상 제거

#### 3. 효율적인 데이터셋 구축

-   **최적화된 동영상 선택**: 스켈레톤이 잘 적용되는 적합한 동영상 확보
-   **CSV 파일 생성**: 각 동영상에 대해서 스켈레톤 데이터를 추출하고 CSV파일로 저장

#### 4. 모델 학습 및 평가

-   **학습 과정**: 스켈레톤 CSV 파일을 이용한 학습
-   **모델 성능 평가**: 학습률과 정확도 측정

#### 5. 범죄 동영상 및 일반 행동 학습

-   **범죄 동영상 학습**: 범죄 행위가 포함된 동영상을 수집하고, 이를 분석하여 학습 데이터셋으로 활용
-   **일반적인 행동 학습**: 걷기, 대화, 앉기 등의 일반적인 행동을 포함하는 동영상 수집 및 학습

#### 6. 멀티 행동 인식 알고리즘 개발

-   **인물 분리**: YOLO, SORT 알고리즘을 사용하여 한 동영상 내의 여러 사람들을 개별적으로 분리
-   **개별 동영상 생성**: 각 인물에 대한 바운딩 박스를 사용하여 개별 동영상 생성
-   **동시 분석**: 생성된 동영상들을 모델에 입력하여 여러 사람들의 행동을 동시에 분석
-   **범죄 행동 구별**: 특정 범죄 행동을 식별

#### 프로젝트 평가 및 보고

-   **진행 상황 보고**: 프로젝트의 진행 상황을 정기적으로 교수님에게 보고하고 피드백을 받음