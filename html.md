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

| 섹션1 | 섹션2 |
| :---- | ----- |
| 섹션3 | 섹션4 |
| 섹션4 | 섹션5 |



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

| 학교       | 창립년도 |
| ---------- | -------- |
| 서울대학교 | 1946     |
| 고려대학교 | 1905     |
| 연세대학교 | 1885     |



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

| 2x1 셀 |        |
| ------ | ------ |
| 1x1 셀 | 1x2 셀 |



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

| 1x2 셀 | 1x1 셀 |
| ------ | ------ |
| 1x1 셀 |        |

