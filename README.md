# investment-portfolio
웹 크롤링 기술을 이용한 포트폴리오 py
<img width="1567" height="871" alt="image" src="https://github.com/user-attachments/assets/94080e7a-b137-4e81-ad6d-ea06494ad82c" />

주요 기능
네이버 경제 뉴스(https://news.naver.com/section/101) 최신 100건 수집


뉴스 제목·본문·링크를 CSV 파일로 저장
PyQt5 기반 GUI 뉴스 탐색기
키워드 검색 기능
선택한 뉴스 본문을 KoBART 모델로 요약
클릭 시 웹 브라우저에서 기사 원문 열기

사용 기술
Python
BeautifulSoup - 웹 크롤링
transformers (KoBART)
PyQt5 - GUI 구현

설치방법
# 가상환경 권장
pip install -r requirements.txt

필요라이브러리
PyQt5
transformers
torch
requests
beautifulsoup4

pip install PyQt5 transformers torch requests beautifulsoup4
 Transformers 모델 digit82/kobart-summarization은 최초 실행 시 다운로드됩니다.

실행방법
 실행 후 GUI 창이 뜨면 🔄 뉴스 불러오기 버튼 클릭 → 최신 뉴스 수집 및 화면 표시
뉴스 클릭 → 본문 확인
📑 요약하기 → BART 모델 기반 요약

요약모델
모델명: digit82/kobart-summarization
기반: SKT KoBART + 한국어 뉴스 데이터로 파인튜닝
최대 토큰: 1024개, 요약 길이 제한 있음 (150 tokens)

[향후목표]
#머신러닝 기반 확장 목표
1. 뉴스 기반 주가 예측 모델 개발
수집한 경제 뉴스를 바탕으로 관련 주가의 등락을 예측하는 머신러닝 모델(XGBoost, LSTM 등) 실험

2. 뉴스 중요도 자동 분류
수집한 뉴스의 영향력(예: 주가에 미치는 영향, 댓글 수, 트렌드 반영 등)에 따라 중요도 레벨을 자동 분류하는 모델 개발

3. 뉴스 감성 분석 모델 적용
KoNLPy, SOYNLP, HuggingFace 기반 감성 분석 모델을 적용해 뉴스 감정(긍정/부정/중립) 자동 라벨링

4. 클러스터링 기반 뉴스 그룹화
TF-IDF, Word2Vec, BERT 임베딩 기반으로 유사한 뉴스끼리 군집화 (KMeans, DBSCAN 등 사용)

5. 사용자 관심사 기반 추천 시스템 구축
사용자의 검색 기록, 클릭 기록, 키워드 기반으로 관심 있는 뉴스만 골라주는 추천 기능 (콘텐츠 기반 필터링 또는 협업 필터링 방식)

6. 요약 모델 커스터마이징(Fine-tuning)
수집된 뉴스 데이터로 KoBART 모델을 파인튜닝하여 나만의 도메인 특화 요약 모델 제작

7. 이상 탐지(Anomaly Detection)
특정 시점에 갑자기 쏟아지는 특정 키워드/뉴스를 감지하여 ‘이슈 알림’ 제공

8. 요약 품질 자동 평가
ROUGE 스코어 계산, 사용자 피드백 수집 등으로 요약 품질을 머신러닝으로 평가/개선





