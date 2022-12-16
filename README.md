## [NICE DNB 최우수상 수상] 비재무 데이터를 활용한 중소기업 휴·폐업 예측
<img src="https://user-images.githubusercontent.com/109210030/208012088-96a640c9-cbe5-4b4a-a2ff-a03644205dd2.png" width="790" height="280"/>

## Technologies
![python3](https://img.shields.io/badge/python-3.10-blue)
![Crawling](https://img.shields.io/badge/Web-Crawling-important)

## Structure
* src
  * newsletter.py : 뉴스레터 컨텐츠를 만들고 HTML 문서를 작성하는 기능이 포함된 모듈
* template
  * tastyoffers.html : 뉴스레터 컨텐츠를 담는 HTML 파일
* utils
  * email.py : 뉴스레터 발송 기능이 포함된 모듈
* main.py : 모듈 실행 파일
```bash
project/
├── src/
│      └── newsletter.py
├── template/
│      └── tastyoffers.html
├── utils/
│      └── email.py
└── main.py
``` 
## Features
 - 검색어 및 출력 갯수(최대 100개) 변경 가능
 - 네이버 블로그 검색결과 최신순 정렬

## Example
> - Input - '서울 맛집'으로 네이버 블로그 4건 검색 (예시) 
>   - step 1 - 네이버 API를 통해 검색 대상 블로그 url 산출
>   - step 2 - 블로그 포스트 내 맛집 정보 Selenium 크롤링 & 광고성 이미지 OCR로 필터링 (---> 가짜 리뷰 n건 제외)
>   - step 3 - 포털에서 업체 별점 및 메뉴 Selenium 크롤링  
>   - step 4 - 비서울권 및 네이버 별점 4.0 미만 업체 제외
>   - step 5 - 뉴스레터 발송
> - Output - 뉴스레터 컨텐츠 
>   - 블로그 포스트명
>   - 포스트 내 첫번째 이미지
>   - 맛집 상호명
>   - 네이버 별점
>   - 주소
>   - 메뉴 
>   - 블로그 포스트 하이퍼링크 
> 



