Ruby 基礎
====================================================================

Install
--------------------------------------------------------------------

### USE ###

 * (Ruby)[http://www.ruby-lang.org/ja/]
 * (git)[http://git-scm.com/]
 * (rbenv)[https://github.com/sstephenson/rbenv/]
 * (ruby-build)[https://github.com/sstephenson/ruby-build]

### Why do you use ###

 Ruby の現在(2013/03)の最新版は 2.0 ですがデファクトスタンダードは 1.9.3 です。
 開発するプロダクトによってバージョンを替える必要があったり新しく出たパッチを試す時など
 複数のバージョンをインストールしたくなります。
 それを実現するエコシステムが rbenv と ruby-build です。

 ruby-build は様々な ruby のバージョンや処理系のビルドをサポートし、rbenv はそれを閉じた環境で構築します。

### 事前準備 ###

#### リポジトリのアップデート ####

Ubuntu/Dbian:

```shell
 $ sudo apt-get update
```

CentOS/Redhat:

```shell
 $ sudo yum update
```

#### 開発ライブラリのインストール ####

Ubuntu/Debian:

```shell
 $ sudo apt-get install build-essential bison openssl libreadline6 libreadline6-dev curl
 $ sudo apt-get install zlib1g zlib1g-dev libssl-dev libyaml-dev libxml2-dev autoconf
 $ sudo apt-get install libc6-dev ncurses-dev automake libtool libssl-dev libsqlite3-dev
```

CentOS/Redhat:

```shell
 $ sudo yum groupinstall "Development Tools"
```

#### Git のインストール ####

Ubuntu/Debian:

```shell
 $ sudo apt-get install git
```

CentOS/Redhat:

```shell
 $ sudo yum install git
```

### rbenv のインストール ###

Ubuntu/Debian CentOS/Redhat

```shell
 $ git clone git://github.com/sstephenson/rbenv.git ~/.rbenv
 $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
 $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
 $ exec $SHELL -l
```

### ruby-build のインストール ###

Ubuntu/Debian CentOS/Redhat

```shell
 $ git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
```

### Ruby 2.0 のインストール ###

Ubuntu/Debian CentOS/Redhat

```shell
 $ rbenv install 2.0.0-p0
 $ rbenv global 2.0.0-p0
```

### Check ###

確認してみましょう。

```shell
 $ ruby -v
   ruby 2.0.0p0 (2013-02-24 revision 39474) [x86_64-linux]
```
