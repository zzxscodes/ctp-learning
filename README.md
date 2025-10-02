reference
https://www.zhihu.com/column/iQuant
				
https://zhuanlan.zhihu.com/p/23015492

https://zhuanlan.zhihu.com/p/23132875

https://zhuanlan.zhihu.com/p/23202005

https://zhuanlan.zhihu.com/p/23293035

https://zhuanlan.zhihu.com/p/23574721

https://zhuanlan.zhihu.com/p/24077002

https://zhuanlan.zhihu.com/p/25357050

https://blog.csdn.net/baidu_37097818/category_12646495.html
				
https://blog.csdn.net/baidu_37097818/article/details/137823763

https://blog.csdn.net/baidu_37097818/article/details/137863824

https://blog.csdn.net/baidu_37097818/article/details/137864936

https://blog.csdn.net/baidu_37097818/article/details/137875711

https://blog.csdn.net/baidu_37097818/article/details/137913588

https://blog.csdn.net/baidu_37097818/article/details/137915441

https://blog.csdn.net/baidu_37097818/article/details/137919365

https://blog.csdn.net/baidu_37097818/article/details/138315903

https://blog.csdn.net/baidu_37097818/article/details/146186082

https://blog.csdn.net/baidu_37097818/article/details/148278951


行情和交易API中的TradingDay交易日规则是怎样的？
如何确定订单的唯一性？换而言之，如何撤单？
如何将成交和订单关联起来？
查询合约手续费率为什么返回品种代码？
各个交易所的持仓的平仓顺序是什么？


https://blog.csdn.net/a642960662/category_11641151.html
				
https://quantfabric.blog.csdn.net/article/details/126751263

https://quantfabric.blog.csdn.net/article/details/123028632

https://quantfabric.blog.csdn.net/article/details/123028659

https://quantfabric.blog.csdn.net/article/details/123028692

https://quantfabric.blog.csdn.net/article/details/123028727

https://quantfabric.blog.csdn.net/article/details/123028768

https://quantfabric.blog.csdn.net/article/details/123028794

https://quantfabric.blog.csdn.net/article/details/123028849

https://quantfabric.blog.csdn.net/article/details/123027836

https://quantfabric.blog.csdn.net/article/details/123027939

https://quantfabric.blog.csdn.net/article/details/123027981

https://quantfabric.blog.csdn.net/article/details/123027996

https://quantfabric.blog.csdn.net/article/details/123028074

https://quantfabric.blog.csdn.net/article/details/123028152

https://quantfabric.blog.csdn.net/article/details/123028207

https://quantfabric.blog.csdn.net/article/details/123028251

https://quantfabric.blog.csdn.net/article/details/123028354

https://quantfabric.blog.csdn.net/article/details/123028370

https://quantfabric.blog.csdn.net/article/details/123028405

https://quantfabric.blog.csdn.net/article/details/123028447

https://quantfabric.blog.csdn.net/article/details/123028479


订单类型
1、LIMIT
2、FAK 立即成交和撤销指令，订单在指定价价格成交，且剩余订单自动被交易所撤消
3、FOK 立即全部成交否则自动撤销指令
4、MARKET

CTP6.3.15
# ThostFtdcMdApi.h

## 回调函数

* OnFrontConnected 行情前置连接成功（未登录前触发）
* OnFrontDisconnected 行情前置连接断开
* OnHeartBeatWarning 心跳超时报警
* OnRspUserLogin 行情登录应答
* OnRspUserLogout 行情登出应答
* OnRspError 行情接口错误应答
* OnRspSubMarketData 订阅行情应答
* OnRspUnSubMarketData 取消订阅行情应答
* OnRspSubForQuoteRsp 订阅询价应答
* OnRspUnSubForQuoteRsp 取消订阅询价应答
* OnRtnDepthMarketData 深度行情推送
* OnRtnForQuoteRsp 询价响应推送

## 查询函数

* CreateFtdcMdApi 创建行情 API 实例（可指定 UDP/组播模式）
* GetApiVersion 获取 API 版本号
* Release 释放接口对象
* Init 初始化并启动线程
* Join 阻塞等待线程结束
* GetTradingDay 获取当前交易日
* RegisterFront 注册行情前置机地址
* RegisterNameServer 注册名字服务器地址
* RegisterFensUserInfo 注册 Fens 用户信息
* RegisterSpi 注册回调接口实例
* SubscribeMarketData 订阅行情
* UnSubscribeMarketData 取消订阅行情
* SubscribeForQuoteRsp 订阅询价
* UnSubscribeForQuoteRsp 取消订阅询价
* ReqUserLogin 行情登录请求
* ReqUserLogout 行情登出请求

# ThostFtdcTraderApi.h

## 回调函数

