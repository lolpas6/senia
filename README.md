# senia
var sicret = ["машина", "телефон", "мобильник", "трактор", "автомобиль","компьютер"];
var sicret = sicret[Math.floor(Math.random() * sicret.length)];

var answerArray = [];
for (var i = 0; i < sicret.length; i++){
   answerArray[i] = "_"
}
var remainingLetter = sicret.length

while (remainingLetter > 0){
alert(answerArray.join(" "))
var guess = prompt("Угадайте букву, или нажмите отменя для выхода")
if (guess === null) {
	break;
} else if (guess.length !== 1){
	alert("Пожалуйста, введите одну букву");
} else {
	for (var j = 0; j < sicret.length; j++) {
		if (sicret[j] === guess) {
			answerArray[j] = guess;
			remainingLetter--;
		}
	}
}
}
    alert(answerArray.join(" "));
	alert("Отлично! Было загадано слово " + sicret);
