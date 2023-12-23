# Summary-of-Solidity-Interview-Questions
https://mp.weixin.qq.com/s/5xdNTCXrOSm0qwtqLCx30g

针对这个写了一份我自己的答案，有错误还请指正，附上参考链接

欢迎打赏转发

0x7F9d8D2c7e4B63f7947768bAF4cfBa93D090ACd7

# Solidity 面试问题汇总

# **简单题**

1. 私有、内部、公共和外部函数之间的区别？
    - `public`修饰符可以从合约内外访问。
    - `private`修饰符仅在当前合约内部访问。
    - `internal`修饰符可以在当前合约内部和继承合约中访问。
    - `external`修饰符仅供其他合约调用，不能在当前合约内部直接调用。
    
    参考：[https://juejin.cn/post/7229213845947531325](https://juejin.cn/post/7229213845947531325)
    
2. 智能合约大小大约可以有多大？
    
    智能合约最大可达 24 KB，否则会消耗完燃料。 可以使用[钻石模式](https://eips.ethereum.org/EIPS/eip-2535)来规避它。
    
    参考：[智能合约简介 | ethereum.org](https://ethereum.org/zh/developers/docs/smart-contracts/#limitations)
    
3. create 和 create2 之间有什么区别？
    
    在以太坊区块链中，`create` 和 `create2` 都是用来创建新的合约实例的指令，它们之间的主要区别在于合约地址的生成方式和可预测性。
    
    具体来说，`create` 指令会在区块链上创建一个新的合约实例，并使用一个随机的地址作为合约地址。这意味着每次执行 `create` 指令时，都会创建一个不同的地址，并且该地址是不可预测的。这种方式有时可能会导致一些问题，例如如果多个合约在同一块区块上被创建，它们的地址可能会发生碰撞，从而导致一些难以预测的问题。
    
    相比之下，`create2` 指令允许合约的创建者指定一个“salt”（盐），并使用这个 salt 和创建者地址作为参数，生成一个可预测的地址。这意味着在相同的 salt 和创建者地址下，每次执行 `create2` 指令都会生成相同的地址，从而避免了地址碰撞的问题。这也使得 `create2` 更容易进行合约地址的预测和计算，因为我们可以事先知道在给定的 salt 和创建者地址下，合约的地址将是什么。
    
    因此，`create2` 的主要优点是它提供了更可预测的合约地址生成方式，从而使得合约的创建更加稳定和安全。当然，在某些情况下，如需要随机性或避免地址被公开的情况下，使用 `create` 也是可以的。
    
    参考：[create create2区别-掘金 (juejin.cn)](https://juejin.cn/s/create%20create2%E5%8C%BA%E5%88%AB)
    
4. Solidity 0.8.0版本对算术运算有什么重大变化？
    
    0.8.0版本开始，算术运算有两个计算模式，一个是“wrapping”（截断）模式或为“unchecked”（不检查）模式，即在发生溢出的情况下会进行“截断”，不会触发失败异常，从而得靠引入额外的检查库来解决这个问题（如OpenZeppelin中的SafeMath库）；另一个是"checked"（检查）模式。默认情况下，算术运算使用的是“checked”模式，会进行溢出检查，如果结果溢出，会出现失败异常回退。

   参考：[https://blog.csdn.net/ling1998/article/details/125550140](https://blog.csdn.net/ling1998/article/details/125550140)
    
6. 代理需要哪种特殊的 CALL 才能工作？
7. 在 EIP-1559 之前，如何计算以太坊交易的美元成本？
8. 在区块链上创建随机数的挑战是什么？
9. 荷兰式拍卖和英式拍卖之间有什么区别？
10. ERC20**[7]** 中的 transfer 和 transferFrom 之间有什么区别？
11. 对于地址 allowlist，使用映射还是数组更好？为什么？
12. 为什么不应该使用 tx.origin 进行身份验证？
13. 以太坊主要使用什么哈希函数？
14. 1 个Ether 相当于 多少个 gwei ？
15. 1 个Ether 相当于 多少个 wei ？
16. assert 和 require 之间有什么区别？
17. 什么是闪电贷？
18. 什么是检查效果（ check-effects ）模式？
19. 运行独立验证节点所需的最小以太数量是多少？
20. fallback 和 receive 之间有什么区别？
21. 什么是重入？
22. 上海升级后，每个区块的 gas 限制是多少？
23. 什么阻止无限循环永远运行？
24. tx.origin 和 msg.sender 之间有什么区别？
25. 如何向没有payable 函数、receive 或回退的合约发送以太？
26. view 和 pure 之间有什么区别？
27. ERC721**[8]** 中的 transferFrom 和 safeTransferFrom 之间有什么区别？
28. 如何将 ERC1155**[9]** 代币转换为非同质化代币？
29. 访问控制是什么，为什么重要？
30. 修饰符（modifier）的作用是什么？
31. uint256 可以存储的最大值是多少？
32. 什么是浮动利率和固定利率？

# **中等难度**

# **有难度题**

# **高难度题**