* OnFrontConnected 连接成功回调（未登录前触发）
* OnFrontDisconnected 连接断开回调
* OnHeartBeatWarning 心跳超时报警回调
* OnRspAuthenticate 客户端认证应答回调
* OnRspUserLogin 登录应答回调
* OnRspUserLogout 登出应答回调
* OnRspUserPasswordUpdate 用户密码修改应答回调
* OnRspTradingAccountPasswordUpdate 资金账户密码修改应答回调
* OnRspUserAuthMethod 查询支持的认证模式应答回调
* OnRspGenUserCaptcha 获取图形验证码应答回调
* OnRspGenUserText 获取短信验证码应答回调
* OnRspOrderInsert 报单录入应答回调
* OnRspParkedOrderInsert 预埋报单录入应答回调
* OnRspParkedOrderAction 预埋撤单录入应答回调
* OnRspOrderAction 报单操作（撤单）应答回调
* OnRspQueryMaxOrderVolume 查询最大报单数量应答回调
* OnRspSettlementInfoConfirm 投资者结算结果确认应答回调
* OnRspRemoveParkedOrder 删除预埋报单应答回调
* OnRspRemoveParkedOrderAction 删除预埋撤单应答回调
* OnRspExecOrderInsert 执行宣告录入应答回调
* OnRspExecOrderAction 执行宣告操作应答回调
* OnRspForQuoteInsert 询价录入应答回调
* OnRspQuoteInsert 报价录入应答回调
* OnRspQuoteAction 报价操作应答回调
* OnRspBatchOrderAction 批量报单操作应答回调
* OnRspOptionSelfCloseInsert 期权自对冲录入应答回调
* OnRspOptionSelfCloseAction 期权自对冲操作应答回调
* OnRspCombActionInsert 组合操作录入应答回调
* OnRspQryOrder 报单查询应答回调
* OnRspQryTrade 成交查询应答回调
* OnRspQryInvestorPosition 投资者持仓查询应答回调
* OnRspQryTradingAccount 资金账户查询应答回调
* OnRspQryInvestor 投资者查询应答回调
* OnRspQryTradingCode 交易编码查询应答回调
* OnRspQryInstrumentMarginRate 合约保证金率查询应答回调
* OnRspQryInstrumentCommissionRate 合约手续费率查询应答回调
* OnRspQryExchange 交易所查询应答回调
* OnRspQryProduct 产品查询应答回调
* OnRspQryInstrument 合约查询应答回调
* OnRspQryDepthMarketData 深度行情查询应答回调
* OnRspQrySettlementInfo 投资者结算结果查询应答回调
* OnRspQryTransferBank 转账银行查询应答回调
* OnRspQryInvestorPositionDetail 投资者持仓明细查询应答回调
* OnRspQryNotice 客户通知查询应答回调
* OnRspQrySettlementInfoConfirm 结算结果确认查询应答回调
* OnRspQryInvestorPositionCombineDetail 投资者持仓组合明细查询应答回调
* OnRspQryCFMMCTradingAccountKey 保证金监管系统资金账户密钥查询应答回调
* OnRspQryEWarrantOffset 仓单折抵查询应答回调
* OnRspQryInvestorProductGroupMargin 投资者产品/产品群保证金查询应答回调
* OnRspQryExchangeMarginRate 交易所保证金率查询应答回调
* OnRspQryExchangeMarginRateAdjust 交易所保证金率调整查询应答回调
* OnRspQryExchangeRate 汇率查询应答回调
* OnRspQrySecAgentACIDMap 二级代理操作员银期权限查询应答回调
* OnRspQryProductExchRate 产品报价汇率查询应答回调
* OnRspQryProductGroup 产品群查询应答回调
* OnRspQryMMInstrumentCommissionRate 做市商合约手续费率查询应答回调
* OnRspQryMMOptionInstrCommRate 做市商期权合约手续费率查询应答回调
* OnRspQryInstrumentOrderCommRate 报单手续费查询应答回调
* OnRspQrySecAgentTradingAccount 二级代理资金账户查询应答回调
* OnRspQrySecAgentCheckMode 二级代理检查模式查询应答回调
* OnRspQrySecAgentTradeInfo 二级代理交易权限查询应答回调
* OnRspQryOptionInstrTradeCost 期权交易成本查询应答回调
* OnRspQryOptionInstrCommRate 期权手续费查询应答回调
* OnRspQryExecOrder 执行宣告查询应答回调
* OnRspQryForQuote 询价查询应答回调
* OnRspQryQuote 报价查询应答回调
* OnRspQryOptionSelfClose 期权自对冲查询应答回调
* OnRspQryInvestUnit 投资单元查询应答回调
* OnRspQryCombInstrumentGuard 组合合约安全度查询应答回调
* OnRspQryCombAction 组合操作查询应答回调
* OnRspQryTransferSerial 银期转账流水查询应答回调
* OnRspQryAccountregister 银期签约关系查询应答回调
* OnRspQryContractBank 签约银行查询应答回调
* OnRspQryParkedOrder 预埋报单查询应答回调
* OnRspQryParkedOrderAction 预埋撤单查询应答回调
* OnRspQryTradingNotice 交易通知查询应答回调
* OnRspQryBrokerTradingParams 经纪公司交易参数查询应答回调
* OnRspQryBrokerTradingAlgos 经纪公司交易算法查询应答回调
* OnRspQueryCFMMCTradingAccountToken 查询保证金监管系统用户令牌应答回调
* OnRspError 错误响应回调
* OnRtnOrder 报单回报回调
* OnRtnTrade 成交回报回调
* OnErrRtnOrderInsert 报单录入错误回报回调
* OnErrRtnOrderAction 报单操作错误回报回调
* OnRtnInstrumentStatus 合约交易状态通知回调
* OnRtnBulletin 公告通知回调
* OnRtnTradingNotice 交易通知回调
* OnRtnErrorConditionalOrder 条件单错误通知回调
* OnRtnExecOrder 执行宣告回报回调
* OnErrRtnExecOrderInsert 执行宣告录入错误回报回调
* OnErrRtnExecOrderAction 执行宣告操作错误回报回调
* OnErrRtnForQuoteInsert 询价录入错误回报回调
* OnRtnQuote 报价回报回调
* OnErrRtnQuoteInsert 报价录入错误回报回调
* OnErrRtnQuoteAction 报价操作错误回报回调
* OnRtnForQuoteRsp 询价响应回报回调
* OnRtnCFMMCTradingAccountToken 保证金监管系统用户令牌回报回调
* OnErrRtnBatchOrderAction 批量报单操作错误回报回调
* OnRtnOptionSelfClose 期权自对冲回报回调
* OnErrRtnOptionSelfCloseInsert 期权自对冲录入错误回报回调
* OnErrRtnOptionSelfCloseAction 期权自对冲操作错误回报回调
* OnRtnCombAction 组合操作回报回调
* OnErrRtnCombActionInsert 组合操作录入错误回报回调
* OnRtnFromBankToFutureByBank 银行发起银行转期货通知回调
* OnRtnFromFutureToBankByBank 银行发起期货转银行通知回调
* OnRtnRepealFromBankToFutureByBank 银行发起冲正银行转期货通知回调
* OnRtnRepealFromFutureToBankByBank 银行发起冲正期货转银行通知回调
* OnRtnFromBankToFutureByFuture 期货发起银行转期货通知回调
* OnRtnFromFutureToBankByFuture 期货发起期货转银行通知回调
* OnRtnRepealFromBankToFutureByFutureManual 期货发起冲正银行转期货通知回调
* OnRtnRepealFromFutureToBankByFutureManual 期货发起冲正期货转银行通知回调
* OnRtnQueryBankBalanceByFuture 期货发起查询银行余额通知回调
* OnErrRtnBankToFutureByFuture 期货发起银行转期货错误回报回调
* OnErrRtnFutureToBankByFuture 期货发起期货转银行错误回报回调
* OnErrRtnRepealBankToFutureByFutureManual 期货发起冲正银行转期货错误回报回调
* OnErrRtnRepealFutureToBankByFutureManual 期货发起冲正期货转银行错误回报回调
* OnErrRtnQueryBankBalanceByFuture 期货发起查询银行余额错误回报回调
* OnRtnRepealFromBankToFutureByFuture 期货发起冲正银行转期货通知回调
* OnRtnRepealFromFutureToBankByFuture 期货发起冲正期货转银行通知回调
* OnRspFromBankToFutureByFuture 期货发起银行转期货应答回调
* OnRspFromFutureToBankByFuture 期货发起期货转银行应答回调
* OnRspQueryBankAccountMoneyByFuture 期货发起查询银行余额应答回调
* OnRtnOpenAccountByBank 银行发起开户通知回调
* OnRtnCancelAccountByBank 银行发起销户通知回调
* OnRtnChangeAccountByBank 银行发起变更银行账户通知回调

