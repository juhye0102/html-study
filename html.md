# \<p> 태그

### 개요

```
<p></p>태그는 paragraph, 즉 문단의 약자로 하나의 문단을 만들 때 쓰임.
```



### 사용법

``` 
<p>문단1</p>
```



### 예제 

		<html>
			<body>
				<p>first paragraph</p>
				<p>second paragraph</p>
				<p>
					new line<br>
					third paragraph
				</p>
			</body>
		</html>

### 출력 결과 

```
first paragraph

second paragraph

new line
third paragraph
```



# \<br> 태그 

### 개요

```
기본적으로 HTML은 코드 가독성 향상을 위해 줄 바꿈을 해도 줄 바꿈이 화면에 출력되지 않음. (한 줄로 연이어 나오게 됨.)

줄 바꿈을 하려면 직접 줄 바꿈을 한다는 명령을 적어 주어야 하며, HTML에서는 <br>를 통하여 줄바꿈을 하게 됨.
```



### 사용법

```
첫번째줄<br>두번째줄
```



### 예제 

```
<html>
	<body>
		the 
		first
		line<br>
		the second line
	</body>
</html>
```

### 출력 결과 

```
the first line
the second line
```



### 추가

```
실제 줄 바꿈이 그대로 반영되게 하고 싶을 때는 <pre> 태그를 사용.

(주의) <pre> 태그는 줄 바꿈 뿐만 아니라 띄어쓰기, 탭 등 원래 무시되던 문자들까지 출력되게 됨.
```



# \<img> 태그 



 ### 개요

``` 
<img/> 태그는 이미지를 삽입하는 태그로, src 속성을 통해 이미지 경로를 지정함.

이미지 파일이 src 속성에서 지정한 경로에 없을시, 이미지는 출력되지 않거나 엑스박스가 뜨게 됨.
```



### 속성 

>src : 이미지의 경로

> width : 이미지 가로 크기

> height : 이미지 세로 크기

<p></p>

### 사용법

```
<img src="my,profile.png" width="500" height="300">
```



### 예제

``` 
<html>
<body>
	<p>
		이미지가 정상적으로 삽입 된 경우<br>
		<img src="/images/attach/logo_black.png" width="245">
	</p>
	<p>
		없는 이미지가 삽입 된 경우<br>
		<img src="no_img.png" width="100" height="50">
	</p>
</body>
</html>
```

### 출력 결과



```
이미지가 정상적으로 삽입 된 경우
```



