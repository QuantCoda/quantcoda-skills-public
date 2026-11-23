# index_weight — 指数成分与权重

**所需套餐**：PRO 及以上

## SDK 方法

```python
qc.index_weight(symbol=None, con_symbol=None, start_date=None, end_date=None, trade_date=None)
```

返回 `pandas.DataFrame`；无数据时返回空 DataFrame。

## 参数

| 参数 | 说明 |
|---|---|
| `symbol` | 指数代码（带后缀），如 000300.SH |
| `con_symbol` | 成分证券代码（带后缀），如 000001.SZ |
| `start_date` | 起始日期 YYYYMMDD |
| `end_date` | 结束日期 YYYYMMDD |
| `trade_date` | 单个交易日 YYYYMMDD（与 start/end 二选一） |

## 返回字段

| 字段 | 说明 |
|---|---|
| `symbol` | 指数代码 |
| `trade_date` | 交易日期 |
| `con_symbol` | 成分股代码 |
| `con_name` | 成分股名称 |
| `weight` | 权重(%) |

## 示例

```python
df = qc.index_weight(symbol='000300.SH')
print(df.head())
```
