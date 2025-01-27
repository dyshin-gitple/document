---
title: 단비챗봇빌더 1월 업데이트 알림 - 챗봇 만들기가 더 쉬워졌어요!
tags: [blog, chatbot-biz, Chatbot-UX]
keywords: blog
summary: 글의 맨 밑에 소스코드 주소가 있어요.
sidebar: blog_sidebar
permalink: newsletter_2301.html
folder: blog

---

{% include image.html file="blog/newsletter/2023/vol1/img01.png" %}

## 1.노드 미리보기 기능 추가

[대화 흐름] 메뉴에서 말풍선 내용을 수정할 때, 어떻게 변하는지 실시간으로 확인할 수 있는 '미리보기' 창이 추가되었어요.  
<br/>
  
  
{% include image.html file="blog/newsletter/2023/vol1/img02.png" %}

---

## 2. 메뉴 추가 및 순서 변경

[지식 답변] 메뉴는 본래 '고급 설정' 카테고리에 있던 것을 ➡️ '챗봇 제작' 카테고리로 옮겼답니다.  
  
[실패 메시지] 메뉴는 본래 [챗봇 추론 설정] 메뉴 안에 있었는데요. 이번에 따로 메뉴화되어 독립했습니다. 🤗  
<br/>
  
  
{% include image.html file="blog/newsletter/2023/vol1/img03.png" %}

---

## 3. 재확인메시지 버튼개수 조절

[특수상황 설정] 메뉴 속 재확인(Reconfirm)메시지에서 나오는 버튼 개수를 조절할 수 있게 되었습니다.  
<br/>
  
  
{% include image.html file="blog/newsletter/2023/vol1/img04.png" %}  

- 테스트 패널에서 입력한 예문은 '개발'입니다.  

- 테스트 결과, 버튼명 [프린터개발]은 50%, [3D프린터개발]은 33.3%가 나왔습니다.   

- 설정되어 있는 재확인(Reconfirm)범위는 20~60%이기 때문에, 두 버튼 모두 설정범위 안에 들어갑니다. 이때 나타나는 버튼 개수를 설정할 수 있게 되었습니다. (최대 6개)  


화면에서 어떻게 나타나는지 보면 이해가 바로 되실 거에요!

​

테스트 패널을 켠 후

[챗봇 테스트] 탭에서

똑같이 '개발'이라고 입력했어요

​

⬇️⬇️⬇️

​

버튼수가 1개일 때
: 두개 중 확률이 높았던
[프린터 개발]만 표시

​

버튼수가 2개일 때
: [3D프린터개발]버튼까지
함께 선택지로 제시  
<br/>
  

{% include image.html file="blog/newsletter/2023/vol1/img05.png" %}


---


## 4. 중의적 의도추론 버튼개수 조절

[특수상황 설정] 메뉴 속 중의적 의도 추론(Multi Intent)메시지에서 나오는 버튼 개수를 조절할 수 있게 되었습니다.<br/><br/>


기능적으로는 방금 설명한 내용과 똑같은데요.<br/><br/>
  
​
재확인 메시지인가: (Reconfirm)
중의적 메시지인가: (Multi Intent)<br/><br/>  

​
하는 개념상의 차이가 있습니다.<br/><br/>  
  
​
중의적 메시지의 예를 하나 들어볼게요.<br/><br/>  
  
​
"나는 차를 좋아해"라고 했을 때, 자동차 🚘일 수도 있고, 마시는 차 일 수도 있겠지요?<br/><br/>  
  
​
대화를 하던 맥락에 따라 어떤 '차'인지 알 수 있을 것입니다. 이때 발화자의 의도가 마시는 차였다면, #홍차 #녹차 #보리차 등의 키워드는 챗봇엔진이 추론했을 때 높은 인접률을 보일 거에요.<br/><br/>  
  
​
#버스 #소방차 #경찰차 등의 키워드도 '차'라는 부분은 걸리지만 맥락적으로는 아닐 확률이 높지 않다고 보겠지요.<br/><br/>
  
​
그래서 중의적 메시지 버튼 설정의 경우 추론율 범위가 5%를 넘어가지 못하게 되어있습니다. (버튼 개수를 최대 6개까지 할 수 있는 것은, 리컨펌 메시지의 경우와 동일합니다.)<br/><br/>
  
​
정리하자면, '최상위 결과의 몇%까지 중의적 표현으로 볼 것인가' 하는 부분을 설정할 수 있게 되었습니다.<br/>


{% include image.html file="blog/newsletter/2023/vol1/img06.png" %}


{% include bottom.html %}