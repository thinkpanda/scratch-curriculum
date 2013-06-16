第一級

#打地鼠

__介紹:__這個作品和 __打地鼠__ 相似。 點擊畫面上的女巫來獲得積分. 這個遊戲的目標是盡可能在30秒內獲得最多的積分！
##￼第一步: 創建一個飛行中的女巫
1. 開始新的作品。2. 移除貓角色及匯入背景 nature/woods。3. 在新增角色一欄，按開啟角色檔案將女巫新增到作品中（使用costumes/fantasy/witch1）。

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

###嘗試
￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼￼__改變速度變數的值令女巫移動快一點或慢一點。____如何令女巫越飛越快?__(這個是棘手的問題，不要擔心。通常完成這個作品，你會得到更多的線索。)##第二步: 令女巫隨機出現及消失

為了令遊戲更加有趣， 在令女巫移動的程式之下，我們將會創作另一個程式。 新程式會令令女巫隨機出現及消失直到遊戲完成。
給女巫這個程式：
```scratch
	當 (綠旗子) 被點一下
	重複執行
		隱藏
		等符 在 2 到 5 間隨機選一個數 秒
		顯示
		等符 在 3 到 5 間隨機選一個數 秒
	(重複執行)
```
###測試你的作品__點一下小綠旗__
女巫在屏幕另一邊移動到另一邊而且會隨機出現及消失嗎？

把你的作品存檔。

###嘗試__嘗試改變隨機數目的範圍。 如果你選擇了十分大或十分小的數目，會發生什麼事？__(這能夠給你線索如何能女巫越飛越快嗎？)##￼第三步: 點一下女巫令她消失
將這個作品變成遊戲，玩家在點擊女巫時會令她消失， 在她消失的同時會播放聲音。
1. 輚到背景標籤， 匯入 electronic/fairydust. 
2. 新增以下程式到女巫：
```scratch
	當Sprite1 被點一下
	隱藏
	播放聲音 Fairydust
```
###測試你的作品__點一下小綠旗__
當你點一下女巫，她有消失和播放聲音嗎？
把你的作吅存檔
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