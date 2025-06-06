# 링크
링크는 현 위치에서 다른 위치로 이동하는 때에 사용한다. a 요소를 사용한다.

## a (anchor)
앵커 요소는 `href` 특성을 통해 다른 페이지나 같은 페이지의 어느 위치, 파일, 이메일 주소 등 다른 URL로 연결할 수 잇는 하이퍼링크를 만들 때 사용한다. 내부 콘텐츠는 링크 목적지의 설명을 나타내야 한다.

## 특성(Attribute)
### download
링크로 이동하는 대신에 사용자에게 URL을 저장할지 물어본다. 값을 지정할 수 있고, 지정하지 않아도 된다. 값이 없으면 파일 이름과 확장자는 브라우저가 다양한 인자로부터 자동 생성해 제안한다.

값을 지정하면 저장할 때의 파일 이름으로서 제안한다. `\`나 `/`는 `_`로 변환한다. 그 외 다른 파일시스템에서 제한되는 문자들은 브라우저가 필요한 경우 추가로 이름을 조정한다.

### href (Hyperlink Reference)
하이퍼링크가 가리키는 URL. 링크는 HTTP 기반 URL일 필요는 없고, 브라우저가 지원하는 모든 URL 스킴을 사용할 수 있다.

- 페이지 구획을 가리키는 프래그먼트 URL
- 미디어 파일 일부를 가리키는 미디어 프래그먼트

### rel
하나의 스페이스로 구분되는 연결한 URL과의 관계를 나타내는 링크 유형의 목록

### target
링크한 URL을 표시할 위치로, 가능한 값은 브라우징 맥락이다.

- `_self` : 현재 브라우징 맥락에 표시
- `_blank` : 새 브라우징 맥락에 표시. 보통 새 탭이지만 사용자의 브라우저 설정에 따라 다름
- `_parent` : 현재 브라우징 맥락의 부모에 표시하고 부모가 존재하지 않으면 `_self`와 동일하게 작동
- `_top` : 최상단 브라우징 맥락에 표시. 부모가 존재하지 않으면 `_self`와 동일하게 작동

> 참고 : `target`을 사용할 때 `rel="noreferrer"`을 추가하여 `window.opener` API의 악의적인 사용을 방지하는 것을 고려하자. 또한, 최근 브라우저에서는 `tarket="_blank"`를 지정하면 `rel="noopener"`를 적용한 것과 같이 동작한다.

## 주소의 값
- 웹 URL (절대적 경로)
- 이동하고자 하는 페이지 내의 HTML 문서 (상대적 경로)
- 페이지 내 이동 (`id` Attribute 사용)
- 메일 주소와 전화번호 연동

> 참고 : `id`를 사용하려면 `a href="#idname"`처럼 사용하면 된다.

> 참고 : 메일쓰기를 연동하려면 `a href="mailto:abc@cdf.com"` 형태로 `mailto:` 뒤에 이메일 주소를 입력하면 되고, 전화번호를 연동하려면 `a href="tel:010xxxxxxxx"` 형태로 사용할 수도 있다.

## 코드 예시

```html
<h1> 
    네이버
</h1>
<h2> 
    모든 이의 더 나은 가능성
</h2>
<p>
    우리는 끝없는 인터넷 세상을 넘어 변화하는 시대를 항해합니다. 우리는 navigators입니다. 우리는 사용자라는 나침반을 따라 변함없이 변화를 만드는 사람들입니다.
</p>

<a href = "naver.com"> 서비스 바로가기 > </a>
```

![](https://velog.velcdn.com/images/aoi-aoba/post/a3f3e361-7dcc-44b6-826d-8f3faebd2697/image.png)