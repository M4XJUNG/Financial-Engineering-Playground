# Financial-Engineering-Playground
Code Repository for Financial Engineering. Implements models from Hands-on ML, Python for Finance, and research papers.

---

## 📚 Project Directory (Study List)

이 저장소에 포함된 학습 프로젝트 및 폴더별 상세 설명입니다.

| 폴더명 (Folder) | 설명 (Description) | 비고 (Source) |
| :--- | :--- | :--- |
| **deep-learning-pytorch-textbook** | 파이토치(PyTorch) 기반 딥러닝 모델 구현 | [《딥러닝 파이토치 교과서》](https://wikidocs.net/book/2788) |
| **doit-pandas** | 판다스 활용 데이터 전처리 및 시각화 | [《Do it! 판다스 입문》](https://github.com/easysIT/doit_pandas) |
| **financial-data-science-practice** | 금융 공학 데이터 실무 테크닉 | 금융 공학 데이터 사이언스 실습 |
| **intro-to-ml-with-python** | 지도/비지도 학습 및 특성 공학 기초 | 《파이썬 라이브러리를 활용한 머신러닝》 |
| **python-machine-learning-perfect-guide** | 머신러닝 핵심 알고리즘 및 사이킷런 | 《파이썬 머신러닝 완벽 가이드》 |
| **quant-investment-portfolio-python** | 퀀트 투자 전략 및 포트폴리오 최적화 | 《파이썬 퀀트 투자 포트폴리오》 |
| **release-your-product-with-fastapi** | FastAPI 활용 웹 서비스 배포 및 API 구축 | 《FastAPI 개발 백서》 |
| **self-study-ml-dl** | 머신러닝/딥러닝 입문 및 기초 예제 | 《혼자 공부하는 머신러닝+딥러닝》 |
| **statistics-with-python-textbook** | 파이썬 활용 통계 분석 및 검정 | 《파이썬으로 배우는 통계학 교과서》 |
| **understanding-financial-ai** | 금융 데이터 분석 및 AI 모델링 기초 | 《금융 AI의 이해》 |

---

## 🚀 How to Run & Edit with Google Colab

이 저장소의 Jupyter Notebook(`.ipynb`) 파일들을 Google Colab에서 바로 실행하고 수정하는 방법입니다.

### 1. 노트북 열기 (Open in Colab)
원하는 파일을 열람하는 두 가지 방법이 있습니다.

* **방법 A (추천):** 아래 링크 형식을 사용하여 브라우저 주소창에 입력합니다.
  > `https://colab.research.google.com/github/M4XJUNG/Financial-Engineering-Playground/blob/main/[파일경로]`
* **방법 B:** [Google Colab](https://colab.research.google.com/) 접속 → `File` > `Open notebook` → `GitHub` 탭 선택 → 이 저장소 주소 붙여넣기.

### 2. 수정한 내용 저장하기 (Save Changes)
Colab에서 수정하거나 주석을 단 내용을 다시 GitHub 저장소에 반영하려면 다음 단계를 따르세요.

1. 상단 메뉴의 **[파일(File)]** 클릭
2. **[GitHub에 사본 저장(Save a copy in GitHub)]** 선택
3. 해당 저장소와 브라우저 인증 진행
4. 커밋 메시지를 작성하고 확인 클릭

> **⚠️ 주의사항:** 데이터를 불러올 때는 GitHub의 `blob` 주소가 아닌 `raw` 주소를 사용해야 판다스(`pd.read_csv`)에서 오류가 발생하지 않습니다.

---

## 📂 Repository Management (How to Merge)

이 저장소는 흩어져 있던 여러 학습 프로젝트를 하나로 통합하여 관리하기 위해 생성되었습니다.  
기존 리포지토리의 파일 구조를 가져오되, 커밋 기록 충돌을 방지하기 위해 다음과 같은 Git 명령어를 사용하여 병합했습니다.

### 🛠️ 통합 과정 (Git Workflow)

각 주제별 리포지토리를 폴더 단위로 깔끔하게 가져오기 위해 사용한 명령어 모음입니다.

```bash
# 1. 원하는 리포지토리를 특정 폴더명(예: python-study)으로 복제(Clone)합니다.
# 형식: git clone [가져올_주소] [내가_원하는_폴더명]
git clone [https://github.com/example/repo-url.git](https://github.com/example/repo-url.git) python-study

# 2. 가져온 폴더 안의 .git 폴더(과거 기록)를 삭제합니다.
# (이 과정을 거쳐야 서브모듈 오류 없이 내 리포지토리의 일부로 완전히 합쳐집니다.)
rm -rf python-study/.git

# 3. 위 과정을 필요한 만큼 반복한 뒤, 변경 사항을 스테이징 영역에 올립니다.
git add .

# 4. 통합된 내용을 커밋 메시지와 함께 저장합니다.
git commit -m "Feat: Merge external study repositories"

# 5. 원격 저장소(GitHub)로 업로드합니다.
# (대용량 파일이 있을 경우 LFS 업로드 시간이 소요될 수 있습니다.)
git push origin main