## 查询函数

* CreateFtdcTraderApi 创建 TraderApi 实例
* GetApiVersion 获取 API 版本号
* Release 释放接口对象
* Init 初始化并启动线程
* Join 阻塞等待线程结束
* GetTradingDay 获取当前交易日
* RegisterFront 注册前置机地址
* RegisterNameServer 注册名字服务器地址
* RegisterFensUserInfo 注册 Fens 用户信息
* RegisterSpi 注册回调接口实例
* SubscribePrivateTopic 订阅私有流
* SubscribePublicTopic 订阅公共流
* ReqAuthenticate 客户端认证请求
* RegisterUserSystemInfo 注册用户系统信息（终端认证模式）
* SubmitUserSystemInfo 上报用户系统信息（终端认证模式）
* ReqUserLogin 用户登录请求
* ReqUserLogout 用户登出请求
* ReqUserPasswordUpdate 用户密码修改请求
* ReqTradingAccountPasswordUpdate 资金账户密码修改请求
* ReqUserAuthMethod 查询支持的用户认证模式
* ReqGenUserCaptcha 获取图形验证码
* ReqGenUserText 获取短信验证码
* ReqUserLoginWithCaptcha 使用图形验证码登录
* ReqUserLoginWithText 使用短信验证码登录
* ReqUserLoginWithOTP 使用动态口令登录
* ReqOrderInsert 录入普通报单
* ReqParkedOrderInsert 录入预埋报单
* ReqParkedOrderAction 录入预埋撤单
* ReqOrderAction 报单操作（撤单、改单）
* ReqQueryMaxOrderVolume 查询最大报单数量
* ReqSettlementInfoConfirm 投资者结算结果确认
* ReqRemoveParkedOrder 删除预埋报单
* ReqRemoveParkedOrderAction 删除预埋撤单
* ReqExecOrderInsert 执行宣告录入
* ReqExecOrderAction 执行宣告操作
* ReqForQuoteInsert 询价录入
* ReqQuoteInsert 报价录入
* ReqQuoteAction 报价操作
* ReqBatchOrderAction 批量报单操作
* ReqOptionSelfCloseInsert 期权自对冲录入
* ReqOptionSelfCloseAction 期权自对冲操作
* ReqCombActionInsert 组合操作录入
* ReqQryOrder 报单查询
* ReqQryTrade 成交查询
* ReqQryInvestorPosition 投资者持仓查询
* ReqQryTradingAccount 资金账户查询
* ReqQryInvestor 投资者查询
* ReqQryTradingCode 交易编码查询
* ReqQryInstrumentMarginRate 合约保证金率查询
* ReqQryInstrumentCommissionRate 合约手续费率查询
* ReqQryExchange 交易所查询
* ReqQryProduct 产品查询
* ReqQryInstrument 合约查询
* ReqQryDepthMarketData 深度行情查询
* ReqQrySettlementInfo 投资者结算结果查询
* ReqQryTransferBank 转账银行查询
* ReqQryInvestorPositionDetail 投资者持仓明细查询
* ReqQryNotice 客户通知查询
* ReqQrySettlementInfoConfirm 结算结果确认查询
* ReqQryInvestorPositionCombineDetail 投资者持仓组合明细查询
* ReqQryCFMMCTradingAccountKey 保证金监管系统资金账户密钥查询
* ReqQryEWarrantOffset 仓单折抵查询
* ReqQryInvestorProductGroupMargin 投资者产品/产品群保证金查询
* ReqQryExchangeMarginRate 交易所保证金率查询
* ReqQryExchangeMarginRateAdjust 交易所保证金率调整查询
* ReqQryExchangeRate 汇率查询
* ReqQrySecAgentACIDMap 二级代理操作员银期权限查询
* ReqQryProductExchRate 产品报价汇率查询
* ReqQryProductGroup 产品群查询
* ReqQryMMInstrumentCommissionRate 做市商合约手续费率查询
* ReqQryMMOptionInstrCommRate 做市商期权合约手续费率查询
* ReqQryInstrumentOrderCommRate 报单手续费查询
* ReqQrySecAgentTradingAccount 二级代理资金账户查询
* ReqQrySecAgentCheckMode 二级代理检查模式查询
* ReqQrySecAgentTradeInfo 二级代理交易权限查询
* ReqQryOptionInstrTradeCost 期权交易成本查询
* ReqQryOptionInstrCommRate 期权手续费查询
* ReqQryExecOrder 执行宣告查询
* ReqQryForQuote 询价查询
* ReqQryQuote 报价查询
* ReqQryOptionSelfClose 期权自对冲查询
* ReqQryInvestUnit 投资单元查询
* ReqQryCombInstrumentGuard 组合合约安全度查询
* ReqQryCombAction 组合操作查询
* ReqQryTransferSerial 银期转账流水查询
* ReqQryAccountregister 银期签约关系查询
* ReqQryContractBank 签约银行查询
* ReqQryParkedOrder 预埋报单查询
* ReqQryParkedOrderAction 预埋撤单查询
* ReqQryTradingNotice 交易通知查询
* ReqQryBrokerTradingParams 经纪公司交易参数查询
* ReqQryBrokerTradingAlgos 经纪公司交易算法查询
* ReqQueryCFMMCTradingAccountToken 查询保证金监管系统用户令牌
* ReqFromBankToFutureByFuture 期货发起银行转期货
* ReqFromFutureToBankByFuture 期货发起期货转银行
* ReqQueryBankAccountMoneyByFuture 期货发起查询银行余额

