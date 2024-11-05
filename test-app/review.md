# PHP App ① レビュー

## 全般

### 以下のaタグのリンクを押下した際にedit.phpの$_GETにどんな値が格納されるか説明してください。

```html
<a href="edit.php?todo_id=123&todo_content=焼肉">更新</a>
```

### 以下のフォームの送信ボタンを押下した際にstore.phpの$_POSTにどんな値が格納されるか説明してください。

```html
<form action="store.php" method="post">
    <input type="text" name="id" value="123">
		<textarea　name="content">焼肉</textarea>
    <button type="submit">送信</button>
</form>
```
id => １２３
### `require_once()` は何のために記述しているか説明してください。
()中に記載あるものを読み込み、中に記載あるものが使用可能になる
### `savePostedData($post)`は何をしているか説明してください。

### `header('location: ./index.php')`は何をしているか説明してください。
 header関数を用いてリダイレクト先を指定しているので、index.php に遷移する。
### `getRefererPath()`は何をしているか説明してください。
絶対パスを取得する
### `connectPdo()` の返り値は何か、またこの記述は何をするための記述か説明してください。
定数のDSN, DB_USER, DB_PASSWORD 
PDOという定義済みのクラスをインスタンス化する。
### `try catch`とは何か説明してください。
例外処理という処理を実装する際に使用。
try｛｝の中に例外が発生する可能性がある処理を書く
throw new Exceptionで例外を発生させる
例外が発生するとcatch ｛｝ の中の処理が行われる。
### Pdoクラスをインスタンス化する際に`try catch`が必要な理由を説明してください。
DBに正常に接続されなかった場合に、エラー文にDBの情報が表示されるから。
## 新規作成

### `createTodoData($post)`は何をしているか説明してください。
POSTで送信されたデータをDBへ保存する処理にデータを渡す。
## 一覧

### `getTodoList()`の返り値について説明してください。
getallrecords（）の返り値。
todosテーブルから、削除されていないレコードを全件配列で取得したもの。
### `<?= ?>`は何の省略形か説明してください。
<?php echo  ?>

## 更新

### `getSelectedTodo($_GET['id'])`の返り値は何か、またなぜ`$_GET['id']` を引数に渡すのか説明してください。

### `updateTodoData($post)`は何をしているか説明してください。

## 削除

### `deleteTodoData($id)`は何をしているか説明してください。

### `deleted_at`を現在時刻で更新すると一覧画面からToDoが非表示になる理由を説明してください。

### 今回のように実際のデータを削除せずに非表示にすることで削除されたように扱うことを〇〇削除というか。

### 実際にデータを削除することを〇〇削除というか。

### 前問のそれぞれの削除のメリット・デメリットについて説明してください。


