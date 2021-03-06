# Linux_of_common_sense  

## chapter_1

<dl>
	<dt>1-1	サーバーとは</dt>	
	<dd>コンピュータはネットワークとつながっています。ネットワーク上で、サービスを提供しているのがサーバー、そこに要求を送っているのがクライアントです。コンピュータが役割を分担して処理をすすめる形式をクライアント・サーバーと言います。インターネットで提供されているサービスの多くはクライアント・サーバー方式です。普通に使っているパソコンは通常クライアントだけど、サーバー・ソフトウェアいれればサーバーにもなるよ。コンピューターのソフトウェアは、大きく分けて基本ソフトウェアと応用ソフトウェアに分かれる。応用ソフトウェアはアプリケーション・ソフトウェアです。基本ソフトウェアはオペレーティングシステムで、OSっていう。OSにはサーバ用がある。通常のOSとの違いはライセンスなど、最大接続数に限りがあればサーバーとしては使えない。そこで、Linuxの登場です。多数の企業などが利用しています。無償というのが一番でかい、もちろん無償だからという理由だけでなく、ほかの商用ソフトなどのライセンスの縛りなどがないので、全くでなくてもカスタムがきくのがでかい。</dd>

	<dt>1-2	代表的なサーバーソフトウェア</dt>
		<dd>一番はやっぱりWebサーバーだと思われ、Webブラウザからの要求に答えてます。Webサーバーから外部のプログラムを実行する仕組みをCGIといいます。代表的なのは、Apache,Nginx,IISなどがある。LAMPなどが多い。CGIは、Webページ上で外部のプログラムを実行し、その実行結果をWebページとして出力する仕組みのことです。次、メールサーバーで、インターネット上でメールを配達するSMTPサーバー、メールボックスに届いたメールをユーザーが受け取れるようにするPOPサーバー、IMAPサーバーがある。IMAPは、メールをサーバに置いた状態で確認することができる。POPサーバーの場合は、メールをクライアントにダウンロードして使います。次ファイルサーバー、ネットワーク上でファイルを共有できるようにする。Sambaは、LinuxをWindownsファイルサーバーにすることができる。そして、WindowsサーバーをLinuxサーバーに置き換えることもできる。次、DNSサーバーはアドレスを自動的にIPアドレスに変換します。クライアントから要求を受け取って名前解決してくれます。FTPサーバー、ネットワーク経由でファイルを転送するためのサーバーです。WebサーバーにWebサイトのデータをアップロードしたり、インターネット上からファイルをダウンロードしたりするのに使われます。次、データベースサーバー、たくさんのデータを集めて、効率的に検索したり更新したりできるようにしたデータの集合体のこと。データベースを運用・管理するソフトウェアがデータベース管理システム。データベースとデータベース管理システムを備え、Webサーバーなどにデータを提供するサーバーをデータベースサーバーといいます。で、MySQLとMariaDBがあるがこれは、今MySQLの所有者がOracle者で、元の開発者が分派させたのがMariaDBになっている。次、プロキシサーバークライアントの代理としてWebサーバーやFTPサーバーにアクセスするサーバー。クライアントに代わってWebサイトにアクセスします。利点は、Webサイトへのアクセス制限で、閲覧履歴を残しておきキャッシュを保存するので、次回から高速にアクセスできる。もちろん閲覧規制もメリットの一つ。次、アプリケーションサーバー、大規模なWebアプリケーションや業務システムを動かすには、Webサーバーだけでは不十分で、Webアプリケーションを実行するための基盤を提供するサーバーとしてアプリケーションサーバーが使われます。主な機能は、Javaなどプログラムの実行環境、データベースへの接続機能、トランザクションの管理機能がある。</dd>

	<dt>1-3	Linuxとは</dt>
	<dd>UnixというOSがあり、1960年代の終わりに開発が、大学や研究機関中心に広まった、初期のインターネットはUNIXで構成されていた。UNIXと互換性のあるOSを、当時学生であったリーナス・トーバルズ氏が、インターネットに上げた。Linuxの開発は、インターネットを通じて多くの開発者を巻き込み。急速に発展した。Linuxの開発はオープンに行われている。誰もが自由にプログラムを読み、自由に開発に参加することができる。自由に使えるだけでなく、自由に販売することもできる。Red Hat Enterprise Linuxなど。カーネルとは、OSの中核部のことハードウェアの違いを吸収し、アプリケーション・ソフトウェアが動作するための基盤となる機能を提供する。ディストリビューションとは、カーネルに様々なソフトウェアを組み合わせて、一つのOSとして完成させたもの。「配布物」。ディストリビューションは、いっぱいあり、企業や少人数で作られたものなどもあり、有償のものもある。種類は大きく分けて2つRed HatとDebian。ディストリビューションが違うとインストールできるソフトウェアも違う。オープンソースもライセンスがある。GNU GPLなど。ディストリビューションには有料と無料があるがその違いは機能・性能ではなく、サポートの有無。無料だと自力での解決だが有料だとサポートを受けることができる。サーバーとして選ぶなら、サポート期間を見て選ぶ必要がある。</dd>

	<dt>1-4	Linuxの使いみち</dt>
	<dd>Linuxはよくサーバーとして利用されている。主要なディストリビューションは、Postfix,BINDインターネットで標準的なサーバー・ソフトウェアが付属している。LinuxはUNIXをベースに発展してきたので、インターネットと相性がいい。イントラネッサーバー、インターネットに公開せず、社内のネットワーク上でグループウェアや社内SNS、掲示板などの業務ソフトウェアをフゴ化したり、ファイルサーバーやプリントサーバーとなるもの。Windowsを使っていることが多いが、Linuxでも同等のことができる。デスクトップクライアント、パソコン用のOSでいうとWindowsが圧倒的で、ついでMac OS Xになる。Linuxはこういう商用ソフトがサポート終了した時に使える。組み込み機器、家電にもOSが入っていたりする。これにもLinuxが使われている。細かく調整できるところが選ばれる理由。Raspberry Piなど今のIoTで騒がれている。</dd>