![img](https://ofcourse.kr/images/attach/logo_black.png)

```
없는 이미지가 삽입 된 경우
```

![image-20210414200143405](C:\Users\user\AppData\Roaming\Typora\typora-user-images\image-20210414200143405.png)



# \<table> 태그

### 개요

```
<table> 태그는 HTML 문서에서 표를 만드는 태그임.
행과 열을 표현하기 위해 <tr>, <td> 등의 태그와 함께 작성하게 됨.

이전에는 웹 페이지의 레이아웃을 구성할 때, <table> 태그를 이용하여 많이 구성하였지만, 적당한 사용 방법이 아니므로 레이아웃 구성시에는 <div> 태그와 CSS 이용을 권장함.

º <tr> 태그는 표의 행을 나타냄.
º <td> 태그는 표의 열을 나타냄. <tr> 태그의 하위에 위치함.
```



### 예제

```
<table>
	<tr>
		<td>섹션1</td>
		<td>섹션2</td>
	</tr>
	<tr>
		<td>섹션3</td>
		<td>섹션4</td>
	</tr>
	<tr>
		<td>섹션4</td>
		<td>섹션5</td>
	</tr>
</table>
```

### 출력 결과

<table>
	<tr>
		<td>섹션1</td>
		<td>섹션2</td>
	</tr>
	<tr>
		<td>섹션3</td>
		<td>섹션4</td>
	</tr>
	<tr>
		<td>섹션4</td>
		<td>섹션5</td>
	</tr>
</table>

### thead

``` 
일반적인 표는 제목 줄을 가지고 있는 경우가 많음.
<table> 태그도 제목 줄을 지원하며, <thead>, <tbody>, <th> 태그를 사용하여 구현함.
º <thead> 태그는 표의 제목 영역을 나타냄. <table> 하위, <tr> 상위에 위치함.
º <tbody> 태그는 표의 본문 영역을 나타냄. <thead> 와 같은 위치에 존재함.
º <th> 태그는 제목 셀을 나타냄. <td> 태그 대신 사용됨.
```



### 예제

```
<table>
	<thead>
		<tr>
			<th>학교</th>
			<th>창립년도</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>서울대학교</td>
			<td>1946</td>
		</tr>
		<tr>
			<td>고려대학교</td>
			<td>1905</td>
		</tr>
		<tr>
			<td>연세대학교</td>
			<td>1885</td>
		</tr>
	</tbody>
</table>
```

### 출력 결과

<table>
	<thead>
		<tr>
			<th>학교</th>
			<th>창립년도</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>서울대학교</td>
			<td>1946</td>
		</tr>
		<tr>
			<td>고려대학교</td>
			<td>1905</td>
		</tr>
		<tr>
			<td>연세대학교</td>
			<td>1885</td>
		</tr>
	</tbody>
</table>

### rowspan, colspan

``` 
표는 셀 병합을 통해 더 보기 좋게 만들기도 하는데, <table> 태그에서는 rowspan과 colspan 이라는 속성을 통해 병합 기능을 제공함.

º colspan 은 <td> 태그에서 사용하며, 열을 확장함. (좌우로)
º rowspan 은 <td> 태그에서 사용하며, 행을 확장함. (상하로)
```



### 예제

```
<table>
	<tr>
		<td colspan="2">2x1 셀</td>
	</tr>
	<tr>
		<td>1x1 셀</td>
		<td>1x2 셀</td>
	</tr>
</table>
```

### 출력 결과

<table>
	<tr>
		<td colspan="2">2x1 셀</td>
	</tr>
	<tr>
		<td>1x1 셀</td>
		<td>1x2 셀</td>
	</tr>
</table>

### 예제

```
<table>
	<tr>
		<td rowspan="2">1x2 셀</td>
		<td>1x1 셀</td>
	</tr>
	<tr>
		<td>1x1 셀</td>
	</tr>
</table>
```

### 출력 결과

<table>
	<tr>
		<td rowspan="2">1x2 셀</td>
		<td>1x1 셀</td>
	</tr>
	<tr>
		<td>1x1 셀</td>
	</tr>
</table>

# \<form> 태그 

### 개요

```
<form> 태그는 웹 페이지에서의 입력 양식을 의미함. 
로그인 창이나, 회원가입 폼 등이 이에 해당함.

텍스트 필드에 글자를 입력하거나, 체크박스나 라디오 버튼을 클릭하고 제출 버튼을 누르면 백엔드 서버에 양식이 전달되어 정보를 처리하게 됨.

실제로 백엔드 코드와 함께 <form>을 사용하기 위해서는 다음 속성들이 사용됨.

º name : 폼의 이름
º action : 폼 데이터가 전송되는 백엔드 url
º method : 폼 전송 방식 (GET / POST)
```



### input

```
<form> 태그는 전체 양식을 의미하며, 화면에 보이지 않는 추상적인 태그임.
실제로 사용자가 양식을 입력하기 위한 태그는 <input> 태그 등이 사용됨.

type 속성을 통해 종류를 나타내며, name을 통해 데이터의 이름, value를 통해 기본 값을 지정.
```

##### type

```
º text : 일반 문자
º password : 비밀 번호
º button : 버튼
º submit : 제출
º reset : 양식 초기화용 버튼
º radio : 한개만 선택할 수 있는 컴포넌트
º checkbox : 다수를 선택할 수 있는 컴포넌트
º file : 파일 업로드
º hidden : 사용자에게 보이지 않는 숨은 요소

등의 유형이 있으며, HTML5에는 더 다양한 종류의 <input> 종류가 추가됨.
```

##### 예제

```
<form>
	<p>
		<strong>아이디</strong>
		<input type="text" name="name" value="아이디 입력">
	</p>
	<p>
		<strong>비밀번호</strong>
		<input type="password" name="password" value="비밀번호 입력">
	</p>
	<p>
		<strong>성별</strong>
		<input type="radio" name="gender" value="M">남자
		<input type="radio" name="gender" value="F">여자
	</p>
	<p>
		<strong>응시분야</strong>
		<input type="checkbox" name="part" value="eng">영어
		<input type-"checkbox" name="part" value="math">수학
	</p>
	<p>
		<input type="submit" value="제출">
	</p>
</form>
```

##### 출력 결과

<form>
	<p>
		<strong>아이디</strong>
		<input type="text" name="name" value="아이디 입력">
	</p>
	<p>
		<strong>비밀번호</strong>
		<input type="password" name="password" value="비밀번호 입력">
	</p>
	<p>
		<strong>성별</strong>
		<input type="radio" name="gender" value="M">남자
		<input type="radio" name="gender" value="F">여자
	</p>
	<p>
		<strong>응시분야</strong>
		<input type="checkbox" name="part" value="eng">영어
		<input type-"checkbox" name="part" value="math">수학
	</p>
	<p>
		<input type="submit" value="제출">
	</p>
</form>



### select, option

```
<select> 및 <option>은 드롭다운 리스트를 만드는 태그임.
```

##### 예제

```
<select>
	<option value="ktx">KTX</option>
	<option value="ㅑtx">ITX 새마을</option>
	<option value="mugung">무궁화호</option>
</select>
```

##### 출력 결과

<select>
	<option value="ktx">KTX</option>
	<option value="ㅑtx">ITX 새마을</option>
	<option value="mugung">무궁화호</option>
</select>

### 기타

```
º <lable>
º <textarea>
º <button>
º <optgroup>
º <fieldset>

태그 등이 <form> 에서 활용됨.
```



# \<div> 태그

### 개요

```
<div></div> 태그는 Division의 약자로, 레이아웃을 나누는데 주로 쓰임.

다른 태그와 다르게 특별한 기능을 갖고 있지는 않고, 가상의 레이아웃을 설계하는데 쓰이며, 주로 CSS와 연동하여 쓰임.
```



### 사용법

```
<div>content1</div>
<div>content2</div>
```



### 예제

```
<html>
	<body>
		<div style="background-color:cyan">구역1</div>
		<div style="width:100px; height:100px background-color:#CFO">구역2</div>
	</body>
</html>
```

##### 출력 결과

<html>
	<body>
		<div style="background-color:cyan">구역1</div>
		<div style="width:100px; height:100px; background-color:#CF0">구역2</div>
​	</body>
</html>



# \<span> 태그

### 개요

```
<span></span> 태그는 <div></div> 태그처럼 특별한 기능을 갖고있지 않고, CSS와 함께 쓰임.
<div> 태그와의 차이점은 display 속성이 block이 아닌, inline이라는 점인데, 이는 CSS display 항목에서 세부 정보를 알 수 있음.

<div>와 <span>의 차이
<div> 줄 바꿈 O
<span> 줄 바꿈 X
```



### 사용법

```
<span>내용</span>
```



### 예제

```
<html>
<body>
	<span style="background-color:red">span1</span>
	<span style="background-color:blue">span2</span>
	<span style="background-color:green">span3</span>
</body>
</html>
```

##### 출력 결과

<html>
<body>
	<span style="background-color:red">span1</span><span style="background-color:blue">span2</span><span style="background-color:green">span3</span>
</body>
</html>



# \<head> 태그

### 개요

```
<head> 태그는 문서의 머리를 나타내는 태그임.
브라우저 화면에 직접적으로 보이지 않으며, 숨은 데이터를 정의하는 태그들이 들어가게 됨.
```



### 목록

```
<head> 태그 내부에 들어가는 대표적인 태그들의 목록
º <title>
º <meta>
º <link>
º <style>
º <script>
```



# \<title> 태그

### 개요

```
<title></title> 태그는 웹 페이지의 제목을 나타내는 태그.
웹 페이지 본문에는 보이지 않으며, 브라우저의 탭 등에서 확인 할 수 있음.

유저에게 문서의 제목을 알리는 용도 뿐만 아니라, 검색 엔진 등에서 가장 크게 보여지는 텍스트이므로 페이지의 특성을 드러내는 제목을 작성하는 것이 중요.
```



### 예시

```
<html>
<head>
	<title>HTML 개요 - ofcourse</title>
</head>
<body>
	...
</body>
</html>
```

