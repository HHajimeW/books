# Spring 解体新書

## 7章 Spring AOP

***

### 7.1 AOPの概要
* AOPとは？ \
AOPとは、アスペクト指向プログラミングの略称。 \
各クラスで共通する処理を抜き出して、まとめて管理する。

* AOPの用語 \
Advice：AOPで実行する処理のこと \
Pointcut：処理を一考する場所（クラスやメソッド）のこと \
JoinPoint：処理を実行するタイミングのこと

* JoinPointの種類 

|タイミング|説明|
|---|---|
|Before|メソッドが実行される前に、AOPの処理（Advice）を実行|
|After|メソッドが実行されたあとに、AOPの処理（Advice）を実行|
|AfterReturning|メソッドが正常終了した場合だけ、AOPの処理（Advice）を実行|
|Around|メソッド実行の前後に、AOPの処理（Advice）を実行|
|AfterThrowing|メソッドが異常終了した場合だけ、AOPの処理（Advice）を実行|

* AOP内部の仕組み \
まず、DIコンテナに登録されているBeanのメソッドを呼び出そうとする。Beanのメソッドを直接呼び出さず、Proxyが自動生成され、Proxy経由でBeanのメソッドが呼び出されるBeanのメソッドを呼び出す前後にAdvice（AOPの処理）を実行する

### 7.2 開発の準備
pom.xml の更新

### 7.3 AOPの実装

* Pointcutの指定方法

|Pointcut|説明|
|---|---|
|execution|正規表現を使って任意のクラス、メソッドなどをAOPの対象に指定|
|bean|DIコンテナに登録されているBean名でAOPの対象に指定|
|@annotation|アノテーション名で指定。指定したアノテーションがついているメソッドがAOPの対象。|
|@within|アノテーション名で指定。指定したアノテーションがついているクラスのすべてのメソッドがAOPの対象。|
|AfterThrowing|メソッドが異常終了した場合だけ、AOPの処理（Advice）を実行|

### 7.4 まとめ

## 8章 SpringJDBC

***

### 8.1 SpringJDBCとは
通常のJDBCより実装が簡単にできるやつ

### 8.2 開発前の準備

### 8.3 JdbcTemplate の実装

### 8.4 NamedParameterJdbcTemplate の実装

### 8.5 トランザクション
トランザクションを使うには @Transactional アノテーション

## 9章 例外ハンドリング