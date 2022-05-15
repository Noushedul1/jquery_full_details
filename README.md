___
section 1
___
```javascript
// first,last,odd,even,*,gt(),lt(),eq(),multiple css 

    $('ul li a:first').css('color','green');
    $('a:last').css('color','red');
    $('a:odd').css('color','red');
    $('a:even').css('color','red');
    $('*').css('color','red');
    $('a:gt(3)').css('color','red');
    $('a:lt(3)').css('color','red');
    $('a:eq(3)').css('color','red');
    $('a:eq(3)').css({
        color: 'white',
        border: '1px solid black',
        background: 'black'
    });
```
___
section 2
___
```javascript
//:text,:submit,:button

    $(':text').css('color','red');
    $(':submit').css('color','green');
    $(':button').css('color','red');
```
___
section 3
___
```javascript
//[href],[href="https://google.com"]

    $('a').css('color','green');
    $('[href]').css('color','red');
    $('[href="https://google.com"]').css('color','black');
```
___
section 4
___
```javascript
// hide(),show(),empty(),detach()

    $('#hide').click(()=>{
        $('p').hide();
    });
    $('#show').click(()=>{
        $('p').show();
    })
    $('#empty').click(()=>{
        $('p').empty();
    });
    $('#detach').click(()=>{
        $('p').detach();
    });
```
___
section 5
___
```javascript
// addClass(classname),removeClass(classname),toggleClass(classname)

    $('#addcls').click(()=>{
        $('p').addClass('section5');
    });
    $('#rmcls').click(()=>{
        $('p').removeClass('section5');
    });
    $('#tgcls').click(()=>{
        $('p').toggleClass('section5');
    });
```
___
section 6
___
```javascript
//attr('target','_blank'),removeAttr('target')

    $('.addattr').click(()=>{
        $('a').attr('target','_blank');
    });

    $('.rmattr').click(()=>{
        $('a').removeAttr('target');
    });
```
___
section 7
___
```javascript
//wrap(),wrapAll()

    $('p').wrap('<h4>');
    $('p').wrapAll('<h4>');
```
___
section 8
___
```javascript
// e,e.currentTarget, e.currentTarget.id , e.currentTarget.className , e.currentTarget.innerHTML , e.currentTarget.outerHTML, e.clientX, e.clientY, e.which

    $('#found').click((e)=>{
        console.log(e);
        console.log(e.currentTarget);
        console.log(e.currentTarget.id);
        console.log(e.currentTarget.className);
        console.log(e.currentTarget.innerHTML);
        console.log(e.currentTarget.outerHTML);
        console.log(e.clientX);
        console.log(e.clientY);
        console.log(e.which);
    });
```
___
section 9
___
```javascript
//get method and set method

    var a = $('p').text();
    $('#myval').html(a);

    var p = $('p').attr('class');
    console.log(p);
    var p = $('p').attr('id');
    console.log(p);

    $('#myval').text('akib');
    $('#myval').html('<h2>hello noushedul islam</h2>');
    $('#myval').attr('class','noushed');
```
___
section 10
___
```javascript
//submit form 

    $('#myform').submit((e)=>{
        e.preventDefault();
        var firstName = $('#firstName').val();
        console.log(firstName);

        var lastName = $('#lastName').val();
        console.log(lastName);

        $('#first').text(firstName);
        $('#last').text(lastName);
    });
```
___
section 11
___
```javascript
 $('form').submit((e)=>{
        e.preventDefault();
        console.log(e);
        console.log(e.target);
    })

    $('form').keyup((e)=>{
        e.preventDefault();
        var code = e.which;
        console.log(code);

        var country = $('#country').val();
        console.log(country);
    });
```
___
section 12
___
```javascript
 //array

    var myarr = ['akib','aki','shaki','mohima','arman'];
    console.log(myarr);

    $.each(myarr, (i,val)=>{
        console.log(`${i} ${val}`);
        $('ul').append('<li>'+val+'</li>');
    });
```
___
section 13
___
```javascript
// append, prepend, appendTo, prependTO

    $('ul').append('<li>joy</li>');
    $('ul').prepend('<li>anish</li>');

    $('#firstP').appendTo('#secondP');

    $('#firstP').prependTo('#secondP');
```
___
section 14
___
```javascript
 // fadeIn(), fadeOut(), fadeToggle(), stip()

    $('#fadeOut').click(()=>{
        $('#content').fadeOut('fast');
        $('#content').fadeOut('slow');
        $('#content').fadeOut(3000);

        $('#content').fadeOut(2000, ()=>{
            $('#fadeOut').css('color','red');
        });
    });

    $('#fadeIn').click(()=>{
        $('#content').fadeIn('fast');
        $('#content').fadeIn('slow');
        $('#content').fadeIn(3000);

        $('#content').fadeIn(2000, ()=>{
            $('#fadeIn').css('color','green');
        });
    });

    $('#fadeToggle').click(()=>{
        $('#content').fadeToggle('fast');
        $('#content').fadeToggle('slow');
        $('#content').fadeToggle(3000);

        $('#content').fadeToggle(2000, ()=>{
            $('#fadeToggle').text('toggleDone').css('color','orange');
        });
    });

    $('#stop').click(()=>{
         $('#content').stop();
    });
```
___
section 15
___
```javascript
// slideUp(), slideDown(),slideToggle(),stop()

    $('#slideUp').click(()=>{
        $('#content').slideUp('fast');
        $('#content').slideUp('slow');
        $('#content').slideUp(3000);

        $('#content').slideUp(2000, ()=>{
            $('#slideUp').css('color','red');
        });
    });

    $('#slideDown').click(()=>{
        $('#content').slideDown('fast');
        $('#content').slideDown('slow');
        $('#content').slideDown(3000);

        $('#content').slideDown(2000, ()=>{
            $('#slideDown').css('color','green');
        });
    });

    $('#slideToggle').click(()=>{
        $('#content').slideToggle('fast');
        $('#content').slideToggle('slow');
        $('#content').slideToggle(3000);

        $('#content').slideToggle(2000, ()=>{
            $('#slideToggle').text('toggleDone').css('color','orange');
        });
    });

    $('#stop').click(()=>{
         $('#content').stop();
    });
```
___
section 16
___
```javascript
// animate()

    $('#moveLeft').click(()=>{
       $('#box').animate({
           left: 250
       });
    });

    $('#moveRight').click(()=>{
        $('#box').animate({
            left: 0
        });
    });

    $('#moveAround').click(()=>{
        var box = $('#box');
        box.animate({
            left: 250
        });

        box.animate({
            top: 250
        });

        box.animate({
            left: 0
        });

        box.animate({
            top: 0
        });
    });

```
___
section 17
___
```javascript
// on method

    $('#air').on({
        'click': ()=>{
            $('#nature').css('color','green');
        },
        'dblclick': ()=>{
            $('#nature').css('color','red');
        }
    });
```
___
section 18
___
```javascript
// get,jetJSON,ajax,each,map

    $.get('https://jsonplaceholder.typicode.com/posts', (data)=>{
        $.each(data,(i,users)=>{
            console.log(users.title);
            $('ul').append('<li>'+users.title+'</li>');
        })
    });

    $.getJSON('https://jsonplaceholder.typicode.com/posts', (data)=>{
        $.each(data,(i,users)=>{
            console.log(users.title);
            $('ul').append('<li>'+users.title+'</li>');
        })
    });

    $.ajax({
        method: 'GET',
        url: 'https://jsonplaceholder.typicode.com/posts',
        dataType: 'json'
    }).done((data)=>{
        console.log(data);
        $.each(data, (i,users)=>{
            $('ul').append('<li>'+users.title+'</li><p>'+users.body+'</p>');
        });
    });

    $.ajax({
        method: 'GET',
        url: 'https://jsonplaceholder.typicode.com/posts',
        dataType: 'json'
    }).done((data)=>{
        console.log(data);
        $.map(data, (users,i)=>{
            $('ul').append('<li>'+users.title+'</li>');
        });
    });
     $('#postForm').submit((e)=>{
        e.preventDefault();

        var title = $('#title').val();
        var body = $('#body').val();

        var url = $('#postForm').attr('action');

        $.post(url,{title: title, body: body}).done((data)=>{
            console.log(data);
        })

    });
```