</dl>

## chapter_2

<dl>
	<dt>2-1	コマンドを使った操作</dt>	
	<dd>
		<dl>
			<dt>コマンドとは</dt>
			<dd> Linuxでは、基本的にコマンドを使う。人とコンピューター都の間で情報のやり取りをする接点・操作方式をユーザーインターフェースという。ユーザーインターフェースは大き分けて2つ、GUIとCUIがある。GUIは、一般的なグラフィカルな環境での操作。CUIは、文字だけでコマンドを実行して操作。になる。LinuxはGUIでもできるが、サーバーでの操作ではCUIが一般的で、指示することをコマンドという。操作が素早くできること、定型処理を自動化しやすいのでコマンド操作が使われる。</dd>
			<dt>端末とは</dt>
			<dd>コンピューターを操作する窓口。昔はコンピューター１台を多数の利用者が合同で利用していた、ディスプレイやキーボードを接続していた。このセットを端末という。GUIにも端末エミュレータがある。広く使われているのがTera Term。</dd>
			<dt>ログインとログアウト</dt>
			<dd>ユーザーを選び、正しくパスワードを入力すると世紀のユーザーであることが認められ、システムを利用できるようになる。これがログイン。その逆が、システムの利用を終了する。ログアウトです。システムを終わらすのはシャットダウンが必要。</dd>
			<dt>ユーザーアカウントとは</dt>
			<dd>
			Linuxシステムに登録されたユーザーのことをユーザーアカウントという。Linuxのユーザーは大きく分けて３種類いる
				<dl>
					<dt>・管理者ユーザー</dt>
					<dd>スーパーユーザー。Linuxシステムでの最高権力。「root」という名前がついてます。</dd>
					<dt>・システムユーザー</dt>
					<dd>システムプログラムやサーバーソフトウェアなどを実行するために用意されるユーザー。Linuxでは、あるユーザーが実行したプログラムはそのユーザーの権限で実行される。</dd>
					<dt>・一般ユーザー</dt>
					<dd>通常のLinux利用者。システムを管理する権限はありません。ユーザーごとに専用の作業場所が与えられ、様々な作業を範囲内でできる。</dd>
				</dl>
			</dd>
			<dt>rootユーザーとは</dt>
			<dd>何でもできるユーザーであるため、一番最初に狙われるのはrootユーザーのパスワード。外部に漏れるとシステムが破壊される。</dd>
			<dt>プロンプトとは</dt>
			<dd>基本的に$の後ろのやつ。rootユーザーなら$が#になる。</dd>
		</dl>
	</dd>

	<dt>2-2	ファイルとディレクトリ</dt>
	<dd>
		<dl>
			<dt>ディレクトリとは</dt>
			<dd>ティレクトリの中にはディレクトリが作れたり、ファイルが作れたりする。ディレクトリの親子関係は「/」で区切って表される</dd>
			<dt>Linuxのディレクトリ構造</dt>
			<dd>Linuxでは、ディレクトリが入れ子状の階層構造になっている。一番最初はルートディレクトリになっている。ルートディレクトリは、「/」で表す。</dd>
			<dt>絶対パスとは</dt>
			<dd>ルートディレクトリを起点としてファイルやディレクトリの場所を表す方法を絶対パスという。</dd>
			<dt>カレントディレクトリとは</dt>
			<dd>ユーザーがいるディレクトリのことをカレントディレクトリという。「現在の」。コマンドpwdにて今いる場所がわかる。</dd>
			<dt>相対パス</dt>
			<dd>カレントディレクトリを起点としてファイルやディレクトリの場所を表す方法を相対パスという。</dd>
			<dt>ホームディレクトリとは</dt>
			<dd>ユーザーがログインすると、カレントディレクトリは「/home/ユーザー」です。この場所をホームディレクトリという。ホームディレクトリは、アクセス権が設定されているので、rootユーザー以外は入れない。</dd>
		</dl>
	</dd>

