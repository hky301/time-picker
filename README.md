# timePicker
a time picker which experience like IOS and it's inspired by the UIDatePicker.
it's base on [picker](https://github.com/ustbhuangyi/picker)

## Usage ##

this time picker only for **mobile** web app and it has very smooth scroll animation.
you can choose time after current time,  but if you want to choose time before current,  fork this repo and do whatever you want.

 It's very easy to use, here is an example.

```html
<div id="date" class="date"></div>
```
```javascript
var $date = $('#date');

$date.timePicker({
	title: '选择出行时间',
	delay: 15,
	day: {
		len: 7,
		filter: ['今天', '明天', '后天'],
		format: 'M月d日'
	}
}).on('timePicker.select', function (e, selectedTime, selectedText) {
  	$(this).text(selectedText);
}).on('timePicker.cancel', function () {
    console.log('user cancel');
});

$date.on('click', function () {
	$(this).timePicker('show');
});
```

## 事件 ##
timePicker.change

当一列滚动停止的时候，会派发timePicker.change事件，同时会传递选择日期的时间戳和显示的文本

timePicker.select

当用户点击确定的时候，会派发timePicker.select事件，同时会传递选择日期的时间戳和显示的文本

timePicker.cancel

当用户点击取消的时候，timePicker.cancel事件。


## Build ##
clone this repo
```bash
git clone https://github.com/ustbhuangyi/time-picker.git
```

install the dependence
```bash
cd time-picker
npm install
```
install webpack if needed

```bash
npm install -g webpack
```
install webpack-dev-server if needed

```bash
npm install -g webpack-dev-server
```
start a server

```bash
webpack-dev-server
```

visit this page via your mobile phone.

> localhost:8080/demo