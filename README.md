## 📌 목차
- [📝 RENOBIT 3.1.0](#-RENOBIT-310-)  
- [📝 TIM+ 2.0.2 ](#-tim-202-)
- [📝 TIM+ 2.0.1 ](#-tim-201-)
- [📝 TIM+ 2.0.0 ](#-tim-200-)
- [📝 TIM+ 1.0.3 ](#-tim-103-)

--------------------------------------------------------
## 📝 RENOBIT 3.1.0 <a name="RENOBIT-310"></a><br>


 📦 버전 정보

• 버전: v3.1.0 
• 릴리즈 일자: 2025년 07월 15일<br><br>

 
 
 ✨ Update 
• THREE.js 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ r147 → r174 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 최신 WebGL/3D 기술 반영 및 호환성 확보 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 향상된 렌더링 품질 및 성능 개선, 향후 기능 확장 기반 마련 

• 애니메이션 라이브러리 Anime.js 지원 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 안정성과 호환성을 고려하여 v3(LTS) 기준으로 지원
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ Anime.js 공식 사이트 참고 <br><br>

 

 🧩Feature 
  🗂 그룹 관리 기능 개선 

• Editor Group Tree

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 에디터 좌측 사이드 패널에 ‘그룹 리스트’ 패널 추가
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 그룹 단위로 컴포넌트를 확인 가능 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 각 그룹과 컴포넌트의 소속 관계 파악 가능 

• Codebox Group Tree 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 코드박스 좌측 사이드 패널에 ‘그룹 리스트’ 패널 추가 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 현재 선택한 그룹 컴포넌트에 포함된 인스턴스 목록 표시 

• Codebox Instance Path 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 그룹에 속한 컴포넌트의 상위 그룹 구조를 Path 형태로 확인 가능 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 선택한 컴포넌트의 배치 경로 표시 

 

        * 자세한 사용 방법은 메뉴얼을 참고해 주세요. 
<br>
 

  🛠 개발 생산성 향상을 위한 모듈 추가 

• WKit : 런타임 이벤트 바인딩 및 컴포넌트 초기화 유틸리티 
• GlobalDataPublisher : 전역 데이터 매핑 및 구독 기반 데이터 전파 시스템 
• WEventBus : 컴포넌트 간 커뮤니케이션을 위한 글로벌 이벤트 버스<br><br>

 

 🐞 Bugfix 

• 통합 가져오기 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 통합 가져오기 시 페이지 ID 중복 여부에 대한 체크 개선 
&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 멀티 데이터소스 설정에 대한 동적 로딩이 정상적으로 동작하지 않던 문제 수정 

• 데이터셋 내보내기 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 데이터셋 내보내기 시 일부 데이터 (UserId, URL)의 복호화가 누락되는 현상 해결 

• 설정 파일 암호화 ( globals.properties ) 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ Globals.DbType 설정을 암호화할 때 데이터셋의 동적 DB 쿼리 접근이 제한되던 문제 수정

• Oracle DB 스키마 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ TB_LOGIN_HIST 테이블 SESSION_ID 컬럼 크기 이슈 수정 

• 기타 보고된 이슈 수정


---------------------------------------------------------


## 📝 TIM+ 2.0.2 <a name="tim-202"></a><br>


 📦 버전 정보

• 버전: v2.0.2
• 릴리즈 일자: 2025년 07월 24일<br><br>

 
 
 ✨ 신규 기능

🚀 TIM+ Engine

• SSL 인증서 무시 기능 추가

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ timplus.httpclient.ignore-ssl-cert 속성 추가 <br><br>

 

 🔧 적용 방법

• timplus.yml 에서 하기 같이 입력
&nbsp;&nbsp;&nbsp; # timplus: 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    version: 2.0.2
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   httpclient:
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;       ignore-ssl-cert: true
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;       enabled-custom-SSL: true <br><br><br>

 

⚠️한번 설정하면, 해당 옵션이 적용된 엔진은 가동 중 SSL 인증을 생략하게 되므로, 보안상 사용에 주의가 필요합니다.


----------------------------------------------------------------------------------



## 📝 TIM+ 2.0.1 <a name="tim-201"><br>

📦 버전 정보

• 버전: v2.0.1
• 릴리즈 일자: 2025년 07월 23일 <br><br>

 
✨ 신규 기능

🚀 TIM+ Engine

• 확장 태스크 추가

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ HazelcastMemoryDebugTask 

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ ExtractXmlByXPathTask (실행 중 XPath 평가 기능 포함) <br><br>

 

🔧 주요 수정 사항

🚀 TIM+ Engine

• 워크플로우 업데이트 시 변경 사항이 없어도 캐시가 갱신되도록 수정<br><br>

 

🚀 TIM+ Studio

• AskField List에서 첫번째 값이 적용 안 되는 오류 수정<br><br>

 

📁 기타 변경 사항

• 기본 예제 워크플로우 백업 파일 등록

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 2025.07.04 교육 내용을 반영한 워크플로우 예제 백업 파일이 추가되었습니다.

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ 파일경로 : timplus-engine/files/sample/xxxx_example.tpbk


----------------------------------------------------------------------



## 📝 TIM+ 2.0.0 <a name="tim-200"><br>

📦 버전 정보

• 버전: v2.0.0
• 릴리즈 일자: 2025년 07월 09일<br><br>

 

✨ 신규 기능

🚀 TIM+ Engine

• 클러스터 통신에 대한 타임아웃 설정 기능 추가

• Built-In 함수 추가

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ splitToList: 구분자로 문자열을 나눠 리스트로 반환

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ joinFromList: 리스트를 구분자로 결합한 문자열 반환

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ replaceAll: 정규식 기반 문자열 치환

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ formatDateTime: 밀리초 시간을 포맷된 문자열로 변환

• 신규 태스크 추가

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ Exit 태스크

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ 성공/실패 관계없이 즉시 워크플로우 종료

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ Zabbix 연동 태스크

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 로그인 (Zabbix Login)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 호스트 조회 (Zabbix Host Resolve)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 호스트 그룹 조회 (Zabbix HostGroup Resolve)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 아이템 마지막 값 조회 (Zabbix Item Last Value)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 아이템 히스토리 조회 (Zabbix Item History)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ Zabbix 아이템 트렌드 조회 (Zabbix Item Trend)

&nbsp;&nbsp;&nbsp;&nbsp;  ▪ Read a text file line by line 태스크

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ○ 텍스트 파일을 한 줄씩 읽기<br><br>

 

🔧 주요 수정 사항

🚀 TIM+ Engine

• 비밀번호 정책, 워크플로우 모니터링 관련 오류 수정

• SQLRawQueryTask 롤백 미작동 문제 수정

• MybatisDirectRegisterTask autoCommit 설정 반영 문제 수정

• Add Header to Response, Set Header in Response 태스크의 필수 파라미터 검증 오류 수정

• Parse Text By Delimiter 태스크의 파싱 오류 수정

• 로그 출력 개선

• format(fmt) -> String Built-In 함수 오류 수정

• UserPolicyEntity 의 createdAt DTO의 create_at 컬럼 매핑 정리 (nullable = false) <br><br>

 


🚀 TIM+ Studio

• 워크플로우 등록 레이어 팝업 내 컨펌 텍스트 유지되는 오류 수정

• 로그인 화면 내 언어 변경 시 invalid text 문구 변경 되지 않는 오류 수정

• 태스크 추가/삭제 후 저장 알림 중복 문제 수정

• 태스크 등록/수정 > 간헐적으로 유효성 검사 실패하는 오류 수정

• 대시보드가 크롬과 엣지에서 워크플로우 정보가 다르게 표출되는 오류 수정

• TransactionQueryTask에서 Testing 팝업 정렬 이슈 수정

• fixedRate,fixedDelay,initialDelay에 숫자만 입력 되도록 수정

• 태스크 삭제 컨펌 문구 오타 및 아이콘 드래그 시 오류 수정

• 브라우저 화면 비율 확대 시 시스템 정보 페이지 UI 깨짐 문제 수정

• Multiple Assign, Parse Text By Delimiter 태스크에서 기존 데이터 삭제되는 문제 수정


-----------------------------------------------------------------------------



## 📝 TIM+ 1.0.3 <a name="tim-103"><br>

📦 버전 정보
• 버전: v1.0.3
• 릴리즈 일자: 2025년 06월 09일<br><br>

 

🔧 주요 수정 사항

🚀 TIM+ Engine

• TransactionQueryTask : clickhouse 테스트 오류 수정
• MybatisDirectRegisterTask : clickhouse 테스트 오류 수정 <br><br>

 

📁 기타 변경 사항

• 설치 가이드가 개발자 가이드에 통합되었습니다. 

• 패키지에는 관리자 가이드와 개발자 가이드가 제공됩니다.

• 개발자 가이드 5.1 TIM+ Container 서비스 항목이 신규 추가 되었습니다.
