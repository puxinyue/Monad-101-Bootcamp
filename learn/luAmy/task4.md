## 第四章：Web3 前端 101

1. 完成课程的实操后，请思考如何监听合约事件；当有别人购买了像素格子的时候，如何及时通过监听事件更新 UI ? 请提交示例代码

```javascript
// 读取合约
  let result = useReadContract({
    abi: ABI,
    address: contractAddress,
    functionName: 'getEarths',
  })
  console.log(result)

  // 监听
  useWatchBlockNumber({
    onBlockNumber(blockNumber) {
      result.refetch()
      setSelectedTile(null)
      console.log('Block number changed!', blockNumber)
    },
  })
```