</dl>

## chapter_3

<dl>
	<dt>3-1	サーバーを公開する</dt>	
	<dd>
		<dl>
			<dt>全体の流れを知ろう</dt>
			<dd>サーバーの準備には、大きく分けて2通りの方法がある。自前サーバーを用意する方法と、レンタルサーバーを契約する方法です。自前の場合、自社に置くのか、データセンターにおくのか、などの選択肢も。さらに、独自ドメインを取得しておく必要がある。</dd>
			<dt>サーバーの準備</dt>
			<dd>サーバーコンピューターを購入する方法と、レンタルサーバーを契約する方法がある。レンタルサーバーの場合は、機材のコストが浮きます。自前だと、サーバー購入、場所など用意する必要がある。通常はデータセンターに預ける形となりますが、データセンターとの契約が必要。</dd>
			<dt>IPアドレスとは</dt>
			<dd>インターネット上でつか荒れる住所がIPアドレス。インターネット接続されたコンピューターが通信するときは、データの送り先や送信元を表すのにIPアドレスを使う。IPアドレスは全世界で重複しないように管理されているので、好きな番号を勝手に使用することはできません。IPアドレスを管理しているのはIANAという組織で、日本ではIANAの配下としてJPNICという団体が日本国内で使われるIPアドレスを管理している。</dd>
			<dt>IPアドレスの種類</dt>
			<dd>勝手に使えるIPアドレスがある。プライベートIPアドレス。これは会社内や家庭内などの構内で自由に利用することができる。それに対して、インターネット上で利用できるIPアドレスがグローバルIPアドレスという。Webサイトなどをインターネット上で公開するにはグローバルIPアドレスを取得する必要がある。</dd>
			<dt>ポート番号</dt>
			<dd>コンピューター同士の通信でも、届け先のコンピューターの何というソフトウェアにデータを届ければよいのかわからなければ、受け取ったコンピューターもわからない。そこで、ポート番号が、IPアドレスと組み合わせて使われる。ファイヤウォールにかからないようにそのポート番号宛が通過できるようせってしなければならない。</dd>
			<dt>ホスト名とは</dt>
			<dd>人にとってはIPアドレスは使い勝手が良くないので、コンピューターに名前をつける。これをホスト名という。</dd>
			<dt>ドメイン名とは</dt>
			<dd>ドメインとは「領域」のことで、「www.example.com」でいうと、「com」という領域にの中にある「example」という領域に存在する「www」という名前のホスト、という意味になる。一番右は、トップレベル・ドメインという。</dd>
			<dt>サーバーの設定</dt>
			<dd>
			サーバーを公開するまでは、いろいろ設定することがある。インターネットに公開する場合適切な設定が必要になる。
				<dl>
					<dt>・コマンドを使って設定する。</dt>
					<dd>古マンドを時効して設定を変更します。サーバーに割り当てるIPアドレス(ifconfig)とか、ただしコマンドを使っての設定の変更は再起動後元に戻ってしまう。</dd>
					<dt>・設定ファイルに設定を記述する</dt>
					<dd>一時的じゃなく永続的に設定を変えるなら設定ファイルを書き換える必要がある。基本文字だけで設定されているのでテキストエディタなどで変更を加える。</dd>
					<dt>・専用の設定ツールを使う</dt>
					<dd>ディストリビューションによっては、設定用の専用ツールが用意されている。しかし、設定ツールは、ティストリビューションによって挙動が違うため意図しない動きをすることがあるであまりよくない。</dd>
				</dl>
			</dd>
		</dl>
	</dd>

	<dt>3-2	ソフトウェアの管理</dt>
	<dd>
		<dl>
			<dt>PCサーバー</dt>
			<dd>見かけや性能がパソコンに近いサーバーをPCサーバーという。見た目は一緒だが、性能や信頼性、可用性を高めるために専用のパーツが使われている。</dd>
			<dt>レンタルサーバー（ホスティング）</dt>
			<dd>サーバーレンタルを行っている事業者と契約してサーバーを借りるのがレンタルサーバーです。事業者がすべてを用意し、利用者がそれを借りることをホスティングという。初期費用や月々のレンタル代がかかるが、最初にサーバーを借りるより、導入コストを抑えることができる。メンテンナンスをしなくて良いというメリットもある。レンタルサーバーには、1台まるごと借りる形態の専用サーバーと、複数の利用者で1台のサーバーを借りる形態の共有サーバーがある。専用サーバーは、高いけど技術的な製薬が小さくなる。共有サーバーは共有している分製薬が大きくなる。</dd>
			<dt>レンタルサーバー</dt>
			<dd>サーバーなどは自前で用意して、業者に設置場所とネットワーク回線を借り受ける形態をハウジングという。サーバーを安全に管理するときに便利。サーバーを自由に選択できるので自分たちにあったものを選べる、社内に置かないのでネットワークや場所を考える必要がない。しかし、申し込んでから時間がかかったりサーバーの増設が難しかったりする。</dd>
			<dt>VPS(Virtual Private Server)</dt>
			<dd>専用サーバーが欲しくてもコストが高い、共有サーバーはできることが限られるなどがあります。そこで、VPSの登場です。1台のサーバーをソフトウェア的に分割して、あたかも複数のサーバーであるかのように使用できる仕組みです。これで低価格で自由にサーバーを利用することができます。</dd>
			<dt>クラウドサーバー</dt>
			<dd>VPSの進化形、仮想化という点では一緒だが、クラウドサーバーの場合必要に応じて容量性能を上げることが可能、予期しないアクセス殺到などに直ちに対応可能。VPSでは仮想サーバー1台ごとに使用料がかかるけど、クラウドは利用した分だけの料金がかかる。</dd>
		</dl>
	</dd>
