# jquery-set-uri-and-remove-uri

~~~
<script type="text/javascript">

var urlParams = new URLSearchParams(window.location.search); //get all parameters
var iParam = urlParams.get('i'); //extract the foo parameter

if(iParam && iParam == 'dgst') { 
   $('.diagnostics-message').html('<div class="alert alert-success" role="alert"><button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button><i class="flaticon-tick-inside-circle"></i><strong>Well done!</strong> Diagnostics Added Successfully</div>');


var uri = window.location.toString();
if (uri.indexOf("?") > 0) {
    var clean_uri = uri.substring(0, uri.indexOf("?"));
    window.history.replaceState({}, document.title, clean_uri);
}

}
~~~
