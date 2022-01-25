# 안드로이드 명명 규칙 - XML

새 프로젝트를 시작할 때마다 아키텍처나 코드 스타일을 통일하는 전략을 세우듯, 리소스 이름을 지정할 전략도 필요합니다.  
정해진 룰은 없지만 성공적인 리소스 관리를 위해 해당 페이지에서는 다음과 같이 명명 규칙을 제공합니다.  


<br/>

## 🌱 기본 원칙 
> 모든 리소스(XML) 이름은 위와 같은 간단한 규칙을 따릅니다.  
> 
```
<WHAT>_<WHERE>_<DESCRIPTION>_<SIZE>
```

### WHAT
* 리소스가 실제로 무엇을 나타내는지를 의미합니다.
* ex) MainActivity -> `activity`

### WHERE
* 앱에서 논리적으로 속하는 위치를 의미합니다.
* 여러 화면에서 사용되는 리소스는 `all` 로 표시합니다.
* 다른 모든 리소스는 해당 리소스가 속한 Android view 하위 클래스 사용자 지정 부분을 사용합니다.
* ex) MainActivity -> `main`

### DESCRIPTION
* 한 화면에서 여러 요소를 구분하기 위해 사용합니다.
* ex) `title`, `button`

### SIZE (Optional)
* 정확한 크기 또는 정해진 크기를 나타낼 때 사용합니다.
* drawable 의 사이즈 표시나 margin 등에 사용됩니다.
* ex) `36dp`, `large`


<br/>

## 🌱 Layouts
```
<WHAT>_<WHERE>
```
* `<WHAT>`은 activity, fragment, view, item, layout 등으로 사용됩니다.  
* ex) `activity_main.xml`, `item_friend.xml`

<br/>

## 🌱 Strings
```
<WHERE>_<DESCRIPTION>
```
* `<WHERE>`은 해당 string 이 사용되는 화면을 나타냅니다. (여러 화면에서 사용될 경우 all 을 사용합니다)
* ex) `sign_in_button_google`, `setting_title`, `all_done`

<br/>

## 🌱 Drawables
```
<WHERE>_<DESCRIPTION>_<SIZE>
```
* ex) `all_background`, `setting_menu_button`

<br/>

## 🌱 Dimensions
```
<WHAT>_<WHERE>_<DESCRIPTION>_<SIZE>
```
* `<WHAT>`에는 width, padding, elevation, textsize 등이 사용됩니다.
* ex) `padding_main_button`, `height_all_topbar`


<br/>

## 🛠 참고
해당 페이지는 [A successful XML naming convention](https://jeroenmols.com/blog/2016/03/07/resourcenaming/) 글을 참고로 작성되었습니다.