</dl>

## chapter_4

<dl>
	<dt>4-1	サーバーのポイント</dt>	
	<dd>
		<dl>
			<dt>サーバーの運用とは</dt>
			<dd>サーバーは構築したら終わりではなく、安定的にサービスを提供しなければならない。サーバーの保守・運用です。
				<dl>
					<dt>・リソース管理</dt>
					<dd>サーバーのメモリや、ハードディスク、CPUの処理能力をリソースという。リソースに余裕があるかを確認しないといけない。もしなければ、増設したりする必要がある</dd>
					<dt>・リモート管理</dt>
					<dd>データセンターなどのサーバーとネットワーク経由で管理すること</dd>
					<dt>・バックアップ</dt>
					<dd>番外地データが失われたり壊れた時のために保存しておくのがバックアップ。ハードディスクは壊れやすいので、定期的に別のメディアに保存しておく必要がある。</dd>
					<dt>・ソフトウェアのアップデート</dt>
					<dd>ソフトウェアは常に最新にしておく必要があり、これを怠るとセキュリティ的不具合により、致命的な打撃を受けてしまう可能性がある。</dd>
					<dt>バックアップの考え方</dt>
					<dd>ハードディスクは壊れやすいものなので定期的にバックアップする必要があります。バックアップには、ディスク全体をバックアップするフルバックアップと更新された分だけをバックアップする差分バックアップ、増分バックアップがある。
							<dl>
								<dt>・フルバックアップ</dt>
								<dd>ディスク全体をバックアップすること。ディスクに障害が発生するとバックアップデータを戻すだけでいい。しかし、毎回バックアップするデータがでかいので時間がかかるし、大容量のメディアも必要になる。</dd>
								<dt>・差分バックアップ</dt>
								<dd>フルバックアップ以降に作成されたり更新されたりした部分のデータだけをバックアップすることを言う。バックアップにかかる時間も容量も少なくてすむ。復旧にはフルバックアップのデータと差分バックアップのデータが必要になる。</dd>
								<dt>増分バックアップ</dt>
								<dd>何かのバックアップ以降に作成されたり更新された部分のデータ。バックアップにかかる時間と容量は最小ですむが、復旧の時にフルバックアップに加えてすべての増分バックアップが必要になる。</dd>
								<dt>・バックアップの実際</dt>
								<dd>バックアップの種類を組み合わせることに加えて、どのデータをバックアップするか、ということも重要です。ログファイルだったり〜。ごく小規模ならバックアップコマンドを定期的に実行するだけでも十分。</dd>
								<dt>・バックアップを戻すには</dt>
								<dd>バックアップしたデータを元に戻す作業をリストアという。手順は、不バックアップをリストアし、次に差分バックアップがあればそれをリストア、最後に増分バックアップをリストア。</dd>
							</dl>
					</dd>
				</dl>
			</dd>
		</dl>
	</dd>

	<dt>4-2	ソフトウェアの管理</dt>
	<dd>
		<dl>
			<dt>パッケージとは</dt>
			<dd>Linuxでは、ソフトウェアはパッケージという単位でインストールします。パッケージは大きく分けて2つあり、RPM形式とDebian形式がある。RPMはファイルの拡張子が「.rpm」、Debian形式では「.deb」になる。この2つの互換性はない。ディストリビューションがどちらのパッケージ形式を採用しているかによって、インストール形式を変えなければならない。そして、同じ形式であればどのディストリビューションにもインストールできる、というわけにも行きません。種類やバージョンによってできるものできないものがある。それが自分のものと一致するときのみインストールできる。</dd>
			<dt>パッケージ管理システム</dt>
			<dd>Linuxのソフトウェアを指定してインターネット上からダウンロードし、インストールする仕組み。これには種類があり、パッケージ管理システムでは、インターネット上のリポジトリというパッケージ倉庫からパッケージをダウンロードしてくる。リポジトリには、ティストリビューションの開発者が提供してるものと、それ以外のサードパーティが提供しているものがある。</dd>
		</dl>
	</dd>

	<dt>4-3	現場で役立つLinuxサーバー管理の知識</dt>
	<dd>
		<dl>
			<dt>サービスとは</dt>
			<dd>システムに常駐して利用者や管理者に対して情報を提供するプログラムをサービスという。サービスの管理や、ユーザーの管理、パスワードの管理などをしたりしている。とくに、ログの管理などはしっかり行っていないといざという時大変だったりする。あと、シャットダウンとか。</dd>
		</dl>
	</dd>
