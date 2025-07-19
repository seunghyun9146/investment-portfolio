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

폴더구조
news_crawler_project/
├── data/
│   └── naver_news.csv       # 저장된 뉴스 데이터
├── main.py                  # 실행 파일 (위의 코드)
├── README.md

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








