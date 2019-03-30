# RPG Object (playerなど)
## 属性(取得設定可能)
- `damage` 属性(非負整数): ふれたとき与えるダメージ
- `atk` 属性(非負整数): 攻撃力
- `hp` 属性(整数): HP
- `money` 属性(非負整数またはundefined): 持っているお金
- `speed` 属性(正の数): 移動速度
- `opacity` 属性(0以上1以上の数): 透明度(0で全透明)
- `collideMapBoader` 属性(真偽値): 端に触れても動き続けるか
- `showHpLabel` 属性(真偽値): HPを表示するか
- `isAutoPickUp` 属性(真偽値): アイテムを自動で拾うか

## 属性(取得専用)
- `mapX` 属性(非負整数): マップ上でのX座標
- `mapY` 属性(非負整数): マップ上でのY座標

## 関数
### locate(xpos: 非負整数, ypos: 非負整数, 任意:map:文字列)
X/Y座標を指示されたとおりに変更し、mapが指定されていればmapを変更する。

### destroy(任意:delay: 非負整数)
delay秒後に(なければすぐ)オブジェクトを破壊(死亡など)する。

### await attack()
攻撃する。スキルがあれば召還する。

### walkLeft()
左に歩く。

### walkRight()
右に歩く。

### shoot(node: RPGObject, 任意:vector:座標が入った配列, 任意:speed:自然数)
RPGObjectを与えられた場所へ与えられた速さで撃つ。