</dl>

## chapter_5

<dl>
	<dt>5-1	Linuxにとっての危険</dt>	
	<dd>
		<dl>
			<dt>インターネット上にある危険</dt>
			<dd>インターネットは危険がいっぱいで、ウイルスメール、フィッシング、不正アクセス、サーバーから見ると攻撃の嵐。インターネットに接続し続けるのは常に誰かから習われるということ。
				<dl>
					<dt>・不正侵入</dt>
					<dd>世紀のユーザーではないのに入っちゃう奴。パスワードクラックにより侵入するなりすまし、ソフトウェアの脆弱性をついて利用権限をうばう方法などがある。入られると情報を見られたり、改ざんされたりする。なので、パスワードを複雑に厳重に管理したり、常に最新のソフトウェアにアプデートする。</dd>
					<dt>・Dos/DDoS攻撃</dt>
					<dd>ネットワーク経由で大量のデータを送りつけることによって利用者へのサービスの妨害をすることをDos攻撃。そして、複数のデバイスにウイルスを仕掛けて同時に目標を攻撃することをDDoS攻撃という。完全に防ぐのは難しいけど、攻撃の始まりを検知して、ネットワークを制限するソフトウェアやファイアウォール製品がある。</dd>
					<dt>トロイの木馬</dt>
					<dd>インターネット上からダウンロードしたソフトウェアをインストールすると、中に潜ませていた悪意あるプログラムまで一緒にインストールされる「トロイの木馬」。公式配布元サーバーでもまれに差し替えられることがある。出処が怪しいところはインストールせず、パッケージ管理システムを使ってのみインストールする、と言った対策が必要。</dd>
					<dt>最新でないソフトウェアは危険</dt>
					<dd>ソフトウェアにはどうしても不具合が紛れ込んでいる。不具合があると修正します。アップデートが公開されたら、直ちにアップデートすることが大事。セキュリティ情報に注意して情報収集しておくと良い。アップデートをしない場合、その不具合を利用した攻撃が増える。手当たりしだいなのでいつ自分に来るか分かんない。</dd>
					<dt>サーバー管理者が招く危険</dt>
					<dd>サーバーのセキュリティが破られる原因を管理者自らが作ってしまっていることがある。サーバーの設定など。緩めて設定したそのママにしてしまっている、自分が理解しないままインターネット上の設定を利用するなど。利便性重視で設定変えたりもするけど、安全のためにやらなければいけないことなどの見極めなどがサーバー管理者に求められる。</dd>
					<dt>Linuxサーバーが乗っ取られたら？</dt>
					<dd>情報漏れたり、全部消されたり。攻撃者は侵入しても管理者にバレないよう身を隠し他のサーバーへの攻撃の準備をすすめるこれを踏み台という。攻撃が終われば攻撃者は痕跡を消し逃亡します。いつの間にか加害者はサーバー管理者になるのです。IDS、IPSいれようね。</dd>
				</dl>
			</dd>
		</dl>
	<dt>5-2	知っておきたいセキュリティ技術</dt>
	<dd>
		<dl>
			<dt>パーミッション</dt>
			<dd>Linuxではファイルやディレクトリにパーミッションが設定されている。rootユーザー以外はパーミッションに従って許可された操作しかできないようになっている。サーバーの設定がうまく行かない時設定をゆるくしてそのままにしてしまうケースよくあります。それに気づかれたら踏み台にされたりする。なので、権限は必要最小限にする。</dd>
			<dt>暗号化技術</dt>
			<dd>Linuxでは、ネットワーク通信を暗号化するための様々な技術が使える。
				<dl>
					<dt>・SSL/TLS</dt>
					<dd>主にWebブラウザとWebサーバーの通信を暗号化するために使われます。</dd>
					<dt>・SSL/TLSサーバー証明書</dt>
					<dd>サーバーの認証機能。Webブラウザが接続してるのは本物かどうかを確認できる機能。この機能を利用するには、サーバー証明書を予め取得して置かなければならない。事業者によって異なるが、年額数万円程度の費用がかかる。</dd>
					<dt>・SSH</dt>
					<dd>ネットワーク経由でLinuxサーバーにログインしたり、安全にファイルをコピーしたりするのに使う。ほとんどのディスりビューションがOpenSSH、ファイルの転送にも使えるよ。</dd>
					<dt>・SFTP/FTPS</dt>
					<dd>ファイルを転送するFTP通信は、暗号化されていません。SSHを使って安全な通信をするのがSFPS、SSL/TLSを使って安全に対応したのがFTPS。</dd>
					<dt>ファイヤウォール</dt>
					<dd>ネットワーク上で流れる情報はパケットという単位で分割される。システムに入ってくるパケットや出て行くパケットを調べ、条件によってパケットを遮断する仕組みがファイヤウォール。Linuxは、標準的にファイヤウォールが動作している。</dd>
					<dt>SELinux</dt>
					<dd>万が一侵入された時のために被害を最小に留めるためのもの。正直標準で有効になっている分邪魔しかしてこないイメージだが、メリットを考えるとでかい存在なのでしっかり考えたほうがよい</dd>
				</dl>
			</dd>
		</dl>
	</dd>

	<dt>5-3	サーバーに求められるセキュリティ対策</dt>
	<dd>
		<dl>
			<dt>ログインを制限する</dt>
			<dd>sshのポート番号の設定を変えれば知っている人しかアクセスできなくなる。もうひとつが、rootユーザーによるログイン禁止にして通常は一般でログインして、権限が必要なときはsuとかを使えばいい。</dd>
			<dt>開いているポートを確認する</dt>
			<dd>もし管理者が気づかないうちに、不要なサービスが稼働していることがあるかも、必要最小限にする少しでもインシデントを防ぐため。</dd>
		</dl>
	</dd>
