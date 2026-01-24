# 국방일보 데이터 분석: 적금 vs 주식 (Savings vs Stocks)

## 프로젝트 개요 (Project Overview)
최근 병사 월급 인상에 따른 국방일보 기사 데이터 분석을 통해, 적금과 주식에 대한 시각 차이를 알아보기 위해 텍스트 마이닝 기법 사용

## 사용 기술 (Tech Stack)
- **Language:** Python 3.9
- **Crawling:** Selenium, BeautifulSoup
- **Analysis:** Pandas, KoNLPy (형태소 분석)
- **Visualization:** Matplotlib, WordCloud

## 트러블 슈팅 (Troubleshooting & Issues)
프로젝트 진행 중 겪었던 기술적 문제와 해결 과정입니다.

### 1. 국방일보 사이트 크롤링 접속 불가 (Connection Timeout)
- **현상:** Google Colab 환경에서 `requests` 및 `Selenium`으로 크롤링 시도 시 지속적인 연결 실패 발생.
- **원인 분석:** - Google Colab 서버의 위치는 미국(US)임.
    - 국방일보 웹사이트는 보안상 해외 IP 대역의 접속을 차단(Geo-blocking)하고 있음을 확인.
- **해결 방안:**
    1. **로컬 실행:** 한국 IP를 사용하는 로컬 PC 환경에서는 정상 작동할 가능성
    2. **가상 데이터 활용:** Colab 환경에서의 분석 실습 및 로직 검증을 위해, 실제 기사 패턴을 반영한 가상 데이터 생성 모듈을 구현하여 분석 프로세스 완성하는 방법.
