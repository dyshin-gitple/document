---
title: 채팅상담으로 전환하는 방법
tags: [channel]
keywords: 채팅상담, 상담원 대화
summary: 챗봇 대화에서 상담원 대화로 전환하는 방법을 정리하였습니다.
sidebar: danbee_doc_sidebar
permalink: channel_chatperson.html
folder: danbeeDoc
previous: {
    title: 마이크로소프트 팀즈(MS TEAMS),
    url: channel_teams.html
}

---
## 인공지능과 사람의 분업
인공지능 시대에는 자동화 부분은 인공지능이 맡고 사람은 사람만이 할 수 있는 일로 서로 분업하여 효율이 높아진다는 이야기를 들어보셨을 것입니다. 챗봇쪽도 마찬가지입니다. 챗봇이 자동으로 처리할 수 있는 문의에 응답하고 접수를 해주고 사람은 자동화할 수 없는 영역에 집중 하는 것이죠.


 {% include image.html file="channel/chatperson/chatperson.png" alt="챗봇과 사람의 분업" caption="챗봇과 사람의 분업" %}

## 분업 방법 1. 콜백
콜백은 실시간이 아닌, "아~ 제가 담당자에게 연락드리라고 하겠습니다!"이야기 한 후 담당자(사람)에게 연락처와 간략한 메모를 전달하는 방법입니다. 챗봇이 연락처와 메모를 받아서 담당자에게 메일이나 문자를 보내주는 형태로 만들 수 있어요.

## 분업 방법 2. 채팅상담

채팅상담은 챗봇 채팅창을 이용하던 사람들이 자연스럽게 사람과 대화를 할 수 있다는 점이 좋습니다. 하던 대화를 이어서 진행할 수 있겠죠?

 {% include image.html file="channel/chatperson/navertalktalk.png" alt="네이버 톡톡에서 상담원 전환" caption="네이버 톡톡에서 상담원 전환" %}

## 채팅상담 연계 방법 2가지
챗봇과 채팅상담으로 연계되는 흐름은 크게 두 가지가 있습니다. 
1) 챗봇과 대화하던 대화창에서 바로 인간 상담원과 대화가 이어지는 흐름
2) 챗봇과 대화하던 대화창은 종료되고 인간 상담원과 대화할 수 있는 채팅창이 다시 열리는 흐름

1번이 사용자 입장에서는 더 자연스럽습니다. 대신 채팅창에서 챗봇이 사용하는 UI가 함께 제공되어야 한다는 점이 고려되어야 해요.
2번은 별도로 만들어 놓더라도 쉽게 구현이 가능합니다. 대신 사용자 입장에서는 1번보다는 부자연스럽습니다.

단비AI에서는 채팅상담 기능을 제공하고 있지 않습니다. 따라서 연결한 메신저나 채팅상담 솔루션에서 관련 기능을 제공할 경우에 이용하실 수 있는 시나리오입니다. (채팅 상담을 직접 만들 수 있거나 기존에 가지고 있는 모듈이 있다면 위 2가지 방법중에 선택해서 개발하는 것을 추천드립니다.)

### 1. 챗봇대화창에서 바로 사람 상담원과 대화
1번을 하기 위해서는 채팅창을 제공하는 모듈에서 챗봇연계 기능을 제공해야 가능합니다. strong>카카오톡</strong>과 <strong>네이버톡톡</strong>은 챗봇대화를 중단하고 사람과 대화하는 기능을 기본적으로 제공하고 있어요. 단비AI를 이용해서 연결하신 경우에도 바로 이용하실 수 있습니다. [네이버톡톡 연결방법](channel_navertalk.html#네이버톡톡-상담원-연결하기)
사용 방법은 <strong>카카오톡</strong>과 <strong>네이버톡톡</strong> 채팅상담 계정에서 확인하실 수 있습니다.

<strong>페이스북</strong>은 단비에서 제공하는 채널연결 기능을 이용해 연결할 경우 채팅상담 전환기능은 현재 이용할 수 없습니다. 
직접 페이스북 API를 통해서 연결할 경우 단비에서 만든 챗봇도 연결이 가능합니다.

국내에서 많은 분들이 이용하는 <strong>채널(channel.io)</strong>는 채널을 먼저 설정하신 후에 단비AI개발팀에서 2주정도 작업을 통해 연결이 가능합니다. 비용은 상담량에 따라 상이할 수 있어 채널IO와 연결을 원하시는 분은 contact@danbee.ai로 연락을 주시면 도와드리도록 하겠습니다.

### 2. 챗봇대화창을 종료하고 상담원 채팅창이 열리는 방식
채팅상담솔루션에서 링크 버튼 방식으로 대화를 시작하게 할 수 있는 경우 챗봇버튼유형을 웹링크로 적용하면 간단히 구현할 수 있습니다.

<strong>깃플(Gitple.io)</strong>를 이용하고 있으시다면, 깃플에서 먼저 채팅상담을 설정한 후에 깃플 고객센터에 단비챗봇연결을 요청하면 도와드리고 있습니다. 이때, 추가 서버증설이 필요할 수 있으며 최소 비용은 월 10만원입니다.


## 챗봇-채팅상담 연계 시나리오 적용 시 고려사항
챗봇이 먼저 대화해보고 안되면 바로 사람이 대응한다는 것은 이상적인 협업의 모습입니다.
다만, 채팅 상담원이 충분하지 않다면 기다려야 하는 상황도 발생할 수 있어요. 챗봇이 대답 못하고, 또 상담원을 기다려야 한다면 대화하는 입장에서는 더욱 불편함을 느낄 수 있습니다. 따라서 상담원이 늘 대기하고 있는 것이 아니라면 콜백방법이 더 좋을 수 있습니다. 

다시 말해 채팅상담연계 방식은 이미 채팅상담을 하고 있는 기업이 적용하기에 좋습니다. 기존에 적용되어 있는 채팅상담 솔루션에 무인 상담 계정을 하나 만들고 이 계정에 챗봇을 연결하는 것이죠. 최초 대응은 챗봇이 하게 하거나 대기시간이 10초 이상 늘어나면 챗봇이 대응하도록 안내하는 방식이 효과적입니다. 

현재 기업상황을 잘 고려하여 최선의 선택을 하시기 바랍니다.


{% include bottom.html %}