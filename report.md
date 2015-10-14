## 課題解答

### その1
#### 変更内容
hello_trema.rb に以下のハンドラを追加

```ruby
def switch_disconnected(datapath_id)
  logger.info "Bye #{datapath_id.to_hex} "
end
```
#### 動作説明
スイッチが切断されたら「switch_disconnected()」が呼び出される．
その際に停止したスイッチのIDを出力する．

### その2
#### 変更内容
hello_trema.rb の「start」ハンドラを以下のように変更

```ruby
def start(_args)
  puts "#{self.class.name} started."
end
```

#### 動作説明
コントローラが起動したら「start」が呼び出される．
その際に自身のクラス名を動的に取得して表示する．
