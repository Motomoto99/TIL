# オブジェクトについて

## 目次
- オブジェクトの初期化
- オブジェクトから値を取得・変更
  - ドット記法
  - ブランケット記法
- プロパティの削除

## オブジェクトの初期化
```
let obj = {
    strProp: "文字列",
    intProp: {
        subProp: "値",
    },
    intProp: 456,
    boolProp: false,
}
```
{~}のことをオブジェクトリテラルっていうらしい。文字列リテラルとかと同じ感じか。  
### 留意点
- プロパティと値は「:」で区切る
- プロパティと値のペア同士は「,」で区切る
- 値はどのデータ型の値でも可能
- オブジェクトの中にオブジェクトを設定することも可能
- 同じプロパティ名が重複した場合は、後に定義した方で上書きされる

## オブジェクトから値を取得・変更
二つの種類がある
### ・ドット記法
オブジェクト名.プロパティ名
```
//オブジェクトpersonのオブジェクトnameのプロパティlastの値を出力
console.log(person.name.last);

//オブジェクトpersonのオブジェクトnameのプロパティlastの値を変更
person.name.last = "次郎";

//オブジェクトpersonにプロパティgenderとその値を追加
person.gender = "男";

//オブジェクトpersonにオブジェクトfamilyとそのプロパティと値のペアを追加
person.family = {wife: "花子", child: "三郎"};
```

### ・ブランケット記法
オブジェクト["プロパティ名"]
```
//オブジェクトpersonのプロパティageの値を出力
console.log(person["age"]);

//オブジェクトpersonのオブジェクトnameのプロパティlastの値を出力
console.log(person["name"]["last"]);

//オブジェクトpersonのオブジェクトnameのプロパティlastの値を変更
person["name"]["last"] = "次郎";

//オブジェクトpersonにプロパティgenderとその値を追加
person["gender"] = "男";

//オブジェクトpersonにオブジェクトfamilyとそのプロパティと値のペアを追加
person["family"] = {wife: "花子", child: "三郎");

//オブジェクトのプロパティの名前に定数や変数を挿入できるってことかな。
const keyBase = "member";
let member = {
    [ keyBase + "1"] : "太郎",
    [ keyBase + "2"] : "次郎"
}
console.log(member);
⇒{ member1: "太郎" , member2: "次郎"}
```

## プロパティの削除
delete オブジェクト名.プロパティ名;

