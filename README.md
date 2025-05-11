# Content Data Crawler

주요 기업들의 온라인 콘텐츠를 수집하는 데이터 크롤러 프로젝트입니다.

## 기능

이 프로젝트는 다음과 같은 플랫폼에서 데이터를 수집합니다:

1. **네이버 블로그**
   - 네이버 블로그 검색 API를 사용하여 기업 관련 블로그 포스트 수집
   - 제목, URL, 요약, 작성일, 작성자 정보 포함

2. **네이버 뉴스**
   - 네이버 뉴스 검색 API를 사용하여 기업 관련 뉴스 기사 수집
   - 제목, URL, 요약, 작성일, 언론사 정보 포함

3. **유튜브**
   - YouTube Data API를 사용하여 기업 관련 동영상 수집
   - 제목, URL, 설명, 썸네일, 조회수, 좋아요 수, 댓글 수, 영상 길이 정보 포함

## 사용 방법

### 환경 설정

1. 필요한 패키지 설치:
```bash
pip install requests python-dotenv isodate
```

2. API 키 설정:
`.env` 파일을 생성하고 다음 API 키를 설정합니다:
```
NAVER_CLIENT_ID=your_naver_client_id
NAVER_CLIENT_SECRET=your_naver_client_secret
YOUTUBE_API_KEY=your_youtube_api_key
```

### 실행 방법

각 크롤러는 Jupyter Notebook으로 작성되어 있으며, 다음과 같이 실행할 수 있습니다:

1. 네이버 블로그 크롤러: `naver-blog-crawler.ipynb`
2. 네이버 뉴스 크롤러: `naver-news-crawler.ipynb`
3. 유튜브 크롤러: `youtube-crawler.ipynb`

## 데이터 저장

수집된 데이터는 `data` 디렉토리에 JSON 형식으로 저장됩니다:
- `naver_blog_results.json`
- `naver_news_results.json`
- `youtube_search_results.json`

## 주의사항

- API 사용량 제한을 고려하여 요청 간 1초의 간격을 두고 있습니다.
- API 키는 반드시 안전하게 보관하고, 공개 저장소에 업로드하지 않도록 주의하세요.