# ThostFtdcUserApiDataType.h

* TThostFtdcTraderIDType 交易员代码
* TThostFtdcInvestorIDType 投资者账号（即资金账号）
* TThostFtdcBrokerIDType 经纪公司代码
* TThostFtdcUserIDType 用户登录名
* TThostFtdcPasswordType 登录密码
* TThostFtdcInstrumentIDType 合约代码（如 rb2401、IF2403）
* TThostFtdcExchangeIDType 交易所代码（如 SHFE、CFFEX）
* TThostFtdcOrderRefType 报单引用（本地自增，用来区分同一会话中的不同报单）
* TThostFtdcOrderSysIDType 交易所系统报单编号（交易所返回的全局唯一）
* TThostFtdcTradeIDType 成交编号（交易所返回的全局唯一）
* TThostFtdcClientIDType 客户编码（上期所、能源中心区分投机/套保/套利）
* TThostFtdcAccountIDType 资金账户（与 InvestorID 通常相同）
* TThostFtdcMacAddressType 终端 MAC 地址（用于合规留痕）
* TThostFtdcIPAddressType 终端 IP 地址
* TThostFtdcSystemIDType 前置/交易系统标识
* TThostFtdcDateType 日期字段（YYYYMMDD）
* TThostFtdcTimeType 时间字段（HH:MM:SS）
* TThostFtdcLongTimeType 精确时间（HH:MM:SS.mmm）
* TThostFtdcPriceType 价格（double）
* TThostFtdcVolumeType 数量（int，手数）
* TThostFtdcMoneyType 金额（double，单位：元）
* TThostFtdcFrontIDType 前置编号
* TThostFtdcSessionIDType 会话编号（FrontID+SessionID+OrderRef 可唯一标识一次报单）
* TThostFtdcRequestIDType 请求编号（异步请求/应答的关联键）
* TThostFtdcSequenceNoType 本地流水号
* TThostFtdcSettlementIDType 结算编号（每个交易日递增）
* TThostFtdcOrderLocalIDType 本地报单编号（CTP 内部用）
* TThostFtdcOrderActionRefType 撤单/改单引用
* TThostFtdcDirectionType 买卖方向：'0' 买，'1' 卖
* TThostFtdcOffsetFlagType 开平标志：'0' 开仓，'1' 平仓，'3' 平今，'4' 平昨
* TThostFtdcHedgeFlagType 投机套保标志：'1' 投机，'2' 套利，'3' 套保
* TThostFtdcOrderPriceTypeType 价格类型：'1' 任意价，'2' 限价，'3' 最优价
* TThostFtdcOrderStatusType 报单状态：'0' 全部成交，'1' 部分成交还在队列，'3' 未成交还在队列，'5' 已撤单
* TThostFtdcOrderSubmitStatusType 报单提交状态：'0' 已提交，'3' 已接受，'4' 已拒绝

