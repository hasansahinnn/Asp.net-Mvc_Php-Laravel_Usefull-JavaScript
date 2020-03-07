------------------------------- //After Page Load + Timer (12 Sec) + Class Trigger Click ----------------------------
window.addEventListener("load", function () {
      setTimeout(chat, 12000);
}, false);

function chat(){$('.hoverl_6R').trigger('click');}
------------------------------- After Page Load + Timer (12 Sec) + Class Trigger Click\\ -----------------------------


----- Add/Remove eventlistener all input with query selector
const inputs = document.querySelectorAll(".input");
function addcl(){
	let parent = this.parentNode.parentNode;
	parent.classList.add("focus");
}
function remcl(){
	let parent = this.parentNode.parentNode;
	if(this.value == ""){
		parent.classList.remove("focus");

	}
}
inputs.forEach(input => {
	input.addEventListener("focus", addcl);
	input.addEventListener("blur", remcl);
});


-----Only Number 
onkeypress='return event.charCode >= 48 && event.charCode <= 57'

-----Only Alpha 
onkeypress='return !(event.charCode >= 48 && event.charCode <= 57)'



------TcNo Control
function tckimlikkontorolu(tcno) {
	var tckontrol,toplam; tckontrol = tcno; tcno = tcno.value; toplam = Number(tcno.substring(0,1)) + Number(tcno.substring(1,2)) +
	Number(tcno.substring(2,3)) + Number(tcno.substring(3,4)) +
	Number(tcno.substring(4,5)) + Number(tcno.substring(5,6)) +
	Number(tcno.substring(6,7)) + Number(tcno.substring(7,8)) +
	Number(tcno.substring(8,9)) + Number(tcno.substring(9,10));
    strtoplam = String(toplam); onunbirlerbas = strtoplam.substring(strtoplam.length, strtoplam.length - 1);
    if (tcno.length == 11) {
        if (tcno[10] == "1" || tcno[10] == "3" || tcno[10] == "5" || tcno[10] == "7" || tcno[10] == "9") {
            $("#tckimlikno").val(tcno.substring(0, 10));
        }
    }
	if(onunbirlerbas == tcno.substring(10,11)) {
		var styleElem = document.head.appendChild(document.createElement("style"));
		styleElem.innerHTML = ".tcNo:before,.tcNo:after {background: #5266d8;}";
		document.getElementById("error").style.display = "none";
	} else{
		var styleElem = document.head.appendChild(document.createElement("style"));
		styleElem.innerHTML = ".tcNo:before,.tcNo:after {background: red;}";
		document.getElementById("error").style.display = "";

	}
}



------
