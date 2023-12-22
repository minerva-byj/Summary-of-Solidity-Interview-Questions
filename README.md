# Summary-of-Solidity-Interview-Questions
https://mp.weixin.qq.com/s/5xdNTCXrOSm0qwtqLCx30g

针对这个写了一份我自己的答案，有错误还请指正，附上参考链接
# Solidity 面试问题汇总

# **简单题**

1. 私有、内部、公共和外部函数之间的区别？
    - `public`修饰符可以从合约内外访问。
    - `private`修饰符仅在当前合约内部访问。
    - `internal`修饰符可以在当前合约内部和继承合约中访问。
    - `external`修饰符仅供其他合约调用，不能在当前合约内部直接调用。
    
    参考：[https://juejin.cn/post/7229213845947531325](https://juejin.cn/post/7229213845947531325)
    
2. 智能合约大小大约可以有多大？
3. create 和 create2 之间有什么区别？
4. Solidity 0.8.0 **[6]**版本对算术运算有什么重大变化？
5. 代理需要哪种特殊的 CALL 才能工作？
6. 在 EIP-1559 之前，如何计算以太坊交易的美元成本？
7. 在区块链上创建随机数的挑战是什么？
8. 荷兰式拍卖和英式拍卖之间有什么区别？
9. ERC20**[7]** 中的 transfer 和 transferFrom 之间有什么区别？
10. 对于地址 allowlist，使用映射还是数组更好？为什么？
11. 为什么不应该使用 tx.origin 进行身份验证？
12. 以太坊主要使用什么哈希函数？
13. 1 个Ether 相当于 多少个 gwei ？
14. 1 个Ether 相当于 多少个 wei ？
15. assert 和 require 之间有什么区别？
16. 什么是闪电贷？
17. 什么是检查效果（ check-effects ）模式？
18. 运行独立验证节点所需的最小以太数量是多少？
19. fallback 和 receive 之间有什么区别？
20. 什么是重入？
21. 上海升级后，每个区块的 gas 限制是多少？
22. 什么阻止无限循环永远运行？
23. tx.origin 和 msg.sender 之间有什么区别？
24. 如何向没有payable 函数、receive 或回退的合约发送以太？
25. view 和 pure 之间有什么区别？
26. ERC721**[8]** 中的 transferFrom 和 safeTransferFrom 之间有什么区别？
27. 如何将 ERC1155**[9]** 代币转换为非同质化代币？
28. 访问控制是什么，为什么重要？
29. 修饰符（modifier）的作用是什么？
30. uint256 可以存储的最大值是多少？
31. 什么是浮动利率和固定利率？

# **中等难度**

# **有难度题**

# **高难度题**
