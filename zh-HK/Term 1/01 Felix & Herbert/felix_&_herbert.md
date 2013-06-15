第一級

#小飛與小拔

__介紹:__
我們將會製作一個__小貓小飛__捕捉__老鼠小拔__的遊戲。你用滑鼠控制着小拔，別讓小飛捉到它。小拔避開愈久，積分就愈高。但別讓小飛捉到，要扣分啊。
##￼第一步：小飛跟着鼠標跑
1. Start a new project.
Keep track of your progress by ticking off the boxes below:
2. Click on the stage next to the sprite and switch to the Backgrounds tab, and then import the background indoors/hall. Delete the original blank background.
3. 把sprite 的名字改成「小飛」。
4. Make sure Felix only points left-right by clicking this button:
5. Create this script:

```scratch

	When FLAG clicked
	forever
		point towards mouse-pointer
		move 10 steps
		next costume
		play drum 62 for 0.3 beats
	(end forever)
```
		
###Test Your Project
__Click the green flag.__
小飛有追着鼠標跑嗎？他移動時看起來像在走路嗎？他移動的快慢冾當嗎？
Save your project
##第二步：小飛追趕小拔

__接下來，我們要小飛追着老鼠小拔，而不是鼠標。__

1. Create another sprite using the choose new sprite from file button and selecting animals/mouse1.
2. 把sprite 的名字改成「小拔」。
3. Edit the costume and make it smaller than Felix.
Try six clicks on the shrink button:
4. Make sure Herbert only points left-right. 5. Give Herbert this script:


```scratch
	
	When FLAG clicked
	forever
		go to mouse-pointer
		point towards Felix
	(end forever)
```
###Test Your Project

__Click the green flag.__

小拔有隨着着鼠標移動嗎？小飛有追着小拔嗎？
Save your project.
##第三步：小飛捉到小拔後說些話

__我們想小飛知道他捉到了小拔，還要告訴我們。__

1. Change Felix’s script to be this:

```scratch
	
	when FLAG clicked
	forever
		point towards mouse-pointer
		move 10 steps
		next costume
		play drum 62 for 0.3 beats
		if touching Herbert
			say Caught you! for 1 secs
		(end if)
	(end forever)
```

###Test Your Project

__Click the green flag.__

小飛捉到了小拔時說了葛麼？
Save your project.

##第四步:￼小拔被捉到時會變成鬼魂

__Instead of Felix saying something, we want Herbert to turn into a ghost when he’s caught.__

1. Change Felix’s script to send this message when he catches Herbert.

```scratch
	
	when FLAG clicked
	forever
		point towards mouse-pointer
		move 10 steps
		next costume
		play drum 62 for 0.3 beats
		if touching Herbert
			broadcast caught
			play drum 58 for 0.2 beats
			wait 1 sec
		(end if)
	(end forever)
```
2. Import a new costume into Herbert from fantasy/ghost2-a.
3. Edit the costume to make it smaller.
Six clicks on the shrink button should do.
4. Change the names of Herbert’s
costumes so the mouse costume is
called ‘alive’ and the ghost costume is called ‘dead’.
5. Create a new script for Herbert to turn him into a ghost:
```scratch
	
	when I receive caught
	switch to costume dead
	wait 0.5 secs
	switch to costume alive
```
	
###Test Your Project

__Click the green flag.__

小拔被捉到時有變成鬼魂嗎？
小飛在正確的時機發出正確的聲音嗎？
Does Felix still stay still for long enough for Herbert to get away
Save your project
##第五步：保存積分
__Let’s add a score so we know how well we do at keeping Herbert alive.
We’ll start the score at zero and increase it by one every second. If Felix catches Herbert, we’ll reduce the score by one hundred.__
1. Make a variable, for all sprites, called Score. Click on Variables in the top menu, make a variable and name it score
2. On the stage, create these two scripts
```scratch
	
	when FLAG clicked
	set score to 0
	forever
		change score by 1
		wait 1 secs
	(end forever)
	
	when I receive caught
	change score by -100
```
	
###Test Your Project

__Click the green flag.__

積分是否每秒鐘都在增加呢？
小拔被捉到時，積分是否減少了一百分呢？
如果小拔被捉到時，積分還不夠一百分，會發生甚麼事呢？
開始一個新遊戲時，積分是否回到零分呢？

Save your project
__做得好，你完成了！你現在可以好好的玩這遊戲了！__
Don’t forget you can share your game with all your friends and family by clicking on __Share__ on the menu bar