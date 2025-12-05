```mermaid
graph LR
    %% ノードの定義（わかりやすく先に定義します）
    List["/idvlist<br/>**キャラクター一覧**"]
    Detail["/idvlist/:number<br/>**詳細表示**"]
    Edit["/idvlist/edit/:number<br/>**編集**"]
    Update["/idvlist/update/:number<br/>**更新処理**"]
    New["/idvlist/create<br/>**新規登録**"]
    Newedit["post /idvlist<br/>**新規登録処理**"]
    Delete["idvlist/delete/:number<br/>**削除処理**"]



    %% 遷移の定義
    List --> Detail
    Detail --> List
    Detail --> Edit
    Edit --> Detail
    Edit --> Update
    Update --> List
    List --> New
    New --> List
    New --> Newedit
    Newedit --> List
    List --> Delete
```