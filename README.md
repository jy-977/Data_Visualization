
<h1 align="center">
  <br>
  <a ><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROG5qBN2FeQfslJPfFVvmiuNqIzLbTxI1PsA&usqp=CAU" alt="Markdownify" width="200"></a>
  <br>
    Data Visualization with Power BI
  <br>
</h1>
<div align="center">
    <a href="https://powerbi.microsoft.com/">
    <img src="https://img.shields.io/badge/Microsoft-0078D4?style=for-the-badge&logo=microsoft&logoColor=white"></a>
    <a >
    <img src="https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"></a>
    <a >
    <img src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=microsoft&logoColor=black"></a>
    <a >
    <img src="https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white"></a>
     <a>
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54"></a>
     <a >
    <img src="https://img.shields.io/badge/Udemy-A435F0?style=for-the-badge&logo=Udemy&logoColor=white"></a>

</div>
<br>


## Objective

As a part of DE, ML studying, this repository will contains the review of **Data visualizaion**
데이터분석이 DE, ML에서도 중요하지만, 비즈니스에서 중요한 것은 커뮤니케이션을 위한 데이터 시각화다. 약간의 데이터 분석 쿼리와 함께 효율적인 데이터 시각화를 위한 툴로 power bi 를 이용하는 과정과 목적을 보여준다.
또 비즈니스적인 측면에서 power bi의 역할과 구조화된 데이터 리포트를 제작하는 과정에 대해 기록한다.

Before we go through Power BI, We need to remind : 

    -  What is Power BI for
    -  Why Power BI is necessary
    -  How can we utilize Power BI for business

 <img src="https://github.com/jy-977/Data_Visualization/blob/main/Captures/91.JPG">

 
## Section 2

<Details>
    데이터 전처리 
    데이터 데이터 형식 지정

Power BI Desktop : transform , model, visualize , analyze
Bower BI cloud : share & collaborate
Bower BI Moile : PBI on mobie


1) get data
2) Transfrom Data : clean data ( power query editor)

**2-12**

3 views + power query editor 
report view (visualizae)
data view : exel form
model view : create relationships

**2-14**

GOAL : visualize the sales 
     카테고리, 프로모션, oevertiem sales, 배달 시간 등

TODO : 
        1) transform data
        2) data model 
        3) visualize data
**2-15**

Basic cleaning
Power Query Editor : 
필요없는 top rows 제거

**2-16**

pbix파일 받았는데 경고 뜰 경우 

Transform data : data source setting change


**2-17  : 데이터 전처리**
빈 row / NA 제거 : filter 이용
Duplication 제거 : remove rows 이용 (colum 클릭 --> remove duplicates)

**2-18  : 데이터 타입**

데이터 타입에 따라 reportview에서 생성할 수 있는 chart의 data가 달라짐 

Power Query Editor 에서도 가능하고 그냥 PBI 에서도 가능함 

String : count 만 가능

Date : 날짜로 변환
Locale : 각 국가형식에 맞는 data type (date, currency etc) 로 변경해줌
Fixed Decimal : currency 에 적합


**2-19  : 데이터 교체 Replacing value**

method 1) replace values option 사용


method 2) Error occured 

    method 2-1) 
         text-->decimal 할때 에러 뜨는 경우 있음
         이때 text ==> replace values (NA ==> 0 혹은 빈칸) ==> fixed decimal 
    
    method 2-2) replace error
    
==> 요약 : Replace Values + Change Date를 잘 조합해서 에러를 없애고 적당한 데이터 타입을 지정하는게 중요하다
</Details>


## Section 3

<Details>
**22 Data Extract**

Transform Tab : Extract
    options

        First / Last Characters
        Text Before / After / Betwee Delemiter 
         (단위제거 값 빈칸 넣어주면 단위 상관없이 제거됨) 


**23 Split Column 열 분할**
열분할 + character transfrom 


**24 Text Operation**

우클릭 Transfrom - trim : 앞뒤 공백 삭제
clean : control cracters(공백, tab) 이런거 깔끔하게 삭제
capitalize : 단어 맨 앞글자 Capitalize


**26 Relations**

model view 에서 product_id drag and drop

은근 관계을때 생각 좀 해야함