# ThostFtdcUserApiStruct.h

* CThostFtdcDisseminationField 行情广播序号与序列号
* CThostFtdcReqUserLoginField 用户登录字段
* CThostFtdcRspUserLoginField 用户登录应答字段
* CThostFtdcUserLogoutField 用户登出字段
* CThostFtdcForceUserLogoutField 强制用户登出字段
* CThostFtdcReqAuthenticateField 客户端认证请求字段
* CThostFtdcRspAuthenticateField 客户端认证应答字段
* CThostFtdcAuthenticationInfoField 客户端认证信息字段
* CThostFtdcRspUserLogin2Field 用户登录应答 2 字段
* CThostFtdcTransferHeaderField 银期转账报文头
* CThostFtdcTransferBankToFutureReqField 银行转期货请求
* CThostFtdcTransferBankToFutureRspField 银行转期货应答
* CThostFtdcTransferFutureToBankReqField 期货转银行请求
* CThostFtdcTransferFutureToBankRspField 期货转银行应答
* CThostFtdcTransferQryBankReqField 查询银行余额请求
* CThostFtdcTransferQryBankRspField 查询银行余额应答
* CThostFtdcTransferQryDetailReqField 查询转账流水请求
* CThostFtdcTransferQryDetailRspField 查询转账流水应答
* CThostFtdcRspInfoField 通用错误信息
* CThostFtdcExchangeField 交易所信息
* CThostFtdcProductField 产品信息
* CThostFtdcInstrumentField 合约信息
* CThostFtdcBrokerField 经纪公司信息
* CThostFtdcTraderField 交易员信息
* CThostFtdcInvestorField 投资者信息
* CThostFtdcTradingCodeField 交易编码信息
* CThostFtdcPartBrokerField 会员-经纪关系
* CThostFtdcSuperUserField 超级用户
* CThostFtdcSuperUserFunctionField 超级用户功能
* CThostFtdcInvestorGroupField 投资者分组
* CThostFtdcTradingAccountField 资金账户
* CThostFtdcInvestorPositionField 投资者持仓
* CThostFtdcInstrumentMarginRateField 合约保证金率
* CThostFtdcInstrumentCommissionRateField 合约手续费率
* CThostFtdcDepthMarketDataField 深度行情
* CThostFtdcInstrumentTradingRightField 合约交易权限
* CThostFtdcBrokerUserField 经纪公司用户
* CThostFtdcBrokerUserPasswordField 经纪公司用户密码
* CThostFtdcBrokerUserFunctionField 经纪公司用户功能
* CThostFtdcTraderOfferField 交易员报盘
* CThostFtdcSettlementInfoField 投资者结算单
* CThostFtdcInstrumentMarginRateAdjustField 合约保证金率调整
* CThostFtdcExchangeMarginRateField 交易所保证金率
* CThostFtdcExchangeMarginRateAdjustField 交易所保证金率调整
* CThostFtdcExchangeRateField 汇率
* CThostFtdcSettlementRefField 结算参考
* CThostFtdcCurrentTimeField 当前时间
* CThostFtdcCommPhaseField 通讯阶段
* CThostFtdcLoginInfoField 登录信息
* CThostFtdcLogoutAllField 全部登出
* CThostFtdcFrontStatusField 前置状态
* CThostFtdcUserPasswordUpdateField 修改用户密码
* CThostFtdcInputOrderField 报单录入
* CThostFtdcOrderField 报单回报
* CThostFtdcExchangeOrderField 交易所报单
* CThostFtdcExchangeOrderInsertErrorField 交易所报单插入错误
* CThostFtdcInputOrderActionField 报单操作录入
* CThostFtdcOrderActionField 报单操作回报
* CThostFtdcExchangeOrderActionField 交易所报单操作
* CThostFtdcExchangeOrderActionErrorField 交易所报单操作错误
* CThostFtdcExchangeTradeField 交易所成交
* CThostFtdcTradeField 成交回报
* CThostFtdcUserSessionField 用户会话
* CThostFtdcQueryMaxOrderVolumeField 查询最大报单量
* CThostFtdcSettlementInfoConfirmField 结算结果确认
* CThostFtdcSyncDepositField 同步入金
* CThostFtdcSyncFundMortgageField 同步货币质押
* CThostFtdcBrokerSyncField 经纪公司同步
* CThostFtdcSyncingInvestorField 同步投资者
* CThostFtdcSyncingTradingCodeField 同步交易编码
* CThostFtdcSyncingInvestorGroupField 同步投资者分组
* CThostFtdcSyncingTradingAccountField 同步资金账户
* CThostFtdcSyncingInvestorPositionField 同步持仓
* CThostFtdcSyncingInstrumentMarginRateField 同步合约保证金率
* CThostFtdcSyncingInstrumentCommissionRateField 同步合约手续费率
* CThostFtdcSyncingInstrumentTradingRightField 同步合约交易权限
* CThostFtdcQryOrderField 查询报单
* CThostFtdcQryTradeField 查询成交
* CThostFtdcQryInvestorPositionField 查询持仓
* CThostFtdcQryTradingAccountField 查询资金账户
* CThostFtdcQryInvestorField 查询投资者
* CThostFtdcQryTradingCodeField 查询交易编码
* CThostFtdcQryInvestorGroupField 查询投资者分组
* CThostFtdcQryInstrumentMarginRateField 查询合约保证金率
* CThostFtdcQryInstrumentCommissionRateField 查询合约手续费率
* CThostFtdcQryInstrumentTradingRightField 查询合约交易权限
* CThostFtdcQryBrokerField 查询经纪公司
* CThostFtdcQryTraderField 查询交易员
* CThostFtdcQrySuperUserFunctionField 查询超级用户功能
* CThostFtdcQryUserSessionField 查询用户会话
* CThostFtdcQryPartBrokerField 查询会员-经纪关系
* CThostFtdcQryFrontStatusField 查询前置状态
* CThostFtdcQryExchangeOrderField 查询交易所报单
* CThostFtdcQryOrderActionField 查询报单操作
* CThostFtdcQryExchangeOrderActionField 查询交易所报单操作
* CThostFtdcQrySuperUserField 查询超级用户
* CThostFtdcQryExchangeField 查询交易所
* CThostFtdcQryProductField 查询产品
* CThostFtdcQryInstrumentField 查询合约
* CThostFtdcQryDepthMarketDataField 查询深度行情
* CThostFtdcQryBrokerUserField 查询经纪公司用户
* CThostFtdcQryBrokerUserFunctionField 查询经纪公司用户功能
* CThostFtdcQryTraderOfferField 查询交易员报盘
* CThostFtdcQrySyncDepositField 查询同步入金
* CThostFtdcQrySettlementInfoField 查询结算单
* CThostFtdcQryExchangeMarginRateField 查询交易所保证金率
* CThostFtdcQryExchangeMarginRateAdjustField 查询交易所保证金率调整
* CThostFtdcQryExchangeRateField 查询汇率
* CThostFtdcQrySyncFundMortgageField 查询同步货币质押
* CThostFtdcQryHisOrderField 查询历史报单
CTPMini1.5.8
# ThostFtdcMdApi.h

