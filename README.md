# 소셜 미디어 통합 Feed 서비스
![bgimg](https://drive.google.com/uc?export=view&id=1FPwKX0OXlH0NaelkLNx1JYn764DUZpFr)
## 팀 소개
<div align="center">

| <img src="https://drive.google.com/uc?export=view&id=1zV9DywkNWbgT5dJIuMNNHMfft0GnkoDU" width="140" height="140"> | <img src="https://drive.google.com/uc?export=view&id=1xZq17TkXxbKIMou_1N8HI5jJ1hGuKmD4" width="140" height="140"> | <img src="https://drive.google.com/uc?export=view&id=1W6rZe96xwdXJeNULFtXOm8Iip6tzN0B6" width="140" height="140"> | <img src="https://drive.google.com/uc?export=view&id=1fBa0aPyXRkrijdG6o3RQcj5ahm_dSktb" width="140" height="140"> |  
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|  
| Back-End                                                                                                   | Back-End                                                                                                        | Back-End                                                                                                                                  | Back-End                                                                                                        |                                                                                                 |
| [이준규](https://github.com/junkyu92)                                                                         | [이현정](https://github.com/12hyeon)                                                                               | [최승호](https://github.com/madst0614)                                                                                                    | [조현수](https://github.com/HyunsooZo)                                                                            |

</div>

## 목차
- [개요](#개요)
- [사용기술](#사용기술)
- [API 문서](#API-문서)
- [구현 기능](#구현기능)
- [시스템 구성도](#시스템-구성도)
- [ERD](#ERD)
- [TIL 및 회고](#프로젝트-관리-및-회고
  )


## 개요

본 서비스는 유저 계정의 해시태그(`#kim_wanted`) 를 기반으로 `Instagram`, `Thread`, `Facebook`, `Twitter`등 <br>
복수의 SNS에 게시된 게시물 중 유저의 해시태그가 포함된 게시물들을 하나의 서비스에서 확인할 수 있는  <br>
통합 Feed 어플리케이션 입니다. 이를 통해 본 서비스의 고객은 하나의 채널로 유저(`#kim_wanted`) <br>
또는 브랜드(`#nike`) 의 SNS 노출 게시물 및 통계를 확인할 수 있습니다.
<br/>


## 프로젝트 관리 및 회고
[![Notion](https://img.shields.io/badge/Notion_문서로_확인하기_(클릭!)-%23000000.svg?style=for-the-badge&logo=notion&logoColor=white)](https://www.notion.so/75c5a817b6b24a98850ff8ca17a8f929?v=8562a6e059c64b7a86d03497f5012cb3&pvs=4)


## 사용기술

#### 개발환경
<img src="https://img.shields.io/badge/java-007396?&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/spring-6DB33F?&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/Spring boot-6DB33F?&logo=Spring boot&logoColor=white"> <img src="https://img.shields.io/badge/gradle-02303A?&logo=gradle&logoColor=white">
<br>
<img src="https://img.shields.io/badge/MariaDB-003545?&logo=mariaDB&logoColor=white"> <img src="https://img.shields.io/badge/redis-DC382D?&logo=redis&logoColor=white"> <img src="https://img.shields.io/badge/Spring JPA-6DB33F?&logo=Spring JPA&logoColor=white"> <img src="https://img.shields.io/badge/querydsl-2599ED?&logo=querydsl&logoColor=white">  <img src="https://img.shields.io/badge/SMTP-CC0000?&logo=Gmail&logoColor=white">
<br>
<img src="https://img.shields.io/badge/AssertJ-25A162?&logo=AssertJ&logoColor=white"> <img src="https://img.shields.io/badge/Mockito-008D62?&logo=Mockito&logoColor=white">
<br>
<img src="https://img.shields.io/badge/intellijidea-000000?&logo=intellijidea&logoColor=white"> <img src="https://img.shields.io/badge/postman-FF6C37?&logo=postman&logoColor=white"> <img src="https://img.shields.io/badge/swagger-85EA2D?&logo=swagger&logoColor=white">

#### 배포환경
<image src="https://img.shields.io/badge/Docker-2496ED?&logo=Docker&logoColor=white"><img src="https://img.shields.io/badge/aws-232F3E?&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/ec2-FF9900?&logo=amazonec2&logoColor=white"> <img src="https://img.shields.io/badge/rds-527FFF?&logo=amazonrds&logoColor=white"> <img src="https://img.shields.io/badge/ElasticCache-201d90?&logo=amazonelasticcache&logoColor=white" alt="actions">
<br>
<img src="https://img.shields.io/badge/github-181717?&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/Jenkins-2088FF?&logo=Jenkins&logoColor=white" alt="actions">

#### 협업도구
<img src="https://img.shields.io/badge/discord-4A154B?&logo=discord&logoColor=white"> <img src="https://img.shields.io/badge/notion-000000?&logo=notion&logoColor=white">
<br/>

## API 문서
[![Swagger](https://img.shields.io/badge/swagger_문서로_확인하기_(클릭!)-85EA2D?&logo=swagger&logoColor=white)](http://54.225.40.161:8090/swagger-ui/index.html#/)


| API Type | Http Method| URL                         | Description    |
|----------|-------------|-----------------------------|----------------|
| **Auth API** | POST | `/api/v1/auth/refresh`                   | 엑세스토큰 재발급      | 
| **User API**| POST | `/api/v1/users/sign-up`                  | 회원가입           |
| **User API**| PATCH | `/api/v1/users/verification`             | 회원가입 인증        |
| **User API**| POST | `/api/v1/users/verification/otp-reissue` | OTP 재발급        |
| **User API**| POST | `/api/v1/users/sign-in`                  | 로그인            |
| **User API**| PATCH | `/api/v1/users/password/modify`          | 비밀번호 변경        |
| **User API**| PATCH | `/api/v1/users/password/reset`           | 비밀번호 재설정       |
| **User API**| POST | `/api/v1/users/sign-out`                 | 로그아웃           |
| **Posting API**| GET | `/api/v1/postings`                       | 조건 검색          |
| **Posting API**| GET | `/api/v1/postings/{id}`                  | 포스팅 상세 가져오기    |
| **Posting API**| PATCH | `/api/v1/postings/like/{id}`             | 포스팅 좋아요        |
| **Posting API**| PATCH | `/api/v1/postings/share/{id}`            | 포스팅 공유         |
| **Log API**| GET | `/api/v1/logs/hashtags`                  | hot hashtag 조회 |


## 구현기능

<details>
  <summary>검색 빈도가 높은 Tag 데이터 저장 기능</summary>

- **구현 기능**<br>
    - 주기적으로 검색에 사용하는 Tag 데이터를 저장하는 기능을 구현했습니다.

- **구현 방법**<br>
    - 스프링 스케줄링 기능을 사용하여 @Scheduled 어노테이션을 이용해 주기적으로 메서드를 실행합니다.
        - saveScheduledTag() 메서드: 매 시간마다 실행되며, 최근 3시간 동안의 빈도 높은 태그를 저장합니다.
</details>
<details>
  <summary>단기간 조회수 급상승 알림 기능</summary>

- **구현 기능**<br>
    - 주기적으로 상세검색에 사용하는 postingId 데이터를 저장하는 기능을 구현했습니다.

- **구현 방법**<br>
    - 스프링 스케줄링 기능을 사용하여 @Scheduled 어노테이션을 이용해 주기적으로 메서드를 실행합니다.
        - checkOnFire() 메서드: 매 12시간마다 실행되며, 단기간에 급상승한 게시물을 확인하고 알림을 보냅니다.
    - 단기간 조회수에 대한 조건을 추가로 설정했습니다.
        - 조건 1) 12시간 동안 100번 이상 조회한 경우
        - 조건 2) 12시간 동안 전체의 50% 보다 많은 경우 (생성된지 3시간 이상인 posting 조건이 포함)
        - 조건 3) preView 높은 순으로 최대 10개

</details>


## 시스템 구성도
![시스템 구성도](https://drive.google.com/uc?export=view&id=1k0sQtQ5S5BhZoroljc43S4tmxW5yyacz)

## ERD
![ERD](https://github.com/12hyeon/sns-feed/assets/67951802/535758ec-8342-4ae0-ba2c-7a218261ecfd)




