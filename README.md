# FFXIV_GP_Lite
* 基于 [FFXIVChnTextPatch-GP](https://github.com/GpointChen/FFXIVChnTextPatch-GP) 修改
* 追加資料來源 [FFXIVChnTextPatch-Souma](https://github.com/Souma-Sumire/FFXIVChnTextPatch-Souma)

## 額外追加說明
* TextCommandParam 指令副選項 為選擇性要件如需使用請自行放入rawexd內
* Cactbot 使用者 在翻譯漢化階段 請取消下列三個的漢化處理
  Action(部分小細節的判定)
  Bnpcname(影響基本運作)
  Placename(影響計時器) 

  
![alt text](image.png)
* 高難專用的會另外放在別的地方處理

## 重要提醒
* 使用漢化包時，請不要展示道具，他人看到的道具名稱會是「中文」。
* 不可使用舊版本漢化，會導致遊戲文件不匹配和各種遊戲問題。
* ACT解析插件語言與原用戶端語言保持一致，例如英文或日文，設置後需要重啟ACT。
* 使用漢化包屬修改客戶端之行為，使用者須自行承擔風險。
* 此項目僅提供學術行為及技術交流使用。
* 嚴格禁止使用於任何商業用途。
* 請下載後24小時內刪除。

# FFXIV Translation Patch Tool
FFXIV的中文漢化器。更多資訊可參考[Wiki頁面](https://github.com/GpointChen/FFXIVChnTextPatch-GP/wiki)。

English description can be found in [Wiki pages](https://github.com/GpointChen/FFXIVChnTextPatch-GP/wiki).

相較於原版：
1. 針對5.5X以後版本修正中文字庫補丁。
2. 新增使用CSV進行漢化的功能。CSV是使用修改過的SaintCoinach輸出。
3. 刪除原版exe中與teemo連線的部分。

## 使用
目前可以使用CSV、中國服檔案或他人製作的漢化覆蓋檔進行漢化。

為了避免更新時出現問題，建議每次更新前先還原檔案，下載完更新後再次漢化。

還原時不需設置資料夾，直接點擊還原即可。

請注意，如果沒有額外備份原遊戲檔案，請不要重複漢化，因為會覆蓋`backup`資料夾裡面的備份檔。



請從[release](https://github.com/GpointChen/FFXIVChnTextPatch-GP/releases)下載。

<img src="https://github.com/GpointChen/FFXIVChnTextPatch-GP/blob/master/docs/fig1.png?raw=true" width="480px" />

<img src="https://github.com/GpointChen/FFXIVChnTextPatch-GP/blob/master/docs/fig2.png?raw=true" width="480px" />

### 如何使用CSV進行漢化？（推薦）
0. 下載右邊的release版本或自行編譯
1. 開啟EXE程式
![](https://i.imgur.com/RPim0G0.png)
2. 點選「設置」
![](https://i.imgur.com/OypMCof.png)
3. 選擇FFXIV遊戲根目錄（例如：`D:\FFXIV\SquareEnix\FINAL FANTASY XIV - A Realm Reborn`）
4. 「檔案語言」：CSV代表使用`resource/rawexd`裡面的CSV檔案進行漢化（推薦）
5. 「原始語言」：想要覆蓋遊戲中的哪種語言（我自己是覆蓋日文，不保證覆蓋其他語言會不會有問題）
6. 「目標語言」：（不需選擇）
7. 點擊「確定」
![](https://i.imgur.com/RPim0G0.png)
8. 點擊「漢化」

其他漢化方法不保證100%可用，請參考[Wiki頁面](https://github.com/GpointChen/FFXIVChnTextPatch-GP/wiki)。


## 編譯筆記
[製作過程的筆記可以參考這裡。](https://hackmd.io/@GpointChen/SJi_gv-ad)

如果你是使用 MacOS，可能需要參考[這篇](https://github.com/GpointChen/FFXIVChnTextPatch-GP/blob/master/docs/MACOS_BUILD.md)。  
如果你是使用 SteamOS（在 SteamDeck 上使用），可能需要參考[這篇](https://github.com/GpointChen/FFXIVChnTextPatch-GP/blob/master/docs/LINUX_BUILD.md)。 


## 更新註記
詳參本專案的[Wiki](https://github.com/GpointChen/FFXIVChnTextPatch-GP/wiki/1.-%E9%A6%96%E9%A0%81)。


## 原項目說明
	
项目说明：

	此工具作用于：
	对国际服客户端(SE版)进行中文资源注入

	此程序
	默认只对国际服客户端打中文字库补丁
	不包含任何中文内容
	
	此项目于 2019-09-01 完全开源

使用方法：

	1.下载编译项目，或者直接下载release发布包
	2.解压运行项目
	3.选择FFXIV游戏根目录
	4.点击汉化按钮 等待
	5.Enjoy
	
	如果需要中文内容替换
	请自行将中文客户端的
	>最终幻想XIV/game/sqpack/ffxiv
	文件夹下的三个文件
	0a0000.win32.dat0
	0a0000.win32.index
	0a0000.win32.index2
	复制到汉化工具的
	>resource/text
	文件夹下重新运行程序即会自动读取
	
	PS:这次的补丁包含了字库内容
	所以不需要重新再打字库补丁
	PS2:每次汉化流程都会备份当前文件
	所以避免在已经汉化的文件上进行二度汉化
	这样会备份已汉化文件导致还原回滚失效
	PS3:因为不确定更新是否会覆盖文件
	所以在每次更新前尽量还原文件以免游戏导致不测
	
	注意:
	繁體中文/正體中文 版本
	可能因为翻译原因有部分的BUG存在
	请慎用使用
	
	特别注意：
	本程式采取修改客户端的形式进行中文资源的加载
	使用本程式表示你已经知晓这是违反官方规则的操作
	并且确认自行承担使用程式带来的任何后果

免责声明：

	1.此项目仅供学习技术以及技术交流使用
	2.严禁使用于任何商业用途
	3.请下载后24小时内删除
