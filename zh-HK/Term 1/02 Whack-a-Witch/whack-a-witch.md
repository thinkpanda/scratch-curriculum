第一級

#打地鼠

__介紹:__這個作品和 __打地鼠__ 相似。 點擊畫面上的女巫來獲得積分. 這個遊戲的目標是盡可能在30秒內獲得最多的積分！
##￼第一步: 創建一個飛行中的女巫
1. 開始新的作品。2. 移除貓角色及將背景轉為自然／樹林。3. 在新增角色一欄，按開啟角色檔案將女巫新增到作品中（使用costumes/fantasy/witch1）。

現在，我們要讓女巫移動

4. 產生一個名為速度的變數給女巫 。
在舞台上，這個變名應該會顯示為“Sprite1 速度”。如果顯示為“速度”，刪除這個變數及再產生一個只適用此角色的變數。取消勾選速度變數旁的方格令舞台不再顯示它。這個速度變數會控制女巫移動的速度。在遊戲進行中，我們將利用這個變數來控制女巫的速度。5. 在遊戲開始時，我們希望女巫會移動，給她這個程式：

```scratch
	當 (綠旗子) 被點一下
	將變數 速度 的值設為5
	重複執行
		移動 速度 步
	(重複執行)
```		
###測試你的作品__點一下小綠旗__ 和觀察你的女巫。 為什麼她會卡在屏幕的邊緣？

6. 為了避免她卡在屏幕的邊緣. 我們讓她碰到邊緣就反彈。在移動 速度 步以下，插入碰到邊緣就反彈。
```scratch
	當 (綠旗子) 被點一下
	將變數 速度 的值設為5
	重複執行
		移動 速度 步
		碰到邊緣就反彈
	(重複執行)
```

7. 要停止女巫翻轉向下，在角色摘要區域，按只允許左、右翻轉。

###測試你的作品__點一下小綠旗__

女巫在屏幕另一邊移動到另一邊嗎？

把你的作品存檔。

###Things to try￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼__Try changing the value of the speed variable to make her fly faster or slower.____How would you make the witch get faster the longer she flies?__
(This is a tricky one, so don’t worry if you can’t see how to do it. You’ll get more clues as you work through the project.)##STEP 2: Make the witch appear & vanish randomly
To make the game more fun, we want the witch to appear and vanish randomly. We’ll do that with another script that runs at the same time as the one that moves the witch. This new script needs to hide the witch for a random time, then show her for a random time, and repeat that forever (or until the game finishes).
Create this script for the witch:
```scratch
	when FLAG clicked
	forever
		hide
		wait pick random 2 to 5 secs
		show
		wait pick random 3 to 5 secs
	(end forever)
```
###Test Your Project__Click the green flag.__ 
Does the witch move from side to side across the screen and vanish and appear again randomly?

Save your project

###Things to try__Try changing the range of the random numbers. What happens if you pick very big numbers or very small numbers?__(Does this give you any more clues for how to make the witch speed up the longer the game is played?)##￼STEP 3: Make the witch disappear when she’s clicked
To turn this into a game, we need to give the player something to do. They need to click on the witch to make her disappear. When the witch is clicked, we want her to disappear and play a sound.
1. In the Sounds tab, import the sound electronic/fairydust. 
2. Add this script to the witch:
```scratch
	when sprite1 clicked
	hide
	play sound Fairydust
```
###Test Your Project__Click the green flag.__ 
Does the witch disappear and play the sound when you click it?
Save your project
##Step 4: Add a score and timer
We’ve got a witch, but now we want to make a game! We want to score points every time we click on the witch but we also want to have a time limit on the game. We can use a variable for the score and the timer.
1. Create a new Variable for all sprites called score, and alter the script for the witch to increase this variable by one when she is clicked.
```scratch
	when sprite1 clicked
	hide
	play sound Fairydust
	change score by 1
```2. Switch to the Stage and create a new variable (this time just for the stage) called timer. Add a new script that occurs when the green flag is clicked to set timer to 30 and reset the score to 0. Then use a repeat until block to wait a second and then reduce timer byone. This should repeat until timer is 0, at which point use stop all to stop the game.
```scratch
	when FLAG clicked
	set timer to 30
	set score to 0
	repeat until timer = 0
		wait 1 secs
		change timer by -1
	(end repeat)
	stop all
```
###Test Your Project__Click the green flag.__ 
Save your project

###Things to try__How might you make the witch speed up as the game goes on?__
__Well done you’ve finished the basic game. There are more things you can do to your game though. Have a go at this challenge!__
##Challenge: add more witches
If one witch is good, more must be better! Let’s have three witches flying around.1. Duplicate the witch by right-clicking it in the sprite list.2. For each witch adjust the size of the sprite so the witches are different sizes.3. For each witch change the speed variable so that they fly at different speeds.4. Move the witches around the canvas so that they are not all together.
###Test Your Project__Click the green flag.__ 
Do you have three witches that move from side to side across the screen, randomly appear and disappear, and disappear when you click on them?
Save your project
###Things to try1. How many witches is a good number for the game?￼￼2. Can you make the witches look different? You could either edit their costumes, or use some blocks from the Looks palette to change them.3. Can you make the witches be worth different points? How about making the fastest (and smallest) witch worth 10 points?
__Well done you’ve finished, now you can enjoy the game!__Don’t forget you can share your game with all your friends and family by clicking on __Share__ on the menu bar!