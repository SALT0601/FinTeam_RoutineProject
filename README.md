# FinTeam_RoutineProject

### 벤처기업 협회에서 주관한 OJT 프로그램의 팀 프로젝트 입니다. 

### 팀원
- <img src="https://img.shields.io/badge/frontend-61DAFB?style=flat-square&logo=React&logoColor=white"/></a> 이민혁 🪄
- <img src="https://img.shields.io/badge/frontend-61DAFB?style=flat-square&logo=React&logoColor=white"/></a> 신주희
- <img src="https://img.shields.io/badge/frontend-61DAFB?style=flat-square&logo=React&logoColor=white"/></a> 이유진
- <img src="https://img.shields.io/badge/backend-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/></a> 한찬희
- <img src="https://img.shields.io/badge/backend-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/></a> 유하영

# SpringBoot_React_Web_Project

Spring Boot의 MVC패턴과 React.js를 기반으로 만든 영양제 복용 기록 및 알림 서비스 입니다. 지속적 복용을 돕기 위해 게이미피케이션 요소를 추가하고 웹 푸시 기능을 구현했습니다. 

# 사용기술

### Back-end
<img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white"/></a>
<img src="https://img.shields.io/badge/SpringBoot-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/></a>
<img src="https://img.shields.io/badge/SpringSecurity-6DB33F?style=flat-square&logo=SpringBoot&logoColor=white"/></a>
<img src="https://img.shields.io/badge/JWT-6DB33F?style=flat-square&logo=JSONWebTokens&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=white"/></a>


### Front-end
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/></a>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=white"/></a>
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=Bootstrap&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Styled-components-DB7093?style=flat-square&logo=tyledcomponents&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=white"/></a>

### DB
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=Redis&logoColor=white"/></a>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=Hibernate&logoColor=white"/></a>


# 사용 툴

<img src="https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat-square&logo=IntelliJIDEA&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Visual_Studio_Code-007ACC?style=flat-square&logo=VisualStudioCode&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=Slack&logoColor=white"/></a>
<img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=Slack&logoColor=white"/></a>



# 기능설명

- ## 회원가입 및 로그인

  - 회원가입 진행시 이메일, 패스워드, 닉네임, 생년월일 을 입력합니다.
  - 패스워드는 패스워드 확인을 이용해 체크하며 `BCryptPasswordEncoder`를 이용해 암호화 하여 DB에 저장하였습니다.
  - 로그인시 JWT 토큰을 발행합니다. 
  - 비밀번호 찾기를 진행할 때 가입한 이메일로 비밀번호 변경 링크를 전송하고 redis를 통해 전송된 링크의 유효성을 검증합니다. 
  
- ## 회원

  - 회원은 `Member`라는 Role을 소유하고 있습니다.
  - 회원은 영양제 등록 페이지에서 복용할 영양제의 복용 시간, 영양제 수량, 복용 갯수를 등록합니다. 
  - 회원은 마이페이지에서 게이미피케이션 요소를 확인할 수 있습니다. 
  - 회원은 개인정보관리 페이지에서 패스워드 및 회원정보를 수정 할 수 있습니다. 이때 패스워드 변경 시 기존 패스워드를 한번 더 체크합니다.




- ## 메인페이지

- 메인페이지에서는 복용할 영양제의 남은 수량과 복용 갯수 및 시간 그리고 복용한 영양제를 체크할 수 있습니다.
- 사용자들의 영양제 복용일수 랭킹을 확인할 수 있습니다.


- ## 웹 푸시

- `Firebase Cloud messaging`을 사용해 사용자가 영양제를 등록할 때 선택한 아침, 점심, 저녁을 구독합니다. 
- 이후 정해진 시간에 `Sprign Schedular`를 이용해 웹 푸쉬를 전송합니다. 



- ## 게이미피케이션

  - 사용자가 영양제를 등록한 시점부터 연속 복용 일 수가 계산됩니다. 
  - 만약 하루라도 복용을 하지 않으면 연속일수는 초기화 되며 최고 연속일수와 현재 연속일수를 확인할 수 있습니다.
  - 또한 복용한 날과 복용하지 않은 날의 영양제의 이미지를 생성합니다.
  - 미리 설정된 정책에 맞춰 회원 별 뱃지를 획득할 수 있습니다. 


- ## 프로젝트 시연 영상 

  ![pillgood](https://user-images.githubusercontent.com/79136087/174006243-bf1aaa7a-a867-4d63-bdab-9337dffb887d.gif)

- 웹 푸시 기능

  ![웹푸시](https://user-images.githubusercontent.com/79136087/174008498-747ea1d5-a375-4b10-b7b3-15661a4c958d.gif)

- ## 웹 전체 실행 영상 

 - https://youtu.be/ajChYZSICEo

