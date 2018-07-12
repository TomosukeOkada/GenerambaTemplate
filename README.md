# これは何？
Xcode用コードジェネレータ[Generamba](https://github.com/rambler-digital-solutions/Generamba)のためのテンプレートです。  
現在、VIPERモジュール用とMVPのPresentation層用の２つがあります。  
VIPERの命名や構成は[こちら](https://github.com/pedrohperalta/Articles-iOS-VIPER)に沿っています。

## my_viper_viewController(VIPERモジュール(UIViewController)生成) ← Add Xcode9.4 support.
Contract, View, Presenter, Interactor, Routerを生成します。  
詳細は中身を見てください:stuck_out_tongue_winking_eye:

## my_viper_view(VIPERモジュール(UIView)生成) ← Add.
Contract, View, Presenter, Interactor, Routerを生成します。  
詳細は中身を見てください:stuck_out_tongue_winking_eye:

## my_presentation(MVPのPresentationモジュール生成)
View, Presenter, Builder, Wireframeを生成します。  
詳細は中身を:stuck_out_tongue_closed_eyes::stuck_out_tongue_closed_eyes:

# 使い方(git)
1) プロジェクトのルートディレクトリで`generamba setup`
2) `Rambafile`のテンプレートの部分を以下のように変更

```
### Templates
catalogs:
- 'https://github.com/TomosukeOkada/GenerambaTemplate'
templates:
- {name: my_viper_viewController} # 使いたいテンプレートを選択
- {name: my_viper_view} # 使いたいテンプレートを選択
- {name: my_presentation} # 使いたいテンプレートを選択
```

3) `generamba template install`でテンプレートを導入
4) `generamba gen [モジュール名] [テンプレート名]`でモジュールを作れます

# 使い方(ファイル)
1) プロジェクトのルートディレクトリで`generamba setup`
2) このリポジトリの`my_viper_viewController`、`my_viper_view`または`my_presentation`ディレクトリを適当な場所に配置
3) `Rambafile`のテンプレートの部分を以下のように変更

```
### Templates
templates:
- {name: my_viper_viewController, local: '/絶対パス/my_viper_viewController/'} # 使いたいテンプレートを選択
- {name: my_viper_view, local: '/絶対パス/my_viper_view/'} # 使いたいテンプレートを選択
- {name: my_presentation, local: '/絶対パス/my_presentation/'} # 使いたいテンプレートを選択
```

4) `generamba template install`でテンプレートを導入
5) `generamba gen [モジュール名] [テンプレート名]`でモジュールを作れます
