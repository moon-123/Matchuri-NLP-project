# 🔮 추리추리 마추리
##### 추리 수수께끼 게임 챗봇
###### 인원: 5명
###### 기간: 2024-01-12 ~ 2024-02-20
-----------------
## 💡 프로젝트 기획
평소에 심심할때 할게없을때 쉽게 할 수 있는 어플을 만들고 싶다는 생각이 들어 인터넷을 찾아보다가 수수께끼 문제들을 찾았습니다. 그래서 마추리팀은 단순 대화만 할 수 있는 챗봇이 아닌 수수께끼 게임을 만들어 문제를 스테이지 형식으로 구성하고 질문하면 해당 질문에 맞는 답변을 사용자에게 전달하고, 힌트 및 정답등을 버튼형식으로 구현하여 사용자가 더욱 쉽고 편하게 게임을 즐길 수 있도록 챗봇을 제작하였습니다.

<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/42333bc2-720b-4fd7-a9eb-24ca94407f7b">

<hr>

# **마추리란?**
사람과 챗봇이 수수께끼 문제를 같이 풀어가는 게임형식의 챗봇으로 유저(브리튼) 챗봇(마추리)로 구성되어있다.
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/ab7bc253-1d86-4c44-93dd-0a10c2a97be8">


## 👨‍💻 Process & Role
#### Overall Process
###### - 기획, 서버구현, 프론트구현, 모델학습, 서버배포, PPT제작, 발표, 데이터수집
#### 😺 My Role
###### - 기획, 모델학습, 서버배포, PPT제작, 데이더수집

## 🌏 Dataset & Model
#### Dataset
- 문제별로 [질문과 답변 데이터](https://github.com/moon-123/Matchuri-NLP-project/files/14344362/QADataset.xlsx)를 직접 작성함
- 모델 학습에 사용한 문제는 총 6개로 2289개의 질문-답 데이터셋 사용

#### Model
- 문장 학습 모델 [skt/kogpt2-base-v2](https://github.com/SKT-AI/KoGPT2)
- 유사도 측정 모델 [ddobokki/klue-roberta-base-nli-sts](https://huggingface.co/ddobokki/klue-roberta-base-nli-sts)
-----------------
## 🚀 Result

### **발표ppt**
[추리추리 마추리 ppt](https://github.com/moon-123/Matchuri-NLP-project/blob/master/%EB%A7%88%EC%B6%94%EB%A6%AC_%EB%B0%9C%ED%91%9C.pdf)


### **프론트**
- 제작 화면1
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/af677f1e-91d0-4911-8816-4e538b9f7586">

- 제작 화면2
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/b52c12a0-405b-45d5-aebd-26d8098c9680">

### **서버**
확장성을 위해 node, python 두가지 서버를 같이 사용 채팅부분을 제외한 나머지 부분은 전무 node.js로 서버를 작업하였고 모델과 소통해야하는 채팅 부분은 python 서버로 작업하였습니다.

<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/4c1845bd-7159-4aad-a4b1-ba270697df4a">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/1be4e00c-1e1e-4fe7-b8d6-42386b16e299">


### **모델**
유저가 질문을 입력하면 RoBerta로 유사성을 검사하고 문제와 유저가 입력한 질문이 유사하다고 판단되면 GPT2 모델에 넣어 학습한 질문과 대조하여 학습된 답변을 그래도 출력하거나 GPT2가 생성한 답변을 출력되게 모델을 학습시켰습니다.

<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/27bc7216-eef5-4dcf-83fc-b3628cf8820e">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/2a346441-d1fb-4f59-9522-f44a0c607c01">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/565fdd90-5315-4be3-b655-5bf0e4bef5f3">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/89b0869c-6248-44e5-b8ac-cc4dd67f2aba">


- **전처리 과정**
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/a56a6b98-1fdd-49ee-85ee-5961e01dc94c">

- **GPT2**
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/9af42433-7b85-4c66-ae30-05c247cfab4b">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/6bd35102-c87d-4015-b57d-6b080c115bb1">
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/0fdc68a8-955c-4b8e-8bc9-e78da9c06d48">

- **최종모델**
<img width="100%" alt="image" src="https://github.com/moon-123/Matchuri-NLP-project/assets/59769304/44533e07-2bca-4678-8283-b9fb9e629ac2">



-----------------
### ⚙️ Skills & Tools

<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/JavaScript-gray?style=flat&logo=JavaScript&logoColor=F7DF1E"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=4479A1"/>&nbsp;&nbsp;
</p>

<p>
  <img src="https://img.shields.io/badge/Colab-F37626?style=flat&logo=googlecolab&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/VScode-007ACC?style=flat&logo=visualstudiocode&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/Discord-5865F2?style=flat&logo=Discord&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/AWSEC2-FF9900?style=flat&logo=amazonec2&logoColor=white"/>&nbsp;&nbsp;
  <img src="https://img.shields.io/badge/AWSS3-569A31?style=flat&logo=amazons3&logoColor=white"/>&nbsp;&nbsp;

  
</p>
