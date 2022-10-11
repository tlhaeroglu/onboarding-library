# onboarding-library
cardType: 3 adet parametreden biri verilebilir. “introCard”,”pulse” ve “stepCard” bu parametreler ile kartın tipi belirlenir. Zorunlu.

triggerType: “unvisible” ve “draggable” olmak üzere iki değeri vardır. 
“unvisible” yine bir step adımı olarak değerlendirilebilir. Sıra bu type’a geldiği zaman bu type’ın ekrandan kaybolduğu durumda diğer step’e geçilir. Bu özellik kullanıldığına o step içerisindeki cardType:”nocard” vermek gerekir.
“draggable” verilmiş olan target’a herhangi bir sürükleme veya dokunmayla step adımı sonrakine geçilir. Optional ihtiyaç olduğu durumlarda kullanılabilir.

target: html tarafından alınan string bir biçimde class veya id verilmelidir. Örnek “.class”, “#id”. Zourunludur.

onBtnGotIt & onBtnCancel: iki adet durumu vardır.
	type: “click” ise target: “.target” parametresi alır.
	type: “custom ise operation: () => {} triggerolacak bir fonksiyon alır.
Optional.

customLocation: {top:int left:int} değerleri vardır. Bu parametrede verilen değerler otomatik olan konumlandırmanın dışında artı ve eksi değerler vererek verilen pixel kadar kaydırmaktır. Optional.

notRenderStep: bu parametreye o stepin oynatılması veya oynatılmaması ile ilgili ek bir durum eklenebilir. True ve false verilebilir. Ayrıca bir target da verilebilir. Örneğin verilen bir target o an bulunabilmişse step render edilmez ve diğer adıma geçer. Optional.

scrollableArea: bu prop scroll listener özelliği performans açısından isterse aktif edilebilsin diye bir target parametresi alır. Verilmiş target içerisinde bir scroll eventi olduğu zaman konumu günceller. Optional

CardType “introCard” - stepCard” parametreleri:

media: resim veya video formatında import edilmiş bir medya beklenir. Optional.

arrow: card dinamik konumlanır fakat dışarından spesifik bir arrow yönü girilmişse ilk tercih o olur. “top”, “left”, “bottom” vb. Optional fakat kullanılması daha sağlıklı.

arrrowColor & btnColor: string içinde hex veya rgb bir renk kodu kabul eder. Optional.

title & content: string değerler alınabilir veya <></> fragment kullanılarak verilebilir. Optional fakat kullanılması daha sağlıklı.

btnGotIt & btnCancel: string değerler verilir buton içerisindeki yazıyı değiştirir. Optional fakat kullanılması daha sağlıklı.
