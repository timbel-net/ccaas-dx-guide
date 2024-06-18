---
theme: purplin
background: https://cover.sli.dev # like them? see https://unsplash.com/collections/94734566/slidev
dark: false
title: CCaaS
highlighter: shiki
drawings:
  persist: false
fonts:
  sans: 'IBM Plex Sans KR'
  serif: Jua
class: text-center
transition: slide-left
mdc: true # enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
---
# Hi, CCaaS!

CCaaS［ɕːikæs］개발에 대한 모든 것



---
layout: quote
position: center
---
# [docs.langsa.ai](https://docs.langsa.ai)


---
layout: quote
position: center
transition: slide-up
---
# 로컬 개발환경 구성


---
transition: slide-up
---

# 코드저장소 gitlab
<small>각 저장소에는 권한 할당에 의해서 접근이 가능해요.</small>

|     |     |     |
| --- | --- | --- |
| 상담어드바이저 | ADV | [/ccaas/adv/service-adv](https://haiv.timbel.net:48443/ccaas/adv/service-adv)‎ ‎ ‎ ‎ ‎ [/ccaas/adv/ui-adv](https://haiv.timbel.net:48443/ccaas/adv/ui-adv) |
| 콜봇 | CB | [/ccaas/cb/service-cb](https://haiv.timbel.net:48443/ccaas/cb/service-cb)‎ ‎ ‎ ‎ ‎ [/ccaas/cb/ui-cb](https://haiv.timbel.net:48443/ccaas/cb/ui-cb) | |
| 대화엔진 | CE | [/ccaas/ce/service-ce](https://haiv.timbel.net:48443/ccaas/ce/service-ce)‎ ‎ ‎ ‎ ‎ [/ccaas/ce/ui-ce](https://haiv.timbel.net:48443/ccaas/ce/ui-ce) | |
| 지식관리시스템 | KMS | [/ccaas/kms/service-kms](https://haiv.timbel.net:48443/ccaas/kms/service-kms)‎ ‎ ‎ ‎ ‎ [/ccaas/kms/ui-kms](https://haiv.timbel.net:48443/ccaas/kms/ui-kms) | |
| 품질평가 | QA | [/ccaas/qa/service-qa](https://haiv.timbel.net:48443/ccaas/qa/service-qa)‎ ‎ ‎ ‎ ‎ [/ccaas/qa/ui-qa](https://haiv.timbel.net:48443/ccaas/qa/ui-qa) | |
| 상담분석 | TA | [/ccaas/ta/service-ta](https://haiv.timbel.net:48443/ccaas/ta/service-ta)‎ ‎ ‎ ‎ ‎ [/ccaas/ta/ui-ta](https://haiv.timbel.net:48443/ccaas/ta/ui-ta) | |



---
transition: slide-up
---
# 코드저장소 복제
<small>해당되는 프로젝트의 선택 하세요.</small>

### Back-end
<select class="outline-none" onchange="document.getElementById('be-command').textContent=`git clone https://haiv.timbel.net:48443/ccaas/${this.value}/service-${this.value}`">
<option value='adv'>상담어드바이저</option>
<option value='cb'>콜봇</option>
<option value='ce'>대화엔진</option>
<option value='kms'>지식관리시스템</option>
<option value='qa'>품질평가</option>
<option value='ta'>상담분석</option>
</select>
<pre class="inline language-shell" id="be-command">git clone https://haiv.timbel.net:48443/ccaas/adv/service-adv</pre>

<br>
<br>
<br>

### Front-end
<select class="outline-none" onchange="document.getElementById('fe-command').textContent=`git clone https://haiv.timbel.net:48443/ccaas/${this.value}/ui-${this.value}`">
<option value='adv'>상담어드바이저</option>
<option value='cb'>콜봇</option>
<option value='ce'>대화엔진</option>
<option value='kms'>지식관리시스템</option>
<option value='qa'>품질평가</option>
<option value='ta'>상담분석</option>
</select>
<pre class="inline language-shell" id="fe-command">git clone https://haiv.timbel.net:48443/ccaas/adv/ui-adv</pre>


---
layout: image-x
image: https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image.png
transition: fade-out
---
# README.md
<small>프로젝트 시작전에 꼭 읽어주세요</small>


---
layout: quote
position: center
transition: slide-up
---
# 플러그인 설치

## checkstyle

---
layout: image-x
image: https://docs.langsa.ai/img/screenshots/plugins-00.png
transition: slide-up
---

- [checkstyle 다운로드](https://plugins.jetbrains.com/plugin/1065-checkstyle-idea) 및 설치
- Settings > checkstyle 에서 스냅샷과 같이 설정


---
layout: image-x
image: https://docs.langsa.ai/img/screenshots/plugins-01.png
transition: fade-out
---

- 검사할 파일을 열고
- 결과 확인


---
layout: quote
position: center
transition: slide-up
---
# 플러그인 설치

## sonarlint


---
layout: image-x
image: https://docs.langsa.ai/img/screenshots/plugins-02.png
transition: fade-out
---

- [sonarlint 다운로드](https://plugins.jetbrains.com/plugin/7973-sonarlint) 및 설치
- Settings > sonarlint 설정
- 검사 대상 파일을 열고 실행


---
layout: quote
position: center
transition: slide-up
---
# 개발 시나리오
기획서는 Slack 을 통해서 개별 전달될 예정입니다.

---
transition: slide-up
---
# feats-*

- main 브렌치에 push 할 수 없어요.
- 특정 업무의 개발이 시작될 때 feats-user-management 와 같이 생성하세요.
- 하루에 1번은 push 를 해주세요.


---
transition: slide-up
---
# commit

- 주기는 짧을 수록 좋아요.
    - Presentation, Service, Repository 등의 Layer 별로
    - 또는 파일 단위로
- 메세지 규칙을 지켜주세요.
    - 첫줄 시작에 "Prefix 기호 + 공백 + 제목" 은 필수 입니다.
    - 자세한 내용은 그 다음줄부터 작성하시면 됩니다.
    - 기본적으로 커밋 메세지 템플릿을 띄워 드려요.

### 예시
```text {1|2-5}
✨ 사용자관리 - 프로필 수정 기능
UserController.create() 개발 및 insert sql 작성
DB Table Schema 에서 사용자 이미지관련 필드 추가 요청 (users.photo) 
```


---
transition: slide-up
---
# checkstyle
checkstyle 검증 결과는 다음과 같이 확인하세요.

![](https://docs.langsa.ai/img/screenshots/checkstyle-00.png)



---
transition: slide-up
---
# push
코드저장소에 푸시 규칙

## `feats-*` or `fixed-*` 두가지 형식만 가능

![](https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-2.png)




---
layout: image
image: https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-1.png
transition: slide-up
---
<h1 class="text-shadow">CI/CD</h1>



---
layout: image
image: https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-4.png
transition: slide-up
---
<br>

<h1 class="text-shadow">정적코드분석 리포트</h1>


---
transition: slide-up
---
<h1 class="text-shadow">정적코드분석 해결</h1>

<img src="https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-5.png" width="300">
<img src="https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-6.png" width="500" class="absolute top-60 left-13">
<img src="https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-7.png" width="600" class="absolute top-30 right-8">


---
transition: slide-up
---
# 이슈 
버그, 수정요청 등의 포괄적인 편집 사항

![](https://raw.githubusercontent.com/timbel-net/ccaas-dx-guide/main/public/image-3.png)


---
transition: fade-out
---
# fixed-*

- `fixed-just-you-ugly` 브렌치를 새로 생성 해서,
- 기존의 `feats-*` 브렌치와 같이 동일한 시나리오를 반복 합니다.


---
layout: end
---

# 끝