</dl>

## chapter_6

<dl>
	<dt>6-1	管理者が知っておきたい基本操作</dt>	
	<dd>
		<dl>
			<dt>サーバーの基本情報を確認する</dt>
			<dd>サーバーを引き継いだ時、まず基本情報を知ることから始まる。コマンドを使って、基本情報シートを作る。</dd>
			<dt>ユーザーを追加する</dt>
			<dd>rootでいるのは危険。なのでユーザーと作る。</dd>
			<dt>ファイル名入力の手間を省く</dt>
			<dd>Tab使おうね</dd>
			<dt>以前に実行したコマンドを再実行する</dt>
			<dd>historyみようね<br />とか思ったけど!履歴番号とかいみはわかるけど知らなかったいいこと知った。</dd>
			<dt>ファイルを検索する</dt>
			<dd>ファイルの場所を検索するlcoate、1日1回ファイル名の一覧データベースを作成しているらしい。find使えばもっと詳しく条件を絞り込めるらしい。</dd>
			<dt>マニュアルを検索する</dt>
			<dd>manとか何書いてるとか理解するの大変だけど読めたら超便利なことも知っている。</dd>
			<dt>ログファイルをバックアップする</dt>
			<dd>/var/logをまるごと圧縮してscpで転送して、名前の付け方は日時などわかる上に重複しないものにし保存すること。</dd>
			<dt>システムを自動的にアップデートする</dt>
			<dd>CentOSでは、yum-cronパッケージをインストールすることでいちいち管理者がアップデートかける必要がない。サービス実行して、自動起動音で終わり。</dd>
		</dl>
	</dd>

	<dt>6-2	トラブルに対処する</dt>
	<dd>
		<dl>
			<dt>コマンドが実行できない</dt>
			<dd>マニュアル通りコマンド実行してもエラー、よくあります。代表的、スペルミス。tabつかいましょう。だいたい「No such file or directory」がでる。「Permission denied」とかの権限のエラーもある。</dd>
			<dt>パスワードを忘れた</dt>
			<dd>一般ユーザーがパスワードを忘れるとrootユーザーにもわからないのでpasswdで再設定する必要がある。</dd>
			<dt>rootユーザーのパスワードがわからない</dt>
			<dd>きました。rootユーザーの場合。もしsudoコマンドでrootユーザーの全コマンドが使えるのなら一般ユーザーからrootユーザーになる。でpasswd。もしsudoコマンドが使えるユーザーがいない場合。システムをシングルユーザーモードで起動すれば、通常パスワード無しでrootユーザーとしてログインできる。</dd>
			<dt>インターネットに繋がらない</dt>
			<dd>まずネットワークが有効になっているかどうかを調べる。大丈夫だったらifconfigみる、大丈夫だったら、pingで通信テストpingで通信ができるときはファイアウォールが怪しいらしい。次、iptables、ファイヤウォールが設定されている場合一度無効にして通信ができればファイヤウォールを無効にするのではなく設定を変える。</dd>
			<dt>SSHで接続できない</dt>
			<dd>原因
				<ul>
					<li>サーバーがダウンしている</li>
					<li>サーバーまでのネットワークに不具合が発生してる</li>
					<li>ファイヤウォールで遮られている</li>
					<li>SSHサーバーが稼働してない</li>
					<li>SSHのポート番号が変更されている</li>
				</ul>
				まずpingでサーバーに大して実行して返ってくるか試す。ない場合、サーバーかネットワークの問題ファイヤウォールの可能性もある。	
			</dd>
			<dt>Webサーバーが応答しない</dt>
			<dd>サーバーへのネットワーク接続に問題がなければnetstatで開いてるポートを確認する。80番ポートが表示されない場合サーバーが稼働してるか確認する。あと、error_logをみよう。</dd>
		</dl>
	</dd>

	<dt>6-3	viエディタを使ってみる</dt>
	<dd>
		<dl>
			<dt>viエディタとは</dt>
			<dd>
				<dl>
					<dt>2つのモード</dt>
					<dd>コマンドモードと挿入モード、これを駆使して戦う。</dd>
					<dt></dt>
				</dl>
			</dd>
		</dl>
	</dd>
</dl>

## Impressions  

しっかり基礎的なことを解説されていて、なぜこれをやってはいけないのかや問題の解決方法を細かく説明されていた。基礎を思い出したい時とか、問題解決とかたまに読み返したい。