**31 piechart**

==> 웬만하면 안쓰는게 낫다,, column chart better 

hard to read --> column chart 
1) Don't use for similar values
2) Don't compare 2 pie chart
3) Only display percentage of total
4) Ideally 2,3 categories ( max 5)
5) No legend --> label + percent 

**32 piechart**

</Details>



## Section 4
<Details>
**34 Table Append**
**35 Table Append Query**
테이블 병합후 column 처리 해줌
이름 다른건 같은이름으로 바꿔서 병합하면되고
같은값인데 다른 이름으로 된건 column 병합

**36 Data & Hierarchy**
날짜별 데이터 년도/ 월별/ 분기별 / 일별 --> heirarchy
차트로 만들때 이것들이 중요한 부분이 될 수 있다

6) 전처리
   header 지정
   필요 없는 row 지우기
   열 분할
   텍스트 단위 없애거나 나누거나,,,

    데이터 타입 지정
    수치 : standard 

    legend : 범례
</Details>

## Section 5


<Details>
**47 merge queries**
이미 있는 테이블에 열 추가
**48 pivot/unpivot**
열/행의 의미를 바꾸는것
ex) building cost / land cost / other cost
    1000            2000        3000
    1500            2500        3300
    2500            1600        9400

이런식의 테이블이 있다고 치면 이걸 항목 / 값 이런식으로 바꿈
ex) cost type       / cost amount
    building cost       1000
    land cost           2000
    other cost          3000
    building cost       1500
    land cost           2500
    other cost          3000

이게 피봇팅 반대는 unpivoting : transform (unpivot )

**49 many to many relationship**

cross filter direction : 화살표
A-->B
    foreign table

many to many : 양방향
중요 : 기본적으로 트랜잭션이 있는 테이블(fact table) --> demension table 


**50 visual filter options**
slicer 로 모델뷰에서 테이블에 대한 필터를 설정 할 수 있음
여러개 slicer 만들어서 필터 항목별 날짜별 값범위 이렇게 세세하게 나눌 수 있음
신기한건 하나 움직이면 reportview 의 모든 개체(visualization)모델들이 동적으로 움직이는것을 확인 할 수 있다


**51 page edit**
이 report view 안에서 model 들을 어떻게 배치하는지 배경을 어떤색으로 넣는지도 중요한 요소임
익건 보고용 이니까 ㅇㅇ
</Details>


## Section 6
1)이제까지는 데이터를 편집해서 가공하고
2) 가공된 데이터로 모델을 만들었다

이제부터는 이 준비된 데이터와 모델을 통해서 대화형을 visualization
<Details>
**53 Filter window**
data blank space : value not correct
--> trim , clean!

**54 Top N filter**
show top , bottom by each fields

**55 Sync slicer**
slicer을 다른 페이지에서도 sync 해서 사용
page A 에서 설정한 슬라이서도 page B에서 똑같이 동작
method 1) page A에서 Ctrl C V
method 2) view tab==> sync slicer


**56 Treemap**
항목이 너무 많을때 한번에 다 못보여줌 (bar chart)--> treemap
space efficient!
hierarchical data 에도 굿
--> 같이 grouping 해도 좋고 // detail에 sub data넣으면 색은 유지, 공간만 나눠짐

**57 interaction edit** 
**[50](#Section-5)** 처럼 하나 클릭하면 다른 visual들도 그에 맞게 움직이는 것을 interaction 이라고 하는데 이것도 editable
1. visual 선택 2. format tab 3. edit interations

**58 drill through**
visual에서 해당항목을 상세히 보고싶을때 링크시켜줌

**59 drill through -keep filter**
drill through original filter 유지할지 말지

**62 activate, deactivated load**
PQE ( power query editor) 테이블 enalble load -- 활성화
비활성화 --> 파일크기 감소

**63 reference and duplication of table**
refernce table duplication table

**64 column from examples**
reference 로 table 참조
column from example로 열참조 ===> custom 해서 value 값 바꿈

</Details>

## Section 7

**66 visualization sort**
정렬 - 요일순
1) visualize 우측 상단 ... ==> ORDER
2) column tools - sort by column ==> COLUMN 순으로 정렬


**67 conditional column add**
66을 위해 CONDITIONAL CULUMN을 만듦
요일 : 우리는 월-일 순으로 알고있지만 컴퓨터는 string type으로 아니까 abc 순으로 정렬하게 됨 
이때문에 Monday-->1 Tuesday-->2 이렇게 바꿔서 새로운 column 을 만들어 줘야하는데 이때 conditional column을 씀

**68 Maps**
filled map이랑 map이랑 다름
filled map은 해당 지역을 색칠해서 보여줌
map : bubble로 보여줌, bubble size 값에따라 크기 조절 가능


**70 forecast**
앞선값에 따라 예측값을 보여줄 수 있다 -> line chart
ignore last : 마지막 n 값을 무시하고 예측값을 보여줌 ==> 실제 값과 비교해서 얼마나 예측이 정확한 지 볼 수 있다

정확도 : 얼마나 데이터가 누적되었는지에 따라 다르다
회색부분 : confident interval 신뢰구간


## Section 8 - advanced : parameters, functions
어려워 ㅠ 차라리 그냥 함수 프로그래밍 하는게 더 쉬운데 버튼으로 하나하나 옮겨가면서 해야하니까 불편하다



**85**

list query : 
1) table 
2) single value
3) list

테이블에서 column 추출 ==> list로 새로운 변수? 저장공간 생성


**86 bring data from web**
bring variable value from web page as table
--> change to value
--> use value on the other tables.

**86 bring data from web**


## Section 10 : DAX( DATA ANALYSIS EXRESSION)
<Details>

**91 Calculated Column**
Calcumated Column : 말그대로 dax를 이용해서 생성된 column , 
기존 column 에서 추출 / 편집한 값

**92 Measure**
Measure : data table에는 생성되지 않고 이론적으로만 편집된 값이 존재함
따라서 data table 확인해보면 없음
1) datble independent : 하나의 table에서 독립적임
2) aggreate a mesure --> sum, average 등 집계함수 사용
3) measure 을 사용해야만 값이 계산됨 : 그전까지는 공간 사용 X
 
Difference of measure and calculated column 


**93 measure Table**
Measure Table 생성 해서 Measure 만든것만 모아둔 table을 만들 수 있다
measure --> measure tool 탭 클릭 --> 


**94 Count, DistinctCount, CountRows**
Count : 중복값 포함 몇개인지 알려줌
distinct count: distinct값 몇개인지
count rows : 공백값포함, 중복값 포함 몇개인지 알려줌

**95 sumx**

iterative 함수들
step 1) evalutate expression for everyrows
step 2) aggregate

**96 average, round**

**97 related**

DAX 함수에서 다른 테이블의 column가져오기 : related

