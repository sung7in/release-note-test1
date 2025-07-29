## 📌 목차
- [📝 TIM+ 2.0.2 ](#-tim-202-)
- [📝 TIM+ 2.0.1 ](#-tim-201-)
- [📝 TIM+ 2.0.0 ](#-tim-200-)
- [📝 TIM+ 1.0.3 ](#-tim-103-)



## 📝 TIM+ 2.0.2 <a name="tim-202"></a><br><br>


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



## 📝 TIM+ 2.0.1 <a name="tim-201"><br><br>

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



## 📝 TIM+ 2.0.0 <a name="tim-200"><br><br>

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



## 📝 TIM+ 1.0.3 <a name="tim-103"><br><br>

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
