# Team1. peacebite
### 3
ATM 사용자의 표정을 통한 감정인식과 전화통화 여부를 판별하여 보이스피싱 피해 예상고객을 탐지하는 AI 알고리즘을 완성하였습니다. 
또한 리액트로 ATM 전체 플로우를 포함하여 탐지된 보이스피싱 피해자에게 보여주는 3단계의 경고 화면까지 구현하였습니다.
### 4
1. OS - 윈도우 / BentoML
2. mysql
3. Web, Typescript, React
4. 웹
### 5
recoil, tailwindcss, react-webcam, react-chartjs
### 6
Emotion Recognition에서 사람 및 얼굴을 탐지하는데 Yolov3를 이용
Phone Detection에서 Yolov5를 이용
### 7
AWS 사용 예정이나 아직 연결하지 않았기 때문에 지출한 비용은 없습니다. 
### 8
2만장 이미지 인풋 15 epoch (1 epoch당 대략 1시간)
### 9
AWS 서버비용 50만원
### 11
내용 없음
### 12
멘토선정 도움필요
# Team2. 김서방
### 3
데이터 셋 수집 및 모델 학습을 했으며, 라즈베리파이4b 사진 촬영 및 서버 전송을 테스트해보았음 안드로이드 기반 앱 화면을 제작하였음 
### 4
1. Windows OS, flutter/dart
2. mysql/firebase
3. flutter/dart
4.안드로이드 기반 크로스 플랫폼 앱 
### 5
라즈베리파이4b 웹캠 카메라 사용 시 파이썬 opencv 활용(https://github.com/opencv/opencv)
라즈베리파이4b 라이브 스트리밍 시 motion 활용(https://github.com/Motion-Project/motion)
앱 qr인식(현재 문제 발견하여 변동 가능성 있음)(https://pub.dev/packages/qr_code_scanner)
### 6
Yolov5 이용하여 실시간 객체 인식(https://github.com/ultralytics/yolov5)
차후 Pytorch 이용하여 수정한 모델을 사용할 계획 (https://pytorch.org/)
### 7
Firebase: 라즈베리 파이에서 촬영된 사진 저장, 앱 데이터베이스로 사용
### 8
yolov5를 이용하여 10000개 이상의 이미지 학습 예정  사용(ai 모델의 경우, 개발과정에서 변동가능) 서비스를 위하여 라즈베리 파이에서 보내온 이미지들(또는 영상)을 저장 후 객체 인식 모델 run
### 12
스타트 멘토 계속
# Team3. 369
### 3
개발을 위한 IA, 기획서, 와이어프레임 등을 구성하였습니다. 또한 어플리케이션을 개발하고 초기 OCR 모델을 구축하였습니다.
### 4
1. Java, Spring, SpringBoot, AWS CodeDeploy, AWS S3, AWS EC2(Ubuntu 20), Github Action,  node.js/nest.js, python/flask
2. mysql(AWS RDS)
3. Flutter
4. 하이브리드 어플리케이션(iOS, Android 둘 다)
### 5
- 시스템 구성에 있어서 모든 항목은 직접 구현하였음
### 6
    1. 영수증에서의 horizontal text detection을 위한 CTPN (Connectionist Text Proposal Network)를 PyTorch를 사용하여 구현하였음.

    2. 영수증에서 감지한 <text 영역>에서의 문자를 검출하기 위하여 HENNet(=Hangul English Number Net)을 (영감을 준 source는 한글만을 위한 HangulNet, 2022이었으나 우리 서비스의 특성상 영어와 숫자 인식이 필수였기에 영어와 숫자인식도 가능하도록 모듈을 변형) Pytorch 로 구현하여 현재 학습중임.

    3. 영수증에서 각 검출한 문자들이 <상품>인지, <수량>인지등의 유형도 구분하여서 서비스에서 유저에게 보여줘야 하기 때문에 우선은 영수증에서의 상대적인 위치등을 기반으로 나누어줄 생각이다. (여기서는 최대한 AI기술을 사용하지 않고 앞선 recognition module의 정확도를 최대로 올려 줄 생각이다. - 만약 잘 안된다면 앞선 detection 모듈에서 text box감지와 더불어서 어떤 유형인지도 동시에 예측하게 할 생각이다. 그런데 데이터 라벨링을 직접 해야 해서 현재는 데이터 전처리중.. 모델은 그냥 CTPN의 output feedforward layer에 classification head하나만 추가하면 되기 때문에 문제 없음.)
### 7
AWS S3를 사용할 예정이며, 현재 서비스 개발이 완료된 상태가 아니기 때문에 비용은 들지 않았음.
### 8
계획있음 - 현재 GPU 양은 충분하지만 RAM 메모리를 늘려주시면 좋겠습니다. (30GB는 너무 적어요)
### 11
변경사항 없습니다.
### 12
김영우, Toss, DevOps 엔지니어(새로운 멘토님으로 변경 예정)
# Team4. 고민박살
### 3
코로나 바이러스의 현황을 제공하고, 다음 세대의 돌연변이를 예측하는 서비스를 기획하였습니다. 이를 웹사이트로 제공하기 위해 먼저 코로나 확진자 수를 히트맵으로 나타내었고, 바이러스 서열을 다운로드해서 기간별로 돌연변이 추이를 분석하였습니다. 
### 4
1. Front-End: Javascript, html, css로 웹사이트 제작 (원래는 angular로 제작하려 하였으나 아직 기술 스택 완성
2. ClusterX(Multiple Sequence Alignment 작업-바이러스 서열 길이를 맞춰주는 프로그램), LSTM이용한 텍스트 생성
### 5
없습니다.
### 6
없습니다. 플랫폼 개발이 완료된 후 CV 기술 및 보안 기술을 사용할 예정입니다.
### 7
없습니다.
### 8
없습니다.
### 9
AWS 서버 이용에 10만원/month 정도 필요할 예정입니다.
### 10
relational DB를 바탕으로 한 웹 서비스 배포를 하려고 합니다. 이를 위해 전반적인 조언을 주실 멘토님이 필요합니다. 
### 11
변경: 졸업프로젝트 주제를 변경하였고, 멘토님을 변경할 예정입니다.

수정의 동기와 이유: 코로나 바이러스 염기 서열을 대상으로 MSA를 진행하여야 우세종 예측과 분석이 가능했다. 우리의 자원으로는 이를 처리하기에 역부족이었기 때문에 멘토님의 서버 자원을 통해 이를 해결하고자 하였다. 하지만 멘토님이 어느순간 연락이 되지 않으셨습니다. 그래서 저희가 이 상황에서 방대한 데이터를 처리할 수 있는 방법이 없었기 때문에 저희의 자원을 가지고도 처리할 수 있는 주제를 선정하게 되었습니다.

변경 전/후 어떻게 되는지: 바이러스 유전자 database를 기반으로 변이 바이러스 단백질 구조 예측 AI → 이화인의 취준/로스쿨진학/고시 정보 검색을 효율적으로 할 수 있는 플랫폼
### 12
멘토선정 도움필요
# Team5. TEAJAVA
### 3
여러 인공지능 모델을 탐색하기 위해서 K-Means Clustering, LSTM, TF-IDF의 cosine similarity 등 여러 모델과 기술들을 파이썬으로 돌려보는 작업을 진행했습니다. 또한 React-Native와 Firebase, Flask, AWS을 연동했습니다.
### 4
OS: 우분투
웹프레임웍: Python/Flask
데이터베이스: Firebase
프론트엔드: ReactNative(EXPO)
클라이언트: 웹앱(iOS + Android)
### 5
없다
### 6
Tensorflow: Transformer 모델로 챗봇을 만들 때 사용합니다. LSTM 모델로 사용자를 분류할 때 사용합니다.
### 7
AWS로 URL을 통해 외부에서 접속할 수 있도록 합니다. 현재까지 516원을 지출했습니다.
### 8
텐센트 GPU클라우드를 사용할 계획이 있습니다. 현재에는 4GiB 크기의 인스턴스를 사용하고 있습니다. 추후 GPU를 활용하여 모델 학습을 할 예정입니다.
### 12
하광림, (주)씨에스리 (스타트멘토 계속)
# Team6. VISTA
### 3
사용자 경험 향상을 위한 UXUI 분석 서비스'를 제작했습니다. 사용자가 디자인된 화면을 업로드하면, 해당 이미지 내의 UI 컴포넌트들을 인식하고, 각 컴포넌트별로 지켜야 할 UX 사항들을 체크리스트 형태로 보여줍니다.
### 4
1. Back-End: Java, Spring-boot
2. Database: mongoDB
3. Front-End: 웹 서비스 개발, TypeScript, React
### 5
Rico dataset (https://www.kaggle.com/datasets/onurgunes1993/rico-dataset) 을 이용하여 딥러닝 모델을 훈련합니다.
### 6
Tensorflow 를 사용합니다.
### 7
주로 Colab을 이용하여 개발을 진행했고, GPU 클라우드를 제공받았을 때에는 텐센트 클라우드를 이용했습니다.
### 8
사용할 계획이 있습니다. 저희가 이미지 기반의 프로젝트이기 때문에 최대한 많은 용량이 필요할 것 같습니다. (데이터셋만 해도 26기가를 차지합니다...!) 
### 11
없습니다
### 12
멘토선정 도움필요
# Team7.  COYD
### 3
스타트 학기에는 ‘성장 주기별 아이용 스마트 옷장 관리 및 중고거래 서비스’를 주제로 프로젝트를 진행하였습니다. 해당 프로젝트는 하루하루 발육 정도가 눈에 띄게 달라지는 아이(특히 영유아)의 옷을 관리하기 위해 출발하였습니다.
사용자는 아이의 옷 사진을 찍고, 해당 옷을 입었던 당시 아이의 신체 정보(키, 몸무게 등)를 입력합니다. 저희 서비스는 등록된 옷 사진으로 옷의 크기를 측정하고, 여기에 사용자가 입력한 옷의 부가 정보를  더하여 해당 옷의 정보를 저장합니다. 
추후에 아이가 더이상 옷을 입지 못하는 상황이 되면 사용자는 해당 옷을 중고거래에 등록할 수 있습니다. 저희 서비스에선 해당 옷에 대한 정보(입었던 당시 신체크기, 개월 수, 옷의 사이즈 등)를 가지고 있기 때문에, 사용자는 보다 쉽게 중고 거래에 의류 정보를 기입할 수 있습니다. 

스타트 최종 발표 이후, 주제 변경이 있었습니다. “블록체인을 활용한 중고 거래 기부 플랫폼”으로 주제를 변경하였습니다. 방학 기간 동안 해당 주제로 개발을 진행하였습니다.
### 4
웹 프레임워크는 백엔드 node.js/express, 프론트엔드 React, 데이터베이스 DB sqlite3, os 윈도우를 사용하였습니다.
웹 클라이언트를 만들었습니다.
현재 Polygon 네트워크 테스트 체인인 Mumbai에서 스마트 컨트랙트를 배포하여 개발 진행, 추후 메인 체인 배포 가능성 있음.
### 5
npm @ethersproject/providers
npm @openzeppelin-solidity
### 6
없습니다
### 7
아직 배포 전이라 해당 비용 발생하지 않았습니다.
### 8
없습니다
### 9
프로젝트 서버 비용을 지불할 계획이며, 현재 Heroku의 배포 서비스를 활용하여 한 달에 3만원 가량 생각하고 있습니다. 또한, 스마트 컨트랙트를 메인 체인에 배포하기 위해 블록체인 가스비를 만 원 내외로 지불할 계획 중입니다.
### 11
프로젝트 주제를 ‘블록체인을 활용한 중고거래 및 기부 플랫폼’으로 변경하고자 합니다. 
스타트 최종 발표에서 저희가 도출했던 문제를 적정기술로 해결할 수 없다는 지적을 받아 지난 방학 동안 고민해본 결과, 블록체인을 활용한 기부 플랫폼을 만들면 기존 문제인 기부처에 대한 불신을 해결할 수 있을 것 같아 주제를 변경하게 되었습니다. 
### 12
멘토선정 도움필요
# Team8. 어푸어푸
### 3
[영상 인식 기반 드론을 이용한 수상 안전 요원]

- yolov5를 이용하여 물에 빠진 사람 구분
- 깊이 추정을 이용하여 물에 빠진 사람의 위치를 받아와서 알림
- pid 제어를 이용하여 사각지대 없이 드론 운용 및 감시
### 4
1. Back-End : nest.js를 쓸 예정이고, os는 윈도우기반으로 할 예정입니다.
2. 데이베이스 : mysql을 쓸 예정입니다.
3. Front-End : 자바, 코틀린 사용합니다.
4. 클라이언트 : Android앱 만듭니다.
### 5
[https://www.anaconda.com/](https://www.anaconda.com/)

[https://nestjs.com/](https://nestjs.com/)

를 사용합니다.
### 6
Yolov5를 이용합니다. pyTorch를 이용하고, dji tello 라이브러리를 사용하고 있습니다.

그리고 opencv를 사용하고 있습니다.
### 7
사용하지 않고 있습니다.
### 8
300포인트 정도 필요할 것 같습니다.
### 9
텔로 에듀 드론 한 대가 필요합니다. 

[https://www.ryzerobotics.com/kr/tello-edu/specs](https://www.ryzerobotics.com/kr/tello-edu/specs) 162,000원, 드론을 직접 날려서 드론 배치를 검증하는데 쓸 예정입니다.
### 12
 오종훈 멘토님 / 클라우드네트웍스 소속 (스타트 멘토 계속) 예정하고 있습니다.
# Team9. L2K
### 3
- 스타트 당시에는 ‘객체 인식 아날로그 스캐너: 아날로그 데이터의 디지털화’를 주제로 해당 기술을 구현하는 데 있어서 핵심이 될 기술 3가지를 구현 및 검증하는데 집중
- Image 전처리(Tesseract를 이용한 Outline detection 및 영역 grouping), OCR을 이용한 Text 인식, python open CV를 이용한 개체 인식을 중심으로 기술 리서치
### 4
- 백엔드: python/django, mysql(또는 sqllite)
- 프론트엔드:  TypeScript, React, Javascipt, SASS
- 적응형 웹 구현
- 블록체인 티켓 거래 도입을 위한 Solidity 스마트 컨트랙트 작성
### 5
- iamport 결제 연동 : [https://api.iamport.kr/](https://api.iamport.kr/)
- nginx 웹 서버 연동
### 6
없습니다.
### 7
AWS를 통해 배포할 예정입니다.
### 8
없습니다.
### 11
- 변경: 현재의 주제(소규모 행사 인원 관리를 위한 스마트 티켓 플랫폼)로 변경
- 변경, 수정의 동기, 이유: 기존 ‘객체 인식 아날로그 스캐너: 아날로그 데이터의 디지털화’ 1. 개발된 앱이 사람들에게 정말 실용적일지, 2. 현 기술 수준에서 사람들이 실용적이라고 느낄 정도로 개발이 가능한지(현재 일반적인 ocr 인식률을 더욱 끌어올릴 심화 작업 필요) 등에 대한 의문 심화
- 변경 전 → 후: 따라서 기존 주제에서 현존 플랫폼에 비해 개선점이 명확한 현 주제로 변경
### 12
새로운 멘토를 컨택 중에 있습니다.
# Team10. 나는가수다
### 3
1. Figma를 이용한 UI/UX 개발 및 플로우차트 구성
2. ERD 작성을 포함한 데이터베이스 구조 설계
3. 아키텍처 설계도 작성
4. REST API 명세서 작성
5. DTRB(Deep Text Recognition Benchmark)와 CRNN을 이용한 OCR 모델 학습 및 EasyOCR fine tuning
6. Konlpy와 TF-IDF를 이용한 한국어 문장 유사도 계산 API 개발
### 4
1. Back-End: Springboot(Java) 프레임워크를 사용합니다.
2. DB: 데이터베이스로는 MariaDB를 사용합니다.
3. Front-End: React와 Typescript를 사용합니다.
4. 웹 앱을 개발합니다.
### 5
tesseract.js(사용 예정)
### 6
1. PyTorch를 기반으로 ClovaAI의 Deep Text Recognition Benchmark와 CRNN을 이용한 OCR 모델 학습을 진행하였습니다.(Deep Text Recognition Benchmark: [https://github.com/clovaai/deep-text-recognition-benchmark](https://github.com/clovaai/deep-text-recognition-benchmark), CRNN :  [https://github.com/mvoelk/ssd_detectors](https://github.com/mvoelk/ssd_detectors)  )

2. PyTorch를 기반으로 EasyOCR의 JaidedAI에서 배포한 korean_g2 모델을 이용하여 OCR 모델의 fine tuning을 진행하였습니다.(JaidedAI: [https://www.jaided.ai/easyocr/modelhub/](https://www.jaided.ai/easyocr/modelhub/))

3. Konlpy를 이용하여 tf-idf 기반의 한국어 문장 유사도 계산 API를 개발하였습니다.(Konlpy : [https://konlpy.org/ko/latest/index.html](https://konlpy.org/ko/latest/index.html) )
### 7
개발용 서버로서 Google Cloud Platform의 VM을 이용하고 있습니다. 크레딧을 사용하여 현재 지불된 금액은 없습니다.
서비스용 서버로서 AWS의 EC2를 이용할 계획입니다.
### 8
OCR 모델 학습을 위해 GPU 클라우드를 사용할 계획입니다. 방학 때 500포인트를 지원받았는데, 학습하기에는 충분하지 않아 가능하다면 이 이상을 지원받고 싶습니다.
### 11
변수명 혹은 파일명에서 영어를 사용하는 것이 편해 팀명을 변경하고 싶습니다.
팀명을 ‘나는가수다’에서 ‘GSD’로 변경하고 싶습니다.
### 12
멘토선정 도움필요
# Team11. JeongHyoYeon
### 3
발 사이즈 정밀 측정과 AI 스타일 추천 기능을 통해
온라인으로 내 스타일에 맞는 신발을 사이즈 고민 없이 구매하는 어플을 기획 및 개발하였습니다.
발사이즈 정밀 측정 기능 70% 개발, 사용자의 전신 사진을 AI로 분석해 신발을 추천해주는 기능 20% 개발, 앱 프론트엔드/백엔드 개발 50% 정도를 완료했습니다.

그러나 현재는 주제가 변경되었고
이와 관련해 23년 1월에 김규호 교수님과 미팅을 진행하였습니다.
### 4
1. 우분투, Python/Django
2. MySQL
3. React
4. 웹앱(모바일웹)
### 5
프론트엔드에서 사용한 모듈:
- react-redux
- redux

백엔드에서 사용한 모듈:
- djangorestframework
- djangorestframework-simplejwt
- django-corsheaders
- boto3
- PyMySql 
- gunicorn

개발이 진행됨에 따라 더 추가될 예정입니다
### 6
1. YOLOv5, pyTorch
URL : https://github.com/ultralytics/yolov5
용도 : 입력된 사진을 labeling 할 때 이용. 예를 들어, 풍경 앞에서 인물 사진을 찍었다면, '나무' '인물' label을 찾아서 앨범 폴더 분류 시 이용. 

2. MTCNN, TensorFlow
URL : https://github.com/ipazc/mtcnn
용도 : 인물 사진에서 face recognition을 통한 인물별 폴더 분류를 위한 모델
### 7
AWS의 EC2 - 서버로 사용
AWS의 RDS - 데이터베이스로 사용
AWS의 S3 - 이미지 저장 공간으로 활용 (데이터베이스에는 이미지 주소를 저장), react 파일 저장하기 위해서 사용
AWS의 Application Load Balancer, Route53 - https 배포를 위해 사용
AWS의 cloudfront 사용 - js의 정적 파일 배포하기 위해서 사용


현재까지 지출한 비용:
도메인 구입비 - 5.5$
서버 이용료 - 1.1$
### 8
사용할 계획 있으나, 어느정도 사용할지 아직 짐작하기 힘든 상황.
### 11
[1. 팀명 수정]
수정 전 팀명 : 풋(foot)마이스니커즈온
수정 후 팀명 : JeongHyoYeon
수정 이유 : 프로젝트 주제 변경

[2. 프로젝트명 수정]
수정 전 프로젝트명 : 슈팅(shoe-ting)
수정 후 프로젝트명 : AfterTrip
수정 이유 : 프로젝트 주제 변경

[3. 프로젝트 주제 수정]
수정 전 주제 : 슈팅(shoe-ting), 사이즈와 스타일 기반 신발 추천 및 구매 플랫폼
수정 후 주제 : AfterTrip, 딥러닝 얼굴 인식을 이용한 효율적인 그룹별 여행 관리 (사진 분류, 비용 정산)
* 주제 변경과 관련하여 1월 19일에 김규호 교수님과 대면미팅을 진행하였습니다.
### 12
멘토선정 도움필요
# Team12. 함꼐가자
### 3
스터디 전용 플랫폼의 부재로 인한 불편함을 줄이고자 스터디 관리 전용 웹 서비스를 개발했습니다. 코로나 이후 비대면 화상 회의 프로그램을 통한 스터디가 크게 늘었습니다. 스터디 활동을 하는 사람들의 스터디 관리의 번거로움을 줄여, 학습 활동에 집중할 수 있도록 하는 것이 목표입니다. 주요 기능으로는 화상회의, 채팅, 출석체크, 과제함, 일정관리 캘린더가 있습니다.
### 4
1. 윈도우, Node.js/Express 
2. mysql 
3. React js 
4. 웹
### 5
PeerJS: https://peerjs.com
Socket.io: https://socket.io
### 6
없습니다.
### 7
추후 AWS 서버 배포를 위해 30~40달러정도 예상합니다.
### 8
없습니다.
### 12
멘토선정 도움필요
# Team13. ,대함현즈
### 3
어두운 밤에 횡단보도를 건너는 보행자를 자동으로 인식하여 추적하며 조명을 비추어주는 조명 시스템을 만들고자 하였습니다
### 4
프론트는 flutter 프레임워크를 이용하여 android앱을 만들고자 하였고, spring boot 프레임워크를 이용하여 백엔드를 구현하고자 하였습니다. db는 mysql 이용하였습니다.
### 5
아두이노 서보모터와 레이저 모듈을 이용하여 전달 받은 객체의 정확한 위치에 레이저로 포인팅이 가능한지 확인하였습니다.
### 6
Yolo4에 coco dataset을 학습시켜 사람 객체를 인식하였습니다.
### 7
AWS
### 8
계획은 있으나 규모는 아직 모르겠습니다.
### 10
바뀐 주제가 캡스톤에 적합한지에 대한 조언을 구하고 싶습니다.
### 11
프로젝트 제목을 "SpotNight : AI와 야간 투시카메라를 이용한 야간 교통사고 방지 spotlighting 시스템"에서 "Liker: 보다 쉬운 중고 라이브 커머스"으로 변경합니다. 스타트 때의 주제는 하드웨어 구현이 복잡하고 하드웨어 구비 및 실현 가능성에 어려움이 있어 새로운 주제로 변경하고자 하였습니다.
### 12
스타트멘토 계속
# Team14. 고글
### 3
서비스 주제 확정 및 기획 구체화, 기술 리서치
음성 변환을 위한 오픈 소스 프로젝트 테스트하며 도메인 이해도 향상
팀원 목소리로 MaskCycleGAN, VITS-TTS 모델 트레이닝 및 테스트
제품 프로토타입 제작
### 4
딥러닝 - Flask, flask-restx

백엔드 - Ubuntu 18.04, Java/Springboot

데이터베이스 - MySQL

AWS - EC2, RDS, S3, CodeDeploy

프론트엔드 - Android Studio

안드로이드 어플리케이션 제작
### 5
https://github.com/xiph/rnnoise : 음성 노이즈 제거를 위한 node.js 모듈을 파이썬으로 사용
### 6
(https://github.com/yl4579/StarGANv2-VC)
StarGAN-VC : 사용자 음성으로 학습하여 음성을 변환하는 모델(Tensorflow)
(https://github.com/coqui-ai/TTS) 
Coqui TTS 중 VITS 모델: 영어(영국), 일본어 TTS 음성 생성(pyTorch)
(https://github.com/TensorSpeech/TensorFlowTTS)  
TensorFlow TTS 모델: 영어(미국), 중국어, 프랑스어, 독일어 음성 생성(Tensorflow)
### 7
AWS의 다양한 서비스를 이용중이며
클라우드 서버 EC2
데이터베이스 RDS
생성된 외국어 음성 파일 저장을 위한 S3 
자동 배포를 위한 CodeDeploy 사용 중입니다. 
### 8
GPU 클라우드 사용 계획입니다. 
### 10
스타트 멘토 확정 이후 주제 변경으로 인해 새로운 지도교수님 및 멘토님 선정이 필요한 상황입니다.
### 12
멘토선정 도움필요
# Team15. 조이룸(joyrOOOm)
### 3
오프라인 환경에서 안경을 구매하는 경우 시착할 때마다 안경사 혹은 매장 직원에게 문의해야 하는 불편함이 있습니다. 또한 시력이 매우 나쁜 경우 안경을 시착해보더라도 해당 안경의 렌즈에는 도수가 없기 때문에 착용한 모습을 정확하게 확인하기 어렵습니다. 대안으로 사진을 촬영하여 모습을 확인해본다고 해도, 자신의 시력에 따른 렌즈 굴절률이 반영된 모습을 확인할 수 없습니다.
이러한 문제점을 해결하고자 굴절률을 반영한 가상 안경 착용 기능을 제공하는 플랫폼을 만들었습니다. AR Core의 얼굴 인식(Face detection), 특징점 추출(Landmark detection), 얼굴 자세 추정(Head pose estimation) 등을 활용하여 가상 안경을 띄우고 비디오 인페이팅을 이용하여 사용자가 실제 착용중인 안경 알의 왜곡만을 제거하여 굴절률을 반영한 가상 안경 착용을 가능하게 하였습니다.
### 4
1. 우분투 OS
- AI 모델 서버 - Python 기반 FastAPI
- 데이터베이스 서버 - Java기반 Spring Boot & JPA
2. MySQL
3. Kotlin을 사용하여 Android Studio에서 Android 네이티브 개발
4. Android 앱을 만들고 있습니다. 

### 5
- 클라이언트: Android Standard Library, Glide, Material Design, OkHttp, Retrofit2, coroutine 사
용
- 데이터베이스 서버:  JPA, QueryDSL
### 6
- PyTorch 기반 Objecet Detection - Yolo v5
- PyTorch 기반 Semantic Segmentation
### 7
Google Cloud SQL, Google Storage Service : 사진 저장, 데이터베이스 배포, 구글 로그인 연동
### 8
사용 계획 있음. 딥러닝 모델 학습 시 GPU 필요
### 10
스타트 때의 프로젝트 주제와 다른 주제로 변경하고자하여 면담이 필요합니다.
저희가 스타트 때 개발했던 굴절률을 반영한 가상 안경 착용 플랫폼은 1. 실존하는 안경 이미지 및 모델의 저작권 문제가 있으며 2. 실제 구매로 이어져야 하는 플랫폼의 특성 상 캡스톤 프로젝트로써 개발 및 앱 출시에 어려움이 있을 것으로 판단하여 새로운 주제를 물색하게 되었습니다. 이에 새로운 주제를 구상하여 기획 및 초기 개발 단계에 있는데, 이와 관련하여 도움을 요청드리고자 합니다.
### 11
프로젝트 주제의 변경
원인: 상품 저작권과 관련해 앱 개발 및 앱 출시에 어려움이 있을 것이라고 예상하였습니다.
변경 전: 굴절률을 반영한 가상 안경 착용 플랫폼
변경 후: 노인들의 영양 섭취 불량 문제 해결을 위한 식단 관리 서비스
### 12
멘토 선정 도움필요
# Team16. ea9gu
### 3
개인정보에 대한 중요성을 바탕으로 sns에 업로드할 시 사진에 담긴 지문 정보를 마스킹할 수 있는 서비스를 만들고자 하였습니다. 손가락 인식, 지문 인식 인공지능 솔루션을 개발하여 성능을 더욱 높이는 과정에 있었으며, 스프링부트를 이용하여 서버를 제작하였습니다.
### 4
- OS: ubuntu (docker)
- Database: MySQL
- Web Framework: Spring Boot (JAVA)
- Front-End: Flutter
- iOS application 제작
### 5
없습니다.
### 6
Tensorflow, 손바닥에서 손가락을 찾고 어느 부분 손가락인지를 탐지하는 깃허브 오픈 소스 이용 후 fine-tuning 진행.
### 7
AWS - 배포, 호스팅
### 8
없습니다.
### 11
기존 주제에 관하여, sns 업로드 시 이루어지는 사진의 화질 저하가 발생하기 때문에 해당 서비스의 필요성에 대한 제고를 진행하였고, 해커들의 사진에서의 지문 인식 가능성에 대한 문제점이 발생하여 수정하게 되었습니다.

기존의 서비스는 활용성이 낮아 실생활에서 활용성이 높은 제품을 탐색하던 도중, 정확한 출석 체크가 진행되지 않아 발생하는 여러 갈등과 문제점들에 대해 인식하게 되었습니다. 

따라서, 저희는 주제를 “공간 주파수를 통한 출석 체크 앱”으로 변경하려고 합니다.
### 12
멘토 선정 도움 필요
# Team17. 메멘토
### 3
팀의 주제인 '판례 암기 어플리케이션'을 제작하기 위해 필요한 기능들을 정리하며 기획서를 작성했습니다. 어플리케이션의 사용 방법을 구체화하기 위해 와이어프레임과 프로토타입을 제작했으며, SENTENCE-KOBERT와 OCR 기술을 검증하는 시간을 가졌습니다.
### 4
1. Back-End로는 Java/Spring boot를 사용하고 있습니다.
2. 데이터베이스는 mysql을 메인으로 사용하며, 회원 토큰 저장에는 redis를 사용하고 있습니다.
3. Front-End에서는 Flutter를 사용하고 있습니다.
4. Flutter를 사용하여 크로스 플랫폼 앱을 만들고자 합니다. 다만 개발 환경은 Android 기기입니다.
### 5
네이버 OCR: https://www.ncloud.com/product/aiService/ocr
### 6
없다
### 7
네이버 OCR: 사용자의 노트에 있는 판결 요지를 추출하기 위해 사용함
### 8
없다
### 12
멘토선정 도움필요
# Team18. 우리는삼총사
### 3
딥러닝을 기반으로 편의점 CCTV를 분석하여 편의점 근로자에게 물리적 위협을 가하는 강력 범죄 행동을 감지하고 신고하는 종합 안전 서비스를 만들었습니다.
### 4
1. OS - Linux, Web - Java/SpringBoot
2. DB - Mysql
3. FE - ReactNative
4. Client - Android
5. Deep Learning Server - Python/Flask
### 5
없습니다.
### 6
pytorch

[https://github.com/carolchenyx/MGFN] (anomaly detection model)
[https://flask.palletsprojects.com/en/2.2.x/] (flask 이용)
### 7
AWS EC2 - 프로젝트 배포를 위해 사용하고 있습니다.
AWS RDS - 데이터베이스 구축을 위해 사용하고 있습니다.
### 8
텐센트 GPU 클라우드를 사용할 계획이 있습니다. 64GB정도 필요할 것 같습니다.
### 9
라즈베리파이 150000원 (용도: CCTV 영상 촬영 Simulation)
라즈베리파이 카메라 10000원 (용도: CCTV 영상 촬영 Simulation)
### 10
서비스 타깃의 변경(이전 주제로의 복귀)으로 면담이 필요합니다. (주제 변경: 범죄 취약 시설 대상 서비스→편의점 대상 서비스)
### 11
(주제 변동) **딥러닝을 기반으로 CCTV를 분석하여 범죄 취약 지역의 범죄행동을 감지하고 자동 신고하는 시스템→딥러닝 기반의 CCTV를 분석하여 편의점(상점) 내 범죄행동을 감지하고 자동 신고하는 서비스**

**사유: 서비스 대상의 구체화 및 기능의 명확성을 위하여 주제를 구체화하였습니다.**
### 12
고희원, SK텔레콤 (스타트멘토 계속)
# Team19. eLENS
### 3
스타트 첫 학기에 딥러닝 모델 학습과 자율주행 구현을 위한 하드웨어(Jetson Nano, LiDAR)를 마련하고 Jetson Nano의 구동을 위한 OS 환경 설정을 마쳤습니다.
PoseNet, PoseLSTM, AtLoc의 다양한 Camera pose estimation 모델을 기존 Bench mark 실내 dataset에 학습시켜 프로젝트에 적합한 모델을 탐색하였습니다.
아이폰 내장 라이다를 사용하여 실제 자율주행 구현을 위한 아산공학관 2층 데이터 셋을 생성하였습니다.
### 4
1. PoseNet 모델 구현 : Pytorch
2. 모델학습 : Colab 
3. Dataset : Google Cloud
4. Dataset 생성 : iphone 12 pro LiDAR (3d scanner app 사용)

딥러닝 모델의 경량화와 성능을 개선하는 연구트랙으로서, 논문 게재를 목표로 합니다.
### 5
Jetson Nano 2GB AI Developer Kit
### 6
PyTorch 기반으로 개발을 진행하며, 사전학습된 GoogleNet 모델을 BackBone으로 한 PoseNet 모델을 사용한다. 

- PoseNet (pytroch)
https://github.com/hazirbas/poselstm-pytorch](https://github.com/hazirbas/poselstm-pytorch
### 7
Colab Pro / 현재까지 지출 약 6만원
### 8
없습니다.
### 9
Colab Pro+, 월 49.99$, 용량이 큰 데이터셋에서 딥러닝 모델 학습
### 12
(멘토선정 도움필요) 현재 멘토로 모시고자 하는 분은 선정해 두었으나 아직 컨택은 하지 않은 상황입니다. https://deep-eye.tistory.com/37
# Team20. 다섯시삼십분
### 3
웹서비스 기획, 인공지능 모델을 통한 기술 검증(유사도 측정 및 본문 요약)
### 4
1. os : 윈도우, 웹프레임워크 : java/spring boot, ci/cd : 젠킨스
2. 데이터베이스 : mysql(maria DB), AWS S3 저장소 사용
3. front-end : React, Typescript
4. 클라이언트 : 웹
### 5
결제 모듈, 계좌실명조회 open api, 더치트 금융사기방지 api, 이더리움
### 6
없다
### 7
aws ec2/서버

aws s3/저장소(이미지 저장)

aws codeDeploy/CICD
### 8
없다
### 9
etherscan 거래 수수료/월 1만원/지갑 스캔

더치트 금융사기 방지 api 사용료/월 5만원/사기신고계좌 및 전화번호 확인
### 10
[주제변경] 주제 변경 승인을 위해 면담하고 싶습니다.

[비용지원] 프로젝트 진행 중 필요한 비용에 대해 지원받을 수 있을지 여부가 궁금합니다. 

[멘토] 블록체인 관련 현직자 멘토를 소개받을 수 있을지 여부가 궁금합니다.
### 11
주제를 변경하였습니다. 

변경 이유 : 자연어 처리를 통한 판례 분석에 한계를 느낌

변경 전 :  ‘PEOPLAW : 성범죄 피해자를 위한 BERT 모델 기반 유사 판례 분석 서비스’ 

변경 후 :  ‘고롱고롱 : 블록체인 기반 길고양이 개인 구조 모금 플랫폼’
### 12
(멘토선정 도움필요)
# Team21. 백조
### 3
전자책 텍스트 분석을 통해 분위기에 맞는 배경음악을 제공해주는 안드로이드 백그라운드 앱
### 4
1. 윈도우즈, python/flask
2. firebase (or mysql)
3. 안드로이드 스튜디오 Java 기반
4. android 어플 개발
### 5
백엔드 : flask, stream_with_context, response, request, json, firebase_admin
프론드엔드: 백그라운드에서 화면을 읽어오기 위한 MediaProjectionAPI : https://github.com/bictoselfdev/MediaProjectionEx
### 6
pytorch언어를 사용하여 인공지능 모델을 개발합니다.
-pretrained kobert nlp 모델을 사용하여 텍스트 다중감성분류를 수행합니다.
-직접 쌓은 cnn 모델을 사용하여 음악 다중감성분류를 수행합니다.
-ocr을 (TesseractAPI) 이용해서 스크린샷 텍스트 추출
### 7
구글의 firebase를 클라우드로 사용합니다. 무료로 사용하고 있습니다.
- storage: mp3 음악 파일을 저장하고 있습니다.
- realtime database : 음악의 메타데이터 json파일을 저장하고 있습니다.
### 8
없습니다
### 11
네.
### 12
멘토선정 도움필요
# Team22. 영시스터즈
### 3
사용자의 영어 발화를 분석하고 피드백을 주는 애플리케이션을 구상하였다. 
### 4
1. node.js/express 2. mysql 3. Swift, UIKit 4.iOS앱 5. 클라우드 - AWS EC2, S3
### 5
Alamofire (클라이언트에서 HTTP 통신 위해 사용, https://github.com/Alamofire/Alamofire)
### 6
tensorflow - nlp
### 7
AWS 사용 예정
EC2 - 서버 배포 위함
S3 - 사용자 음성 녹음 데이터 저장 위함
### 8
없다
### 11
없다.
### 12
멘토선정 도움필요
# Team23. 골투더퓨처
### 3
웹 기획 및 디자인
웹 프론트엔드 ui 구현
웹 백엔드 기능 구현
드론 적용을 위한 공 추적 알고리즘 작성
두 사람의 패스 수 카운트 구현 (경기분석)
### 4
1. OS - 윈도우즈, 웹 프레임웍 - java/spring
2. 데이터베이스 - mysql
3. 프론트엔드 프레임워크 - react
4. 웹
### 5
OpenCV
### 6
Yolov5(https://github.com/ultralytics/yolov5), 경기 분석 용도
deepsort(https://github.com/mikel-brostrom/yolov8_tracking), Yolov5와 함께 사용하여 경기 분석
### 7
텐센트 GPU 클라우드 사용 예정
### 8
사용 계획 있음, 웹 서버(동영상, 이미지, 서버) 용
### 9
축구공, 4만원, 드론 자동 추적 테스트용
### 12
스타트멘토 계속
# Team24. 캐릭캐릭뮤직체인지
### 3
입력된 미디파일을 로파이 스타일로 변경해주는 웹 사이트를 만드는 중
### 4
1. os -우분투, 웹프레임웍-python/flask
2. 데이터베이스는 사용하지 않음
3. 이용하지 않음
4. 웹
5. x
### 5
tonejs, magenta
### 6
groove2groove(https://github.com/cifkao/groove2groove.git)-음악 스타일 트랜스퍼, tensorflow
### 7
아직 정해지지 않음.
### 8
없음
### 12
스타트멘토 계속
# Team25. 밤낮박김
### 3
사용자가 웹(크롬)에서 글을 작성하면 그 입력값으로 가져와서 목적에 맞게( 맞춤법 교정, 단어 교체, 격식 전환) 자연어 처리 기술로 가공하여 실시간으로 피드백을 제공해주는 크롬 익스텐션 서비스 입니다. ( 한국판 grammarly )
### 4
1. 윈도우즈/ 웹프레임워크 자바스프링
2. mySQL
3. react (예정)
4. 웹 (크롬 익스텐션)
5. 자연어처리 딥러닝 모델
### 5
모델 서버:  fastAPI, uvicorn
### 6
pyTorch: NLP에 사용
RoBERTa: 문맥에 맞는 어휘 추천 및 검색
KoBART: 맞춤법 검사, 격식 문장 변환
### 7
아직 없으나 추후에 aws와 같은 클라우드 서비스를 이용할 예정입니다.
### 8
필요합니다. RoBERTa, KoBART 모델을 fineTuning할 정도면 될 것 같습니다.
### 12
멘토선정 도움필요
# Team26. yeahcherry
### 3
AI를 이용해서 IT 사이드 프로젝트의 팀원을 매칭해주는 웹서비스를 만들었습니다. 구체적으로는 데이터를 크롤링 후 KoBERT로 팀원 매칭 AI를 구현하려다가, 어려움이 있어서 기술을 바꿔 k-means clustering을 이용한 팀원 매칭 AI를 구현했고, 프론트엔드의 뼈대를 만들고 백엔드 공부를 했습니다.
### 4
1. Back-End : 우분투, Python/Flask
2. DB : mysql
3. Front-End : React
4. 클라이언트 : 웹
5. AI : 핵심기능인 팀원 매칭을 k-means clustering을 이용하여 구현
### 5
없습니다.
### 6
sklearn과 같은 기본적인 라이브러리만 사용합니다.
### 7
학교에서 지원해주는 tencent cloud, AI 구현을 위한 GPU 사용
### 8
있습니다.
### 10
AI 구현에 있어서 좀 더 효율적이고 정확도 높은 구현 방식을 여쭤보고 싶습니다. 다음주 중에 면담이 된다면 좋겠습니다.
### 11
프로젝트명 변경
수정 이유 : 기술 구현 중 NLP가 아닌 다른 기술을 이용하여 AI를 구현하게 됨
변경 전 : NLP를 이용한 IT 사이드프로젝트 팀원 매칭 서비스
변경 후 : AI를 이용한 IT 사이드프로젝트 팀원 매칭 웹서비스
### 12
스타트멘토 계속
### 13
강의실 자리가 바뀌었으면 좋겠습니다.
# Team27. ARchive
### 3
장소 기반의 증강현실 안드로이드 SNS 앱을 제작했습니다.

저희 앱의 슬로건 ‘지금, 여기’ 입니다.

모든 게시글은 현재 유저가 위치 장소에서 찍은 사진 혹은 동영상을 포함합니다. 그리고, 게시글이 올려질 때 유저가 있는 현재 위치에, 해당 게시글의 AR 썸네일이 남겨집니다.

앱을 켜면 자동으로 AR 카메라가 실행되고, 자신의 주변에 남겨진 게시글들의 썸네일이 AR 물체로 나타납니다. 각 게시글이 자신의 현재 위치로부터 어느 방향에 있고 어느 정도 거리에 있는지가 표시되기 때문에, 공간감을 느끼며 SNS를 즐길 수 있습니다.
### 4
AR 부분에 있어서는 안드로이드의 증강 현실 앱을 빌드할 수 있는 ARCore 플랫폼과 Unity Asset을 이용해서 개발 중입니다.

클라이언트 부분에서는 kotlin을 사용하여 안드로이드 앱을 개발 중입니다.

Back-end는 Java/Spring을 사용해 개발합니다. 개발에 사용 중인 OS는 윈도우즈입니다. 스프링부트를 사용한 RESTful API 서버를 구축한 뒤 안드로이드와 연동하여 개발합니다.
### 5
ARCore Geospatial API
https://developers.google.com/ar/develop/geospatial

Google Map API
https://developers.google.com/maps?hl=ko

Retrofit2 라이브러리
https://square.github.io/retrofit/

파이어베이스 DB
https://firebase.google.com/
### 6
없습니다.
### 7
구글 Cloud의 Maps SDK: 현재 본인의 위치와 포스팅의 위치 표시를 위한 지도 기능,
구글 Cloud의 ARCore for Android 서비스: AR 카메라에 AR 모델을 나타내기 위한 기능
### 8
없습니다.
### 9
유니티 에셋, 50달러, AR 카메라 화면에 표시할 객체
### 10
지도교수님을 변경하고 싶습니다. 스타트 중간발표 이전에 컴퓨터비전을 활용한 아이템을 계획했었어서, 인공지능 관련 교수님을 지도교수로 선정하였습니다. 그러나 중간발표 이후에 주제를 인공지능에서 AR로 변경했습니다. 따라서 AR 개발에 자문을 주실 교수님이 필요합니다.
### 12
서영수, BOTO (새로운 멘토에게 이메일로 컨택 시도 중. 컨택 실패 시 도움필요)
# Team28. 이김조
### 3
얼굴을 이용하여 아바타를 생성한 후, 해당 아바타와 함께 몰입하여 역사 AR 컨텐츠를 즐길 수 있도록 하는 AR 웹앱 기획 / 얼굴의 특징점을 잡는 모델을 이용하여 아바타를 만들 수 있는 코드 작성
### 4
1. OS : windows 
2. 데이터베이스 : mysql
3. 웹프레임웍 : Unity/WebGL
4. Front-End : Unity
5. 클라이언트 부분 : 웹앱
### 5
참고한 오픈소스 프로젝트 URL
https://github.com/Kwonkunkun/DrawAndPainting_VR
### 6
참고한 오픈소스 프로젝트 URL
1. 81개 facial landmark를 인식하는 모델. 얼굴(코,입,눈썹,입술,얼굴형)파츠를 선택하는것에 사용.
https://github.com/codeniko/shape_predictor_81_face_landmarks

2.얼굴형 분류한 논문. 이목구비의 비율을 구하는 수식을 참고하기 위해 활용함. 
https://www.researchgate.net/publication/362903132_Human_Face_Shape_Classification_with_Machine_Learning
### 7
AWS RDS : mysql 데이터베이스 생성용
AWS Lambda : Unity와 mysql 데이터베이스 연동을 위한 함수 작성용 
비용 지출 내역 없음
### 8
GPU클라우드 사용할 계획은 있으며, 대략적인 예상 사용량은 300~400포인트 사용할 것으로 예상됩니다. 
### 9
항목명 : google colab pro plus
추정가격 : 월 9.99$
용도 : AI 모델 학습 및 실행용
### 10
원래 계획은 특정 그림체로 스타일을 변환한 2D image를 3D object로 변환하는 방식을 이었으나, 기술적인 어려움을 느껴 닌텐도의 <Mii Studio>의 방식과 비슷하게 실제 얼굴과 사전 제작한 파츠의 비교를 통해 비슷한 외형의 아바타를 제작해주는 방식으로 변경하였습니다.
이에 대해서 기술적인 완성도가 떨어지는것이 아닌지 우려되어 해당 사항에 대해 면담을 요청드리고자 합니다.
### 12
멘토선정 도움필요
### 13
스타트때 사업자 등록을 했었는데, 해당 사업자등록증으로 사업자 등록 가산점을 받을 수 있을까요? 
아니면 새로운 업종으로 사업자 등록을 해야할까요?
# Team29. 나인틴
### 3
시선 추적과 표정 분석 기술을 활용한 유튜브 리뷰 플랫폼(Seetube)의 기획을 완료했습니다. Seetube는 유튜버가 리뷰를 의뢰한 영상들을 리뷰어들에게 제공, 리뷰 완료 시 리워드를 제공하여 리뷰 데이터를 수집합니다. 리뷰는 영상을 시청하고 있는 리뷰어의 시선 및 표정 데이터를 수집하는 방식으로 진행됩니다. 이후 해당 데이터를 사용하여 리뷰어들이 영상에서 집중한 장면과 감정을 느낀 장면을 선정하고, 이를 바탕으로 재편집된 2차 숏폼 컨텐츠(하이라이트 영상, 유튜브 Shorts)를 유튜버에게 제공합니다. 또한 유튜버들은 리뷰어들의 반응을 통해 향후 영상 콘텐츠의 구성 및 편집 방향에 도움을 제공받을 수 있습니다.
### 4
1. OS: ubuntu, 프레임워크: node.js/express
2. 데이터베이스: mysql
3. X
4. 클라이언트: iOS 네이티브 앱, 개발언어 - Swift
5. X
### 5
ffmpeg: 디지털 음성 스트림과 영상 스트림 편집 라이브러리. 시선과 표정데이터 분석 결과를 바탕으로 원본 영상을 편집하여 하이라이트/쇼츠 동영상을 제작하는데 필요.[https://github.com/FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)
pymysql: python에서 sql문법을 사용해 데이터베이스를 다루는 라이브러리.
### 6
SeeSo: 시선 추적 SDK, iOS 2.5.1 버전
MiniXception: 표정 분석 모델, [https://arxiv.org/abs/1710.07557](https://arxiv.org/abs/1710.07557)
YOLOv5: 동영상 내 객체 인식 용도
### 7
AWS EC2 인스턴스에 서버 구동중
$0.005 per Elastic IP address not attached to a running instance per hour (prorated) 항목으로USD 3.82 지출하였습니다.
### 8
있습니다. YOLO 구동을 위해서 필요합니다.
### 9
Apple Developer Program, $99, iOS의 경우 앱 배포(테스트배포 포함)를 하려면 개발자 계정이 필요합니다.
### 12
스타트멘토 계속
# Team30. 찐감자
### 3
주제 선정, 기술 선정, 웹사이트 구조 디자인(Figma), 웹사이트 기본 기능 구현, 데이터셋 구축, 딥러닝 모델 학습 (진행중)
### 4
1. OS - 윈도우즈, 웹프레임웍 - Python/django
2. dbSQLite
3. 사용하지 않음
4. 웹
### 5
없다
### 6
Tensorflow
### 7
AWS 사용 예정
### 8
사용할 계획이 있습니다.
### 11
없다.
### 12
멘토선정 도움필요
# Team31. 존버그
### 3
보행해충 탐지를 위한 인공지능 모델을 학습시켰습니다.
모바일 어플리케이션 개발을 위해 피그마로 디자인하였습니다.
백엔드 개발을 위해 Springboot 스터디를 진행하였습니다.
사용자가 사용할 수 있는 형태의 Android 어플리케이션 백엔드 API를 구현하였습니다.
### 4
1. 우분투, JAVA/SpringBoot
2. mysql
3. kotlin
4. Android 앱 개발
### 5
없음
### 6
Yolo v5
### 7
구글 클라우드 : 이미지 데이터 저장
AWS
- EC2 : 서버
- RDS : 관계형 데이터베이스 연결
### 8
없음
### 11
없음
### 12
멘토선정 도움필요
# Team32. 분노의추적
### 3
저희 팀은 BFP (Block Floating-Point)를 이용해 ray tracing 알고리즘의 최적화하는 연구를 진행하고 있습니다. 이 연구를 위해 스타트 첫 학기에 크게 두 가지의 결과물을 만들었습니다.

첫 번째는 BFP 연산을 지원하는 사칙연산 프로그램을 만들었습니다. 이 프로그램은 두 floating point를 연산하는 일반 사칙연산뿐만 아니라 BFP 연산을 소프트웨어적으로 구현합니다. 그러나 아직 에러가 존재하여 완성하지는 못한 상황입니다. 이번 그로쓰에서 에러들을 해결한 후 완성된 BFP 연산 프로그램을 이용해 BFP 연산이 ray tracing 알고리즘을 최적화하는지 그 여부를 실험해보고자 합니다.

두 번째 결과물은 ray tracing 알고리즘입니다. 저희 팀은 ray tracing 알고리즘을 자체적으로 구현하였으며, 다양한 알고리즘 중 BVH (Bounding Volume Hierarchy)를 활용하는 알고리즘을 택했습니다. 위에서 언급한 BFP 연산 프로그램을 저희가 구현한 ray tracing 알고리즘에 적용하여 실험을 진행할 계획입니다.
### 4
OS는 Linux를 사용하고 있으며 CUDA를 이용하여 GPU를 활용하고 있습니다
### 5
레이 트레이서 뼈대 (교재)
https://raytracing.github.io/


복잡한 3차원 물체(triangular mesh) 렌더링하기
https://github.com/mgaillard/Renderer
https://github.com/anandhotwani/obj_raytracer
### 6
없습니다. 
### 7
저희는 연구트랙이기 때문에 서비스를 위한 클라우드를 사용하지 않습니다. 
### 8
없습니다. 
### 12
멘토선정 도움필요
# Team33. 삼문철
### 3
첫학기 동안 딥러닝 모델을 간단한 데이터에 적용하여 적절한 방법임을 확인하였으며 간단한 웹서버를 제작하였습니다.
### 4
현재 ubuntu 서버에서 python flask 이용하여 웹 개발중이며 데이터베이스는 aws의 dynamodb를 이용하고 있습니다 또한 colab에서 딥러닝 모델을 이용해 첫학기 동안 간단한 video 식별이 가능하도록 구현했습니다
### 5
없습니다
### 6
tensorflow keras 이용하여 딥러닝 개발 중입니다
### 7
aws ec2 서버에서 개발 중입니다
aws dynamodb를 데이터베이스로 이용하고 있습니다
aws s3에 영상 저장을 하고 있습니다. 
### 8
없습니다
### 12
스타트멘토 계속
# Team34. 해오름시샘
### 3
opensource를 활용해 영상의 모션 일치도를 볼 수 있는 머신러닝을 이용해보았다. 이를 토대로 정확한 요가 동작이면 다음 동작으로 넘어가는 기능을 구현해보았다. 
### 4
1. 현재 Front 부분만 구현함. / 원도우 / python-django 사용 예정/
2. firebase, mysql 사용 예정
3.  안드로이드 스튜디오
4.  Android 앱을 만듦
### 5
https://github.com/mohit9949/Pose-Estimation-Similarity-With-TensorFlow
### 6
tensorflow lite 사용.
### 7
firebase의 firestore를 사용하여 요가 포즈 분별을 위한 데이터 셋을 올려놓음
### 8
사용할 가능성 있음. 머신러닝 모델 개발을 위해 사용할 계획 있음. 
### 12
스타트 멘토 계속 
# Team35. 김앤장
### 3
멘토님의 피드백을 바탕으로 서비스 기획과 뷰 디자인을 완료했고, 서버 개발을 끝냈습니다.
방학에는 프론트 뷰 개발(서버 연결 X)과 AI(GPT 사용) 개발을 진행했습니다.

* 뷰를 확인할 수 있는 피그마 링크 : https://www.figma.com/file/xr6PJfTGBkIaxClV0xpnSn/%EC%9A%B0%EB%A6%AC%EB%91%90%EB%A6%AC?node-id=53%3A121&t=lX7Z5XcuJTjbGevz-1
### 4
* Back-End : Typescript/Node.js, MySQL
* Front-End: Javascript/React Native
* 최종 산출물은 태블릿용 하이브리드 앱(iOS&Android 모두 호환)입니다.
### 5
* 사용 라이브러리 : https://github.com/react-native-voice/voice (STT 라이브러리)
* 사용 목적 : 동화 릴레이 제작 과정에 사용됨. 아이들의 말을 텍스트로 변환하여 GPT에 넘겨주는데 사용.
### 6
1. GPT-3(pyTorch) : 동화 릴레이 제작 과정에 사용됨. <우리두리>는 릴레이 소설처럼 한 문장씩 번갈아가며 동화를 만드는 방식의 서비스이기 때문에, 아이들이 말한 문장에 이어서 새로운 내용을 만드는데 사용. (현재 네이버 하이퍼클로바 이용중 - https://www.ncloud.com/product/aiService/clovaStudio)

2. Dall-e-2 : 동화 릴레이 제작 과정에 사용됨. 생성된 문장에 맞는 그림을 생성하는 AI 라이브러리. (https://openai.com/product/dall-e-2)
### 7
AWS - EC2, RDS, S3 사용중 (1년 무료티어 사용중으로 아직까지 과금 내역 없음.)
### 8
있음. GPT 관련 추가 개발을 위해 사용 예정.
### 9
네이버 하이퍼클로바 / Dall-e 이용 비용 (건당 비용 부과. 정확한 비용은 아직 예측할 수 없으나 최대 (넉넉잡아) 10만원을 넘기지 않을 것으로 추정.)
### 10
1. 멘토 선정 도움 필요
아래 멘토 질문에도 동일한 답변 남겨두었습니다. GPT 개발에 도움을 받을 수 있는 멘토를 구하려고 찾는 중입니다.

2. GPT 개발 관련 도움 필요
<우리두리>가 동화를 제작하는 서비스이다 보니 제작된 이야기를 관통하는 하나의 서사를 만들기 위해 고민하고 있습니다. 기존 GPT 기반 문장 제작 서비스(ex - 네이버 하이퍼클로바)의 API를 끌어와서 사용하는 방식이라 코드를 직접 수정할 수가 없어서(기업에 문의했으나 코드 공유는 어렵다는 답변을 받음.) 저희가 필요한 기능을 어떻게 추가해야 할지 방법을 고민중입니다.
### 11
변경사항 없음.
### 12
멘토선정 도움필요 / 우선 네이버 하이퍼클로바 AI 엔지니어분과 컨택중입니다.
# Team36. VRain
### 3
1️⃣ 가상현실 속에서, 3D 모델링한 도시(City)를 배경으로 3D 페인팅(Paint) 서비스
2️⃣ 증강현실 기술을 통해, 실제 도시(City)에 작품(Paint)을 띄워 관람하는 서비스
### 4
1. OS : ubuntu (AWS의 가상머신 이용)
2. Cloud : AWS 
3. DB : MySQL (AWS의 RDS 서비스 이용)
4. Frontend : Unity / Backend : python (AWS의 Lambda 이용)
5. Client : Android 어플리케이션 / VR 프로그램 (실행을 위해서는 오큘러스 퀘스트 VR 기기 필요)
### 5
1. Tilt Brush : VR 작품 그리기 (https://github.com/googlevr/tilt-brush)
2. Unity-Mapbox (WorldWide Scale) : 현실과 동일한 장소 구현
3. AsImpL : obj 파일을 유니티의 에셋으로 임포트 (https://github.com/gpvigano/AsImpL)
4. Aspose.3D : fbx를 obj 파일로 변환 ([Convert FBX to OBJ via Python | products.aspose.com](https://products.aspose.com/3d/python-net/conversion/fbx-to-obj/))
5. Vuforia : AR 카메라 기능 ([Home | Vuforia Developer Portal](https://developer.vuforia.com/))
### 6
없습니다.
### 7
1. 클라우드 : AWS
2. RDS : Mysql 기반 데이터베이스
3. S3 : 작품 파일, 이미지 저장하는 스토리지
4. Lambda + API gateway: API 기능 
5. 비용 : 무료 (AWS 프리티어 계정 사용 중)
### 8
없습니다.
### 9
없습니다.
### 10
가상현실 프로그램을 개발하고 있어서, 이 부분을 지도해주실 팀 지도교수님으로 변경하고 싶습니다.
### 11
네 알겠습니다.
### 12
멘토선정 도움필요
### 13
저희가 팀 지도교수님께 메일을 드려서 직접 변경하면 될까요?
Missing Teams:
38
39
