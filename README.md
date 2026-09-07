<!-- ======================== 헤더 배너 ======================== -->
<div align="center">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=220&section=header&text=tomatosugarpickled&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Backend%20Developer%20Portfolio&descAlignY=60&descSize=18" />

</div>

## 회원·인증 도메인을 구현하는 백엔드 개발자 홍성호입니다.

Java와 Spring Boot로 회원가입·로그인, 마이페이지, 계정 설정 API를 구현했습니다.
Global Gates에서는 JWT·OAuth2 인증과 Redis 토큰 처리, Spring–FastAPI 연동을 담당하고, 인증 객체와 계정 상태 전이에서 발생한 오류를 추적해 수정했습니다.

[포트폴리오](https://app.notion.com/p/Backend-Portfolio-36fc7b94f5a68109addce43ce4352408) · [기술 블로그](https://velog.io/@tjdgh1851/posts) · [이메일](mailto:tjdgh1851@gmail.com)

## 대표 프로젝트

### Global Gates
중소기업과 해외 바이어를 연결하는 무역 B2B SNS 팀 프로젝트입니다.

- **담당:** 회원·인증, 마이페이지·설정 백엔드, Spring–FastAPI 연동, 뉴스 자동화와 배포
- **문제 해결:** 로그인 식별값 누락, 계정 비활성화 직후 로그아웃 실패, 회원 정보 수정 시 캐시 처리
- **기술:** Java 17, Spring Boot, Spring Security, MyBatis, PostgreSQL, Redis

[백엔드 코드와 기여 안내](https://github.com/tomatosugarpickled/globalgates-back) · [배포 저장소](https://github.com/CI-CD-globalgates/CI-CD-globalgates) · [상세 포트폴리오](https://app.notion.com/399c7b94f5a6812aa6dcec7f535538be)

### Commit & Merge
팀·파트너 매칭과 펀딩을 연결하는 플랫폼의 팀 프로젝트입니다.

- **담당:** 일반 회원 로그인·회원가입, 마이페이지 경력·학력·활동 내역, 게시물·팔로워·프로필 기능
- **구현 경험:** Spring MVC와 MyBatis 계층 구성, 목록 조회와 화면 연동, 활동 내역·파일 처리
- **기술:** Java 17, Spring Boot, Thymeleaf, MyBatis, MySQL, JavaScript

[백엔드 코드](https://github.com/tomatosugarpickled/candm-back) · [AWS 배포 버전](https://github.com/tomatosugarpickled/aws-candm) · [상세 포트폴리오](https://app.notion.com/39dc7b94f5a681548913d737a9ec3186)

## 코드로 확인할 수 있는 문제 해결

| 사례 | 변경 내용과 근거 |
| --- | --- |
| 로그인 식별값 누락 | DTO에서 누락된 값을 다시 읽던 방식을 바꾸고, 인증 시 전달받은 식별값을 인증 객체에 전달했습니다. [수정 커밋](https://github.com/tomatosugarpickled/globalgates-back/commit/cf41f5eeaf2f1eac41680d88d59a41d5abc778d7) |
| 비활성화 직후 로그아웃 실패 | 로그아웃 경로의 회원 조회 실패 처리와 토큰 누락 시 분기를 보완했습니다. [수정 커밋](https://github.com/tomatosugarpickled/globalgates-back/commit/920b04cd40f7fec4516b9c0f22c49367f42a1b32) |
| 회원 정보 변경 시 캐시 처리 | 배포 저장소에서 반환값이 없는 변경 메서드에 `@CacheEvict`를 적용했습니다. [반영된 코드](https://github.com/CI-CD-globalgates/CI-CD-globalgates/blob/master/src/main/java/com/app/globalgates/service/MemberService.java) |

개발 저장소와 배포 저장소는 반영 시점이 다릅니다. 각 사례의 코드와 실행 검증 범위는 [Global Gates README](https://github.com/tomatosugarpickled/globalgates-back#검증-범위와-남은-과제)에 구분해 두었습니다.

## 학습 기록

Java 기초와 네트워크 학습 내용을 예제 코드와 함께 정리하고 있습니다.

[Java 학습 코드](https://github.com/tomatosugarpickled/study-java) · [벨로그](https://velog.io/@tjdgh1851/posts)

<details>
<summary>사용·학습 기술과 도구</summary>

<!-- ======================== Tech Stack ======================== -->
<div align="center">

## 🛠️ Tech Stack 🛠️

<table>
  <tr>
    <th align="center">Back-End</th>
    <th align="center">Front-End</th>
    <th align="center">Database</th>
    <th align="center">IDE</th>
    <th align="center">InfraStructure</th>
  </tr>
  <tr valign="top">
    <td>
      <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      <img src="https://img.shields.io/badge/JSP-007396?style=flat-square&logo=java&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" />
      <img src="https://img.shields.io/badge/JSON-000000?style=flat-square&logo=json&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
      <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" /><br/>
      <img src="https://img.shields.io/badge/Thymeleaf-005F0F?style=flat-square&logo=thymeleaf&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/MyBatis-DC382D?style=flat-square&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=eclipseide&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/DBeaver-382923?style=flat-square&logo=dbeaver&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Sourcetree-0052CC?style=flat-square&logo=sourcetree&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=flat-square&logo=intellijidea&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/AWS%20S3-569A31?style=flat-square&logo=amazons3&logoColor=white" />
      <img src="https://img.shields.io/badge/AWS%20EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white" />
      <img src="https://img.shields.io/badge/AWS%20IAM-DD344C?style=flat-square&logo=amazoniam&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/AWS%20Route%2053-8C4FFF?style=flat-square&logo=amazonroute53&logoColor=white" />
      <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Gabia-2D2D2D?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
      <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" />
    </td>
  </tr>
</table>

<table>
  <tr>
    <th align="center">Communication</th>
    <th align="center">Management</th>
    <th align="center">Environment</th>
    <th align="center">API</th>
  </tr>
  <tr valign="top">
    <td>
      <img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=slack&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=discord&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white" />
      <img src="https://img.shields.io/badge/yml-CB171E?style=flat-square&logo=yaml&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=springboot&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/JUnit-25A162?style=flat-square&logo=junit5&logoColor=white" />
    </td>
    <td>
      <img src="https://img.shields.io/badge/JDBC-4479A1?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/REST-02569B?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/Kakao%20Map-FFCD00?style=flat-square&logo=kakao&logoColor=black" />
      <img src="https://img.shields.io/badge/KAKAO%20login-FFCD00?style=flat-square&logo=kakao&logoColor=black" /><br/>
      <img src="https://img.shields.io/badge/BootPay-EA4335?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/SMTP%20Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white" />
      <img src="https://img.shields.io/badge/Naver%20login-03C75A?style=flat-square&logo=naver&logoColor=white" />
      <img src="https://img.shields.io/badge/Google%20login-4285F4?style=flat-square&logo=google&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Facebook%20login-1877F2?style=flat-square&logo=facebook&logoColor=white" />
      <img src="https://img.shields.io/badge/SOLAPI-FF6F00?style=flat-square&logoColor=white" />
      <img src="https://img.shields.io/badge/OAuth2-3C8DBC?style=flat-square&logo=oauth&logoColor=white" />
      <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" /><br/>
      <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white" />
    </td>
  </tr>
</table>

</div>

<br/>


</details>

<details>
<summary>전체 프로젝트 저장소</summary>

<!-- ======================== Projects ======================== -->
<div align="center">

## Projects

<table>
  <tr>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/CI-CD-globalgates">
        <b>CI-CD-globalgates</b>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/globalgates-back">
        <b>globalgates-back</b>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/globalgates-front">
        <b>globalgates-front</b>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/aws-candm">
        <b>aws-candm</b>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/candm-back">
        <b>candm-back</b>
      </a>
    </td>
    <td align="center" width="33%">
      <a href="https://github.com/tomatosugarpickled/candm-front">
        <b>candm-front</b>
      </a>
    </td>
  </tr>
</table>

</div>


</details>

<!-- ======================== Footer ======================== -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=120&section=footer" />
</div>