ex) losgistics cost = sumx('sales', 'sales'[sales]*RELATED(product[volume]*0.001)

**98 calculate**
정적인 filter을 계산함
시각 모델로 filter링을 해도 변하지 않는 filter를 할때 유용
다른 필터링 (filter context)보다 cacluate 함수가 우선함


**99 filter**
measure 은 다른 mesure에서 참조가 가능함
mesure1 = mesure2*0.02


**100 filter**

not ==> <>
measrue = 조건 1 + 조건 2
filter 사용

          #조건 1 , filter()      #조건2,(filter)
    mesure =  caculate(cost *0.1 , filter(state = 'california')) + cacluate(cost*profit*0.25, filter(state<>'calinfornia'))

    
**101 logic**
&& and
|| or



**102 Command**
fomatting cacluation : shift +enter : 줄바꿈
// ==> COMMAND




**106 ALL**
all : filter 무시

**108 ALLEXCEPT**
allexcept : 1개 빼고 filter 무시

**109 ALLSELECTED**
allselected : 외부 필터는 적용 내부 필터는 무시

**109 DATEADD**
Time intelligence : 

dateadd 지정된 날짜 만큼 앞의 날짜를 포함하는 열
1달전, 1주전.. 등

**110 datesYTD**
Dates year to day 
연말을 기준으로 새로 축적
1월1일 혹은 새로운 년도가 되면 축적이 0에서 다시 시작함
datesYTD, DATSQTD, DATESMTD도 있음

**111 Rounding**
round 
1 소숫점 1자리
-1 10의 자리
round up : 반올림 / rounddown : 반내림

mround : 배수로 올림 (0.25단위라던지..)

ceiling : 올림
floor : 내림

**112 format**
날짜 custom format


</Details>



## Power BI Cloud



<!-- 
<h4 align="center">A minimal Markdown Editor desktop app built on top of <a href="http://electron.atom.io" target="_blank">Electron</a>.</h4>

<p align="center">
  <a href="https://badge.fury.io/js/electron-markdownify">
    <img src="https://badge.fury.io/js/electron-markdownify.svg"
         alt="Gitter">
  </a>
  <a href="https://gitter.im/amitmerchant1990/electron-markdownify"><img src="https://badges.gitter.im/amitmerchant1990/electron-markdownify.svg"></a>
  <a href="https://saythanks.io/to/bullredeyes@gmail.com">
      <img src="https://img.shields.io/badge/SayThanks.io-%E2%98%BC-1EAEDB.svg">
  </a>
  <a href="https://www.paypal.me/AmitMerchant">
    <img src="https://img.shields.io/badge/$-donate-ff69b4.svg?maxAge=2592000&amp;style=flat">
  </a>
</p>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#related">Related</a> •
  <a href="#license">License</a>
</p>

![screenshot](https://raw.githubusercontent.com/amitmerchant1990/electron-markdownify/master/app/img/markdownify.gif)

## Key Features

* LivePreview - Make changes, See changes
  - Instantly see what your Markdown documents look like in HTML as you create them.
* Sync Scrolling
  - While you type, LivePreview will automatically scroll to the current location you're editing.
* GitHub Flavored Markdown  
* Syntax highlighting
* [KaTeX](https://khan.github.io/KaTeX/) Support
* Dark/Light mode
* Toolbar for basic Markdown formatting
* Supports multiple cursors
* Save the Markdown preview as PDF
* Emoji support in preview :tada:
* App will keep alive in tray for quick usage
* Full screen mode
  - Write distraction free.
* Cross platform
  - Windows, macOS and Linux ready.

## How To Use

To clone and run this application, you'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/amitmerchant1990/electron-markdownify

# Go into the repository
$ cd electron-markdownify

# Install dependencies
$ npm install

# Run the app
$ npm start
```

> **Note**
> If you're using Linux Bash for Windows, [see this guide](https://www.howtogeek.com/261575/how-to-run-graphical-linux-desktop-applications-from-windows-10s-bash-shell/) or use `node` from the command prompt.


## Download

You can [download](https://github.com/amitmerchant1990/electron-markdownify/releases/tag/v1.2.0) the latest installable version of Markdownify for Windows, macOS and Linux.

## Emailware

Markdownify is an [emailware](https://en.wiktionary.org/wiki/emailware). Meaning, if you liked using this app or it has helped you in any way, I'd like you send me an email at <bullredeyes@gmail.com> about anything you'd want to say about this software. I'd really appreciate it!

## Credits

This software uses the following open source packages:

- [Electron](http://electron.atom.io/)
- [Node.js](https://nodejs.org/)
- [Marked - a markdown parser](https://github.com/chjj/marked)
- [showdown](http://showdownjs.github.io/showdown/)
- [CodeMirror](http://codemirror.net/)
- Emojis are taken from [here](https://github.com/arvida/emoji-cheat-sheet.com)
- [highlight.js](https://highlightjs.org/)

## Related

[markdownify-web](https://github.com/amitmerchant1990/markdownify-web) - Web version of Markdownify

## Support

<a href="https://www.buymeacoffee.com/5Zn8Xh3l9" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

<p>Or</p> 

<a href="https://www.patreon.com/amitmerchant">
	<img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## You may also like...

- [Pomolectron](https://github.com/amitmerchant1990/pomolectron) - A pomodoro app
- [Correo](https://github.com/amitmerchant1990/correo) - A menubar/taskbar Gmail App for Windows and macOS

## License

MIT

---

> [amitmerchant.com](https://www.amitmerchant.com) &nbsp;&middot;&nbsp;
> GitHub [@amitmerchant1990](https://github.com/amitmerchant1990) &nbsp;&middot;&nbsp;
> Twitter [@amit_merchant](https://twitter.com/amit_merchant)
 -->