* OnFrontConnected 建立连接
* OnFrontDisconnected 断开连接
* OnHeartBeatWarning 心跳超时告警
* OnRspUserLogin 登录响应
* OnRspUserLogout 登出响应
* OnRspError 错误响应
* OnRspSubMarketData 订阅行情响应
* OnRspUnSubMarketData 取消订阅行情响应
* OnRspSubForQuoteRsp 订阅询价响应
* OnRspUnSubForQuoteRsp 取消订阅询价响应
* OnRtnDepthMarketData 深度行情推送
* OnRtnMBLMarketData 分价表行情推送
* OnRtnForQuoteRsp 询价通知

* CreateFtdcMdApi 创建API实例
* GetApiVersion 获取API版本
* Release 销毁API实例
* Init 初始化并启动线程
* Join 阻塞等待线程结束
* GetTradingDay 获取当前交易日
* RegisterFront 注册前置机地址
* RegisterSpi 注册回调接口
* SubscribeMarketData 订阅行情
* UnSubscribeMarketData 取消订阅行情
* SubscribeForQuoteRsp 订阅询价
* UnSubscribeForQuoteRsp 取消订阅询价
* ReqUserLogin 用户登录
* ReqUserLogout 用户登出

# ThostFtdcTraderApi.h

* OnFrontConnected 建立连接
* OnFrontDisconnected 断开连接
* OnHeartBeatWarning 心跳超时告警
* OnRspAuthenticate 客户端认证响应
* OnRspUserLogin 登录响应
* OnRspUserLogout 登出响应
* OnRspOrderInsert 报单录入响应
* OnRspOrderAction 报单操作响应
* OnRspExecOrderInsert 执行宣告录入响应
* OnRspExecOrderAction 执行宣告操作响应
* OnRspForQuoteInsert 询价录入响应
* OnRspQuoteInsert 报价录入响应
* OnRspQuoteAction 报价操作响应
* OnRspBatchOrderAction 批量报单操作响应
* OnRspOptionSelfCloseInsert 期权自对冲录入响应
* OnRspOptionSelfCloseAction 期权自对冲操作响应
* OnRspCombActionInsert 组合操作录入响应
* OnRspQryOrder 查询报单响应
* OnRspQryTrade 查询成交响应
* OnRspQryInvestorPosition 查询投资者持仓响应
* OnRspQryTradingAccount 查询资金账户响应
* OnRspQryInvestor 查询投资者响应
* OnRspQryTradingCode 查询交易编码响应
* OnRspQryInstrumentMarginRate 查询合约保证金率响应
* OnRspQryInstrumentCommissionRate 查询合约手续费率响应
* OnRspQryExchange 查询交易所响应
* OnRspQryProduct 查询产品响应
* OnRspQryInstrument 查询合约响应
* OnRspQryCombInstrument 查询组合合约响应
* OnRspQryCombAction 查询组合操作响应
* OnRspQryInvestorPositionForComb 查询组合持仓响应
* OnRspQryDepthMarketData 查询深度行情响应
* OnRspQryInstrumentStatus 查询合约状态响应
* OnRspQryInvestorPositionDetail 查询投资者持仓明细响应
* OnRspQryInvestorPositionCombineDetail 查询投资者组合持仓明细响应
* OnRspQryExchangeMarginRate 查询交易所保证金率响应
* OnRspQryExchangeMarginRateAdjust 查询交易所保证金率调整响应
* OnRspQryOptionInstrTradeCost 查询期权交易成本响应
* OnRspQryOptionInstrCommRate 查询期权手续费率响应
* OnRspQryExecOrder 查询执行宣告响应
* OnRspQryForQuote 查询询价响应
* OnRspQryQuote 查询报价响应
* OnRspQryOptionSelfClose 查询期权自对冲响应
* OnRspError 错误响应
* OnRtnOrder 报单回报
* OnRtnTrade 成交回报
* OnErrRtnOrderInsert 报单录入错误回报
* OnErrRtnOrderAction 报单操作错误回报
* OnRtnInstrumentStatus 合约交易状态通知
* OnRtnExecOrder 执行宣告回报
* OnErrRtnExecOrderInsert 执行宣告录入错误回报
* OnErrRtnExecOrderAction 执行宣告操作错误回报
* OnErrRtnForQuoteInsert 询价录入错误回报
* OnRtnQuote 报价回报
* OnErrRtnQuoteInsert 报价录入错误回报
* OnErrRtnQuoteAction 报价操作错误回报
* OnRtnForQuoteRsp 询价通知
* OnErrRtnBatchOrderAction 批量报单操作错误回报
* OnRtnOptionSelfClose 期权自对冲回报
* OnErrRtnOptionSelfCloseInsert 期权自对冲录入错误回报
* OnErrRtnOptionSelfCloseAction 期权自对冲操作错误回报
* OnRtnCombAction 组合操作回报
* OnRspQryInstrumentOrderCommRate 查询报单手续费率响应

