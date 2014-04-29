asp.net-mvc-5
=============

This project is presenting how to use asp.net mvc native client side validation with bootstrap modal.

Refactor the project from the second chapter of this book
Pro ASP.NET MVC 5
5th Edition

By Adam Freeman


Issues:
1, Client Side Validating Bootstrap Modal Form (VS 2013/MVC5/BS3)
http://forums.asp.net/t/1979187.aspx?Client+Side+Validating+Bootstrap+Modal+Form+VS+2013+MVC5+BS3+
solution: 
put these lines above your form:

You need to refrence the scripts

<script src="@Url.Content("~/Scripts/jquery.validate.min.js")" type="text/javascript"></script>
<script src="@Url.Content("~/Scripts/jquery.validate.unobtrusive.min.js")" type="text/javascript"></script>

2, Twitter bootstrap remote modal shows same content everytime (disable cache)
http://stackoverflow.com/questions/12286332/twitter-bootstrap-remote-modal-shows-same-content-everytime
solution: 
For bootstrap 3 you should use:

$('body').on('hidden.bs.modal', '.modal', function () {
    $(this).removeData('bs.modal');
});



