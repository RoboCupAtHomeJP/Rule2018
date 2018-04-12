

# Go Get It in Unknown Envrionment
In this task, it is assumed that a robot acquires the knowledge about domestic environments through interaction with its owner when the robot are  newly introduced. In particular, it is focused on objects name and their locations and we evaluate ability of acquisition and generalization about those knowledge through interaction.   

このタスクでは，新たなロボットが家庭に導入された際に，人がその家庭の様々な情報をロボットへ教示することで，ロボットが知識を獲得することを想定している．特に家具や物体の配置・呼び方などを対象として，人とのインタラクションを通してロボットが新たな知識を獲得すること，またその知識を実環境の中で汎化して利用することを目的として，これらの性能を評価する．

## Focus
1. Efficient knowledge acquisition with HRI
2. Generalization of acquired knowledge
3. Mobile manipulation
4. Online mapping 


5. HRIによる効率的な知識獲得
6. 獲得した知識の汎化
7. モバイルマニピュレーション
8. オンラインマッピング


## Task
1. **Traning Phase** 
    * After the door is opened, the robot and a team member (teacher) enter the arena. 
      ドアオープンによりロボットと，ロボットへの教示を行うチームメンバー1名（教示者）が入場．

    * The teacher teaches features, names, locations and so on of five unknown objects. The teacher can use any methods for teaching that do not conflict with the rules of RoboCup@Home. Therefore, the following methods are not allowed. 
      教示者はロボカップ＠ホームのルールに反しない範囲で，ロボットに部屋内に配置された5つ未知物体の特徴・名称・物体の位置等を教示する．以下の行為は原則として禁止である．
		
	- Input from external devices such as keyboard, mouse, touchpad, laptop pc and smart phone.        キーボード・マウス・タッチパッド，ノートPC，スマートフォン等からの入力

    * After the teaching, the robot moves to the designated position and the team member declares the end of training phase. 
    教示終了後に指定された場所へロボットを移動させ，チームメンバーがTraning Phaseを終了することを審判に宣言する．

3. **Test Phase**
    Following procedure is repeated five times: 
    
    * The referee generates a sentence "Bring me \*. " to have the robot bring a object. The generated sentence is a sentence thet can identify one object in the environment using object categories, features, location and so on. Words used in the sentence is not opened. Examples of the sentences are as follows:
    審判は，特定の物を持ってくるような指示文「Bring me \*. 」を生成する．物体をそのカテゴリ，見た目，位置などで特定できるような指示文となるが，どのような単語が使われるかは公開されない．以下が指示文の一例である．

		- "Bring me a juice near the standing person. "
		- "Bring me a red object in front of the TV. "

      The time taken to generate the sentence is not included in the time limit. 
      文生成をしている時間は制限時間には含まれない．
 
	* One team member (instructor) instructs the robot using the sentence "Bring me \*. "
	  指定場所でチームメンバー（指示者）がロボットに特定の物を持ってくるように「Bring me \*. 」と音声にて指示をする．

	* If the robot cannot recognize it correctly or the instructor makes speech error, the instructor can instruct the robot three times in total. The instructor also can skip the instruction and, in this case, this instruction is considered as failure. 
	ロボットが指示文を認識できない場合や指示者が言い間違えた場合，指示者は合計3回まで同じ指示文をロボットへ与えることができる．また，チームの判断により，次の指示へと移行できる．その場合は，与えられた指示は失敗とみなされる．

	* The robot can ask if it is OK to execute the task using yes-no question. To answer the question, the instructor can only use "yes" or "no." Moreover, the instructor cannot answer "yes" to the question whose answer should be "no" and vice versa. 
	ロボットは，指示者に対して実行していいかの確認のみを行うことができる．その際，指示者が発して良い単語は「Yes」または「No」のみである．また，明らかに「No」と答えるべき質問に，「Yes」と答えることはできない．

	* The robot grasps the specified object, return to the designated position and hand it to the instructor.
	ロボットは指示された物を掴み，指定された場所へ戻り，物体を指示者に手渡す．

	* If the robot brings a false object, it is put to the original position again. 
	もし，ロボットが誤った物体を持ってきてしまった場合には，その物体は再度フィールド内へと戻される．

## Additional Rules and Remarks
* **Restart:** The team can restart the task only once. In this task, time limit of restart described in the general rules is not applied. The task finish when the robot cannot restart within the time limit of the task. When the team declare the restart, the objects and their locations are changed.  
チームは1回のみリスタートをすることができる．本タスクではGeneral Ruleにある再開に要する制限時間は設けない．ただし，タスク全体の制限時間内に復帰できない場合には，そこでタスクは終了となる．リスタートを宣言した場合，物体配置，対象となる物体などは変更される．

* **Room and designated position:** The room used in this task and designated position where the robot takes order are announced the previous day.
 タスクで使用する部屋と，ロボットが戻ってくる指定場所は前日にアナウンスされる．

* **Object locations:** There are objects that are not used in the environment. After the training phase, the objects are randomly moved about 10 cm. 
 物体は学習対象の物体以外の物体も置かれている．Traning Phase終了後，物体を10cm程度移動させる．

* **Furniture location:** The furniture locations are changed about 30 minutes before the task. After the change, the team members cannot enter the room. 
家具の配置はタスク開始30分前に変更される．変更後，部屋へ入ることはできない． さらに，チームごとに家具の配置が変更となることがある．

* **Publish the method:**  If the team publish the method with used in this task a paper or web page, the additional points are given. The team send url of the paper or the web page to the exective comittee via e-mail the previous day. The EC review it and judge if the additional points can be given. 
 本タスクで使用した手法・プログラムを論文・Webで公表した場合，加点される．論文・Webページは，タスク前日のチームリーダーズミーティング後に，実行委員へメールにて送付すること．実行員で審議し，公表内容によっては加点とならない場合もある．


## Score Sheet

The maximum time for this task is 10 minutes. 
タスクの制限時間は10分である．



|Action　　　　　　　　　　　　　　　|Score　　　|
|:---------------------------------------|-:|
|||
|***Test Phase:***||
|　Reaching a specified locaiton			|5x10|
|　Grasping a correct object			|5x20|
|　Delivering a correct object			|5x20|
|||
|***Special penaltie & bonuses:***	||
|　Not attending					|-50|
|　Outstanding performance		|15|
|　Publishing the method						|35|
|||
|Total(excluding penalties and bonus)   |250|

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ1NzExMzI3MSwtODI5NDAzMjk5XX0=
-->