* CreateFtdcTraderApi 创建API实例
* GetApiVersion 获取API版本
* Release 销毁API实例
* Init 初始化并启动线程
* Join 阻塞等待线程结束
* GetTradingDay 获取当前交易日
* RegisterFront 注册前置机地址
* RegisterSpi 注册回调接口
* SubscribePrivateTopic 订阅私有流
* SubscribePublicTopic 订阅公共流
* ReqAuthenticate 客户端认证请求
* ReqUserLogin 用户登录请求
* ReqUserLoginEncrypt 加密登录请求
* ReqUserLogout 用户登出请求
* ReqOrderInsert 报单录入请求
* ReqOrderAction 报单操作请求
* ReqExecOrderInsert 执行宣告录入请求
* ReqExecOrderAction 执行宣告操作请求
* ReqForQuoteInsert 询价录入请求
* ReqQuoteInsert 报价录入请求
* ReqQuoteAction 报价操作请求
* ReqBatchOrderAction 批量报单操作请求
* ReqOptionSelfCloseInsert 期权自对冲录入请求
* ReqOptionSelfCloseAction 期权自对冲操作请求
* ReqCombActionInsert 组合操作录入请求
* ReqQryOrder 查询报单
* ReqQryTrade 查询成交
* ReqQryInvestorPosition 查询投资者持仓
* ReqQryTradingAccount 查询资金账户
* ReqQryInvestor 查询投资者
* ReqQryTradingCode 查询交易编码
* ReqQryInstrumentMarginRate 查询合约保证金率
* ReqQryInstrumentCommissionRate 查询合约手续费率
* ReqQryExchange 查询交易所
* ReqQryProduct 查询产品
* ReqQryInstrument 查询合约
* ReqQryCombInstrument 查询组合合约
* ReqQryInvestorPositionForComb 查询组合持仓
* ReqQryCombAction 查询组合操作
* ReqQryDepthMarketData 查询深度行情
* ReqQryOptionSelfClose 查询期权自对冲
* ReqQryInstrumentStatus 查询合约状态
* ReqQryInvestorPositionDetail 查询投资者持仓明细
* ReqQryInvestorPositionCombineDetail 查询投资者组合持仓明细
* ReqQryExchangeMarginRate 查询交易所保证金率
* ReqQryExchangeMarginRateAdjust 查询交易所保证金率调整
* ReqQryOptionInstrTradeCost 查询期权交易成本
* ReqQryOptionInstrCommRate 查询期权手续费率
* ReqQryExecOrder 查询执行宣告
* ReqQryForQuote 查询询价
* ReqQryQuote 查询报价
* ReqQryInstrumentOrderCommRate 查询报单手续费率

# ThostFtdcUserApiDataType.h

# ThostFtdcUserApiStruct.h
补充
# api spi

| 维度    | API                               | SPI                                 |
|-------|-----------------------------------|-------------------------------------|
| 全称    | Application Programming Interface | Service Provider Interface          |
| 使用者   | 你的程序                              | CTP 内部工作线程                          |
| 调用方向  | 你 CTP                             | CTP 你                               |
| 典型动作  | 登录、下单、撤单、查资金、订阅行情 …               | 收到登录回报、成交回报、行情推送 …                  |
| 使用方式  | 直接调用 API 对象的成员函数即可                | 必须写一个类继承 SPI，把关心的虚函数重写，再把该对象注册给 API |
| 线程上下文 | 任何线程均可调用；CTP 保证线程安全               | 回调总在 CTP 内部工作线程触发，注意线程同步            |

/home/yangcheng/clion_project/wondertrader/src/API/CTP6.3.15/
/home/yangcheng/clion_project/wondertrader/src/API/CTPMini1.5.8/

# ctp mini-ctp

```
miniCTP 与标准 CTP 的本质区别可以概括为“瘦身版”与“完整版”的关系，核心差异体现在系统架构、功能集、性能与运维 4 个维度：

1. 系统架构  
   • **CTP（主席/标准版）**：传统三层——交易前置 tServer、行情前置 mServer、报盘前置 fServer 分别独立部署，模块完整，支持所有交易所全品种。  
   • **miniCTP**：官方把三层合并成一个精简 tServer 进程，仅保留上期所/能源中心/中金所/大商所/郑商所的核心交易报盘和行情报盘，剔除非必要组件。

2. 功能集  
   • **CTP**：API 全部 200+ 个查询 / 业务接口均可用。  
   • **miniCTP**：  
     – 删减了若干低频查询（例如部分风控、席位、会员类查询）；  
     – 回调逻辑略有变化，如最后一条数据指针可能为 NULL，需要显式做空指针保护；  
     – 其余字段、枚举、流控机制与标准 CTP 完全兼容，已基于 CTP 开发的程序一般只需重新链接 miniCTP 库即可运行。

3. 性能与资源  
   • **延迟**：miniCTP 去掉多余线程与网络转发，撮合高峰时段报单/撤单延迟比主席 CTP 可低 1~3 ms。  
   • **资源占用**：内存占用下降 30 %~50 %，CPU 消耗更低，适合轻量级云主机或容器化部署。

4. 运维与场景  
   • **CTP**：期货公司主席席位，支持全品种、全业务（银期、期权执行、组合保证金等），适合 95 % 普通投资者。  
   • **miniCTP**：  
     – 期货公司次席/极速通道、私募自营机房；  
     – 高频/量化策略、低延迟需求场景；  
     – 不开放银期转账、期权执行等复杂业务，需由主席 CTP 补位。

一句话总结  
miniCTP = CTP API 兼容 + 系统大幅精简 + 延迟更低 + 功能裁剪，适合对速度敏感、不需要全部业务接口的量化交易者；标准 CTP 功能最全、生态最成熟，适合普通投资者及需要银期、期权等完整业务的场景。
```
