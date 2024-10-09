# About iweb native library

--------------------------------------------------------------------------------

<link href="dist/icon/css/font-awesome.min.css" rel="stylesheet" type="text/css"/>
<link href="dist/iweb.native.css" rel="stylesheet" type="text/css"/>
<script src="dist/iweb.native.js" type="text/javascript"></script>
<script>const iweb = (new iwebApp()); iweb.init();</script>

--------------------------------------------------------------------------------

1. Input - iweb.inputBox();

<input type="text" name="name" data-validation="required" value="">

<input type="tel" name="telephone" data-validation="required|number" value="12345678">

<input type="text" name="email" data-validation="required|email" value="demo@123.com">

<input type="password" name="password" data-validation="required|password" value="Abc123">

<input type="date" name="start_date" data-validation="required|date" value="2024-10-10">

<input type="color" name="mycolor" data-validation="required" value="#000000">

--------------------------------------------------------------------------------

2. Autocomplete - iweb.inputBox();

<input type="text" class="fill-id" name="member_id" value="1" 
    data-validation="required"
    data-autocomplete="1"
    data-default="chan tai man"
    data-url="your_url_here"
    data-param1="type:1"
    data-sfunc="select_autoc"
    data-rfunc="remove_autoc">

--------------------------------------------------------------------------------

3. Select - iweb.selectBox();

<select name="professionals[]" data-validation="required" data-virtual="1" data-filter="1" multiple></select>

--------------------------------------------------------------------------------

4. Checkbox - iweb.checkBox();

<div class="iweb-checkbox-set">
    <div>
        <input type="checkbox" id="promotional_method_1" name="promotional_method[]" value="email" data-validation="required" checked>
        <label for="promotional_method_1">Email</label>
    </div>
    
    <div>
        <input type="checkbox" id="promotional_method_2" name="promotional_method[]" value="mobile" data-validation="required">
        <label for="promotional_method_2">SMS</label>
    </div>

    <div>
        <input type="checkbox" id="promotional_method_3" name="promotional_method[]" value="whatsapp" data-validation="required">
        <label for="promotional_method_3">Whatsapp</label>
    </div>
</div>

--------------------------------------------------------------------------------

5. Raido - iweb.radioBox();

<div class="iweb-radio-set">
    <div>
        <input type="radio" id="male" name="gender" value="male" data-validation="required">
        <label for="male">M</label>
    </div>

    <div>
        <input type="radio" id="female" name="gender" value="female" data-validation="required">
        <label for="female">F</label>
    </div>
</div>

--------------------------------------------------------------------------------

6. Responsive Div - iweb.responsive();

<div class="iweb-responsive" data-width="1280" data-height="712"></div>

--------------------------------------------------------------------------------

7. Ajax Post

iweb.ajaxPost({
    dataType: 'json',
    url: your_url_here,
    values: {
        name_1: 1,
        name_2: 2
    }
}, function(responseData) {
    console.log(responseData);
});

--------------------------------------------------------------------------------

8. Ajax Form - iweb.initForm();

<form data-ajax="1"></form>

--------------------------------------------------------------------------------

9. Ajax Upload

iweb.bindEvent('click', '#btn-select-files', function(target, e) {
    iweb.uploader({
        dataType: 'json',
        url: your_url_here,
        values: {
            name: 'abc'
        },
        allowed_types: 'jpg|png|pdf',
        max_filesize: 8
        auto_close: true
    }, function() {
        cosole.log('end');
    });
}

Or

<div><input type="file" id="myfiles1"></div>

iweb.uploaderArea('myfiles1', {
    dataType: 'json',
    url: your_url_here,
    values: {
        name: 'abc'
    },
    allowed_types: 'jpg|png',
    max_filesize: 8
    auto_close: true
}, function() {
    cosole.log('end');
});

--------------------------------------------------------------------------------

10. Pagination - iweb.pagination('div.mypage');

<div class="mypage" data-totalpage="10"></div>

--------------------------------------------------------------------------------

11. Dialog

alert(message = '', callBack, customizeClassName)

confirm(message = '', callBack, customizeClassName)

dialog(htmlCode, initFunc, callBack, customizeClassName)

--------------------------------------------------------------------------------

12. Event

bindEvent(eventType, selector, callBack)

triggerEvent(eventType, selector) {

--------------------------------------------------------------------------------

13. Validation

isValue(value)

isMatch(value1, value2, sensitive = false)

isNumber(value, digital_mode = false)

isEmail(value)

isPassword(value)

isDate(value, format = 'Y-m-d')

--------------------------------------------------------------------------------

14. Convert

toNumber(value, currency_mode, decimal)

toDateTime(value, format = 'Y-m-d H:i:s')

--------------------------------------------------------------------------------

15. Cookie

setCookie(cname, cvalue, exdays = 14)

getCookie(cname)

--------------------------------------------------------------------------------

16. Others

deBounce(callBack, delay = 100, prevent = true)

showBusy(status, value)

scrollTo(element, adjustment_value, callBack)

formatBytes(bytes, decimals)

getURL(extra)

getURLParameter(name)

randomNum(min, max)

randomString(length)

detectDevice(index)

--------------------------------------------------------------------------------

16. Callback - DOMContentLoaded

function iweb_common_layout(function(win_width) { });

function iweb_layout(function(win_width) { });

function iweb_extra_layout(function(win_width) { });


function iweb_common_func(function() { });

function iweb_func(function() { });

function iweb_extra_func(function() { });

--------------------------------------------------------------------------------

17. Callback - windowLoaded

function iweb_common_layout_done(function(win_width) { });

function iweb_layout_done(function(win_width) { });

function iweb_extra_layout_done(function(win_width) { });


function iweb_common_func_done(function() { });

function iweb_func_done(function() { });

function iweb_extra_func_done(function() { });

--------------------------------------------------------------------------------

18. Callback - windowResize

function iweb_common_layout(function(win_width) { });

function iweb_layout(function(win_width) { });

function iweb_extra_layout(function(win_width) { });

--------------------------------------------------------------------------------

19. Callback - windowScroll

function iweb_common_scroll(function(scroll_top) { });

function iweb_scroll(function(scroll_top) { });

function iweb_extra_scroll(function(scroll_top) { });
