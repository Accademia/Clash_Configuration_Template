

# 项目概述

项目名称：超级省电clash配置模版

项目链接： https://github.com/Accademia/Clash_Configuration_Template
 
项目简述：

 - 提供一套 同时支持  “ Clash Meta （ 如 ：Clash Verge Rev 、 OpenClash 等 ） / Stash for iPhone ”  的分流策略模版。

 - 力求 ： 
   + 极致省电🔥🔥 
   + 0 DNS泄漏 
   + 0 绕路 白名单翻墙 （不干扰日常上网）
   + 0 代价 修改IP归属地显示 
   + 0 频繁维护（省心） 
   

<br>
<br>

------

# 本模版的 需求汇总 

<br>

制作本模版，是希望能将 clash meta / stash 客户端，配置成 以下效果：

  > 🔋 24小时不关闭VPN = 0费电 
  
  > 🇨🇳 国内APP 使用 = 0影响 
  
  > 🌍 跨洋翻墙 体验 = 本地网络
  
  > 🫥 翻墙行为 + 境外流量 = 0特征 0泄漏 

<br>

<br>

✅ 目前 本模版 目前状态（已实现）：

 - 100% 达到 🇺🇸 “美国数字居民” 级 VPN 的规格 ❕❕❕

   >  也就是说，只要你有 🇺🇸 🇬🇧 🇦🇺 🇯🇵 住宅IP，你可以用本模版，全天在后台挂 这几个国家的任意金融级APP（如 花旗银行、劳埃德银行） ，也不会被账号封控（这些APP的GPS位置必须关闭）。注意：🇺🇸 美国数字居民、美国离岸居民、美国云居民 ，对于VPN的要求 ，比 OpenAI ChatGPT ，严格的多。

   >  运营海外视频自媒体账号，也同样能保证不会漏馅。
   
   >  7x24小时 常驻后台，🇨🇳 国内APP =  秒加载 无感知 无绕路 。

<br>
<br>
  
<br>
<br>

-----


⚠️⚠️⚠️⚠️ 不看完 本说明自述 ，尤其不看完如下 两个章节 ，就想指挥别人当保姆的 、就说本模版有BUG的。🤣 直接 0 社交 关闭issue

   >  - [ 《 规格说明 》 ](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E8%A7%84%E6%A0%BC%E8%AF%B4%E6%98%8E)  
   >
   >  - [《 如何将节点 加入本模版，并导入VPN软件 》](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E5%A6%82%E4%BD%95-%E4%BD%BF%E7%94%A8%E6%9C%AC%E6%A8%A1%E7%89%88-%E5%A6%82%E4%BD%95%E5%B0%86-vpn%E8%8A%82%E7%82%B9%E5%8A%A0%E5%85%A5%E5%88%B0%E6%9C%AC%E6%A8%A1%E7%89%88%E5%B9%B6%E5%AF%BC%E5%85%A5vpn%E8%BD%AF%E4%BB%B6) 

本模版 = 7x24挂机 高强度 自用级验证， 实锤 = 100% 可用，如果你分流失败，建议多照照自己的原因，实在不行 问ai。但肯定不是本模版有bug。（千万别问 免费AI ！至少 Gemini 3 Pro + GhatGPT Think 顶级付费AI！ 再次强调，付费AI 付费AI 付费AI ❕  ）

特别提示： 本模版 支持 无脑导入。但必须 “手工填入” 你自己的节点，才可正常使用！把本模版 当成免手工配置 + 自动筛选 订阅节点 的 🚫 100%不生效 🚫 

 > 之所以不支持自动筛选，这是由于 自动筛选 ，无法区分 哪些是 落地节点、中转节点，而本模版的 “抗节点损毁+IP稳定功能” 需要 精细区分节点性质。

❌ 拒绝适配 ：Clash Meta、Stash 以外的 其他客户端

-----


<br>
<br>
  
<br>
<br>


------


# 本模版 已实现的功能：

-  ### 支持 **黑名单翻墙 、白名单翻墙** 两套模版 ** 

-  ### **不影响 国内APP 使用体验** 
 
   > 在 “白名单翻墙”模式下 ：访问🇨🇳国内网站 = **几乎0绕路海外** 。
 
   > 🇨🇳 中国IP 分流优先级 = 最靠前、最高❕ 

   > 通过基于 《 魔改版 GeostieCN + 魔改版 ChinaMax 》打造 “两级缓存结构” ，实现 🇨🇳 国内流量 几乎0绕路 ！

-  ### 支持 海外 主流APP  
 
   >  几十个 🌍 海外APP，可 **“逐个APP”** 配置分流规则

-  ### 避免 被APP识别出 使用了VPN
 
   > 避免 "APP的安全机制" 通过识别VPN返回的 "假IP" 🦠  识别出正在使用VPN。禁用FakeIP功能 

-  ### **0 DNS泄漏** 
 
   > 🇨🇳 国内域名 ，只发送给 国内DNS。
   
   > 🌍 海外域名，只通过 海外VPN节点 转发给海外dns进行解析，不会同时发送给国内DNS服务器。
   
   >  上述两者 全程使用 DOH加密 

-  ### **满血版DNS解析** 
 
   > 不限制域名解析。 全程禁用 no-resolve

-  ### **最大化节约内存**
 
   > 降低DNS请求数量 ，全程禁用 Fallback DNS 。并将 外部规则集 全部迁移到 Domain / IP 的格式上。

-  ### **最小化电力消耗** 
 
   > 关闭所有 冗余并发。
  
   > 精简浓缩 规则数量。
  
   > 将日常场景中，高命中的规则放在最前部，避免出现 每次网络请求，都要对比了十几万条 🔥 才发现 域名是日常使用的 🇨🇳国内IP 

-  ### 支持 **修改IP归属地显示**
  
   > 覆盖 国内主流APP 

-  ### **按地理位置** 就近分配 VPN节点 
 
   > 对于 “有” 地理位置的的网站（如 各国顶级域名、各国IP地址），支持 按地理位置 全自动就近分配落地节点

-  ### **按VPN节点位置** 就近请求 CDN
  
   > 对于 “无” 地理位置的网站，支持 落地节点 **自动选取最近的CDN** 获取网站数据数据 。以便 境外流量 能100%避免，如 “🇺🇸美国节点 访问 🇯🇵日本CDN” 等 “全球绕路” 的情况
  
   > ⚠️ 注意： Stash 不支持此功能，此功能为Clash Meta 独占 

-  ### **保证IP地址稳定** 

   > 即便落地节点被墙，也不会乱跳IP 
 
   > 通过  **代理链** ，锁定落地节点。中转节点 随便被墙，配置会自动选择最优线路（延迟最低的中转线路）。
 
   > 不仅仅是TCP流量 ，100% 支持 **UDP代理链、QUIC代理链**  （ ⚠️ 注意： Stash 不支持此功能，此功能为Clash Meta 独占 ）

-  ### **抗节点损毁**

    > 任意节点损毁后（包括落地节点损毁后），会自动切换到备份节点上（所有的节点 都自动注册为备份节点）。 优先级 ：落地节点/住宅IP节点（及代理链） -> 损毁 -> 落地节点/住宅IP节点 所在国的其他节点（及代理链） -> 损毁 -> 全球延迟最低的节点 （及代理链）。即，只要还有最后一个节点在，外网就会被自动切换到此节点上（以求最大程度省心）
 
    > 除外 ：各国银行类网站 、强住宅IP检测类网站 。
 
-  ### 内置 **两组 远程规则集** 互为备份 
 
   > 哪怕任意一个外部规则源 更新慢 、停更，也不怕 

-  ### 让GFW监控你的 **“深度包检测”** 技术，全部归0 

   > 默认白名单翻墙 + DNS白名单分流， 让GFW无法探测你任何境外流量，隐私性拉满 


<br>

### ✅ 总结：本模版 非常适合，在iPhone手机上，“全天不关闭VPN” 的方式使用❕❕❕ 

哪怕跟国内外好友微信视频、看抖音快手、AppStore下载、使用各种国内办公软件、国内网盘，都不会因 本模版开启后常驻后台，而导致上网卡顿、绕路 或 消耗VPN节点流量。

<br>
<br>

------


# 本模版 包含哪些 分流类别：

<br>

- ### **分流 🌐 “DNS查询” 流量**：

   > 🌍 全球网站，只走 VPN节点 转发给海外DNS（ 不发起Fallback 、无FakeIP ）

   > 🇨🇳 中国网站，只走 国内DNS（极低延迟）

   > 上述两者：均全程DOH加密访问 （ 效果 = 无DNS泄漏 + 无DNS污染 ）

- ### **分流 🕑 “NTP查询” 流量**：

- ### **分流 ⛔️ “广告、偷窥隐私、反诈监控 …” 等 流氓流量**：

- ### **分流 🚧 “GFW” 流量**：

   > 默认被关闭（因为默认使用了白名单模式，如果你想默认使用黑名单模式，可以手动打开此选项）

- ### **分流 🌍 “境外” 主流应用 流量**

   > 包括：境外游戏、视音频、社交、新闻、AI、下载站、网盘、交易所、支付、购物、测速、其他工具 等等，每个都支持独立配置

- ### **分流 🌍 “境外” 强制住宅IP才能访问的 流量**：

   > 如：当地银行 （ 以便满足 🇺🇸 🇬🇧 🇦🇺 🇯🇵 “美国、各国数字移民” 的分流需求 ）

- ### **分流 🇨🇳 “中国APP” 的 IP归属地显示 流量**： 

   > 只代理 显示IP归属地 所需的流量，但APP内的其他流量、如图片 视频 ，均不走代理

- ### **分流 🇨🇳 ”中国” 流量**：
 
   > 中国分流 = 几乎0绕路直连！并且支持 以下每个国产APP都单独分流（且不影响IP归属地显示）
   
   > 网盘、短视频、长视频、社交、新闻、购物、手机厂、大厂 ：总计 40多个APP单独分流（默认关闭，可手动开启）

- ### **分流 🔄 “APP升级、系统升级” 流量**：

   > “苹果、微软、索尼、任天堂” 这四个超级大厂（非AI服务）默认直连，以避免 ios、windows、playstation、switch ，在软件升级、系统升级时，VPN流量被过度消耗。

- ### **基于 📍 “地理位置” 的 兜底策略**：

   > 如果没有匹配到上述的 分流策略，根据目标网站地理位置，匹配最近地理位置的节点

- ### **抗节点失联**：

   > 如单一节点被GFW间歇性封锁，但又需要此节点的IP来访问网站，那么其他任意中转节点，都会自动作为中间节点 转发链式代理。 从而最大限度保证了访问单一网站时IP的稳定性 

- ### **反代理识别软件的检测**：

   > 强制redir-host，避免因返回fakeip，而被软件检测识别出使用了代理。

- ### **内置双远程规则源**：

   > 同时内置两组 互为备份的 远程规则集 ：
   >    + 第一组 ：Geosite
   >    + 第二组 ：blackmatrix7/ios_rule_script  + Additional_Rule_For_Clash
   >    + 两组规则 = 90%重叠 ：即，哪怕任意一组 维护更新慢 或 停更，另外一组也能覆盖住。

- ### **完全隐秘行踪**：
 
   > 默认为白名单模式（出境流量 = 通过VPN线路加速 ）！在默认模式下，对GFW、上层网络出口，做到100%隐秘境外行踪。
 
   > 同时，也支持用户 手动配置切换成黑名单模式 从而节省流量
    
<br>
<br>

------

<br>



# 分流策略总揽

<br>

总计十级分流

```yaml


   # -------------------------------------------------------------- 
   #  说明文档 ： 路由规则（Rule）  -  大纲 ❕           总计十级 
   # -------------------------------------------------------------- 
   #      [第一级] 分流规则   :  前置规则 （ 如 局域网、DNS ）      
   # --------------------------------------------------------------   
   #      [第二级] 分流规则   :  回国 （ 如 CN ）                 🇨🇳
   # --------------------------------------------------------------   
   #      [第三级] 分流规则   :  外国 APP、网站                   🌍    
   # --------------------------------------------------------------   
   #      [第四级] 分流规则   :  外国 大厂                        🌍    
   # --------------------------------------------------------------   
   #      [第五级] 分流规则   :  国家、洲际（ 根域名 ）            🌍    
   # --------------------------------------------------------------   
   #      [第六级] 分流规则   :  国家、洲际（ GeoIP ）            🌍    
   # --------------------------------------------------------------   
   #      [第七级] 分流规则   :（ 不区分国家地区的 ） 全球性服务    🌍    
   # --------------------------------------------------------------   
   #      [第八级] 分流规则   :  GFWList                         🚧    
   # --------------------------------------------------------------   
   #      [第九级] 分流规则   :  回国兜底 （ 如 CN ）             🇨🇳
   # --------------------------------------------------------------   
   #      [第十级] 分流规则   :  全球兜底                               
   # --------------------------------------------------------------     


```

<br>
<br>

------


# 十级分流策略详解（按如下顺序匹配）

<br>

```yaml

   #  说明文档 ： 路由规则（Rule）  -  明细
   #
   # ------------------------------------------------------------------------------
   #           [第一级] 分流规则 : 前置 规则                 ( IP匹配 + DNS解析 )
   # ------------------------------------------------------------------------------
   #
   # [1st-00] -  基础协议 
   # [1st-01] -  DNS \ NTP 
   # [1st-02] -  局域网 
   # [1st-03] -  自己的 VPS  ：域名 \ IP
   # [1st-05] -  反私有DNS跟踪（HttpDNS）                            ⛔️        
   # [1st-06] -  反劫持（Hijacking）                                ⛔️    
   # [1st-08] -  保护隐私                                            ⛔️        
   # [1st-09] -  屏蔽广告                                            ⛔️              
   # [1st-09] -  第三方VNP软件                      
   #
   # ------------------------------------------------------------------------------
   #       [第二级] 分流规则 :  回国  （ 如 中国 ）            ( IP匹配 + DNS解析 )
   # ------------------------------------------------------------------------------
   # 
   # [2st-01] -  IP归属地        
   #                       
   # [2st-02] -  回国：网盘、云盘、下载软件                      # 暂未启用 ❌           
   # [2st-02] -  回国：视音频                                    # 暂未启用 ❌           
   # [2st-02] -  回国：社交                                      # 暂未启用 ❌               
   # [2st-02] -  回国：媒体                                      # 暂未启用 ❌    
   # [2st-02] -  回国：购物                                      # 暂未启用 ❌       
   # [2st-02] -  回国：游戏                                      # 暂未启用 ❌       
   # [2st-02] -  回国：硬件                                      # 暂未启用 ❌       
   # [2st-02] -  回国：BAT                                       # 暂未启用 ❌           
   # [2st-02] -  回国：其他                                      # 暂未启用 ❌       
   #                      
   # [2st-05] -  国家根域名（中国） 
   # [2st-05] -  GeoIP（中国）    
   #
   # ------------------------------------------------------------------------------
   #         [第三级] 分流规则 : 外国 APP、网站                 ( IP匹配 + DNS解析 )
   # ------------------------------------------------------------------------------
   #
   # [3st-00] -  测速
   #  
   # [3st-01] -  智能设备    
   # [3st-02] -  公有云：云盘、云存储                  
   # [3st-04] -  P2P下载软件        
   # [3st-05] -  需加速 才能流畅访问的网站      
   #                    
   # [3st-11] -  金融                
   # [3st-12] -  各国银行    (默认路由：不可配置)
   # [3st-13] -  专属网站（ 必须HomeIP才能下单的网站 … ）   (默认路由：不可配置)
   #                                                   
   # [3st-20] -  购物                 
   # [3st-21] -  游戏                 
   # [3st-22] -  视频                 
   # [3st-23] -  短视频               
   # [3st-24] -  直播                 
   # [3st-25] -  音频                 
   # [3st-26] -  社交                 
   # [3st-27] -  网络电话、eSIM        
   # [3st-28] -  资讯                 
   # [3st-29] -  AI                 
   # [3st-30] -  工具                 
   #
   # ------------------------------------------------------------------------------
   #       [第四级] 分流规则 :  外国 大厂                        ( IP匹配 + DNS解析 )
   # ------------------------------------------------------------------------------
   #  
   # [4st-01] -  国外大厂          
   #
   # ------------------------------------------------------------------------------        🔻🔻🔻🔻🔻🔻  
   #      [第五级] 分流规则 : 国家、洲际（ 根域名 ）            ( 域名匹配 )               ｜            
   # ------------------------------------------------------------------------------        ｜            
   #                                                                                       ｜            
   # [5st-01] -  国家根域名（VPS所在国家）                                                 ｜            
   # [5st-02] -  国家根域名（其他国家，按洲际分类）                                        ｜            
   #                                                                                       ｜            
   # ------------------------------------------------------------------------------        ｜            
   #       [第六级] 分流规则 : 国家、洲际（ GeoIP ）           ( IP匹配 + DNS解析 )        ｜            
   # ------------------------------------------------------------------------------        ｜    白名单  
   #                                                                                       ｜   专属规则 
   # [6st-01] -   GeoIP       （VPS所在国家）                                              ｜            
   # [6st-02] -   GeoIP       （全球，按洲际分类）                                         ｜            
   #                                                                                       ｜            
   # ------------------------------------------------------------------------------        ｜            
   #       [第七级] 分流规则 : （不区分国家地区的） 全球性服务  ( IP匹配 + DNS解析)        ｜            
   # ------------------------------------------------------------------------------        ｜            
   #                                                                                       ｜            
   # [7st-01] -   海外 CDN                                                                 ｜            
   #                                                                                       ｜            
   # ------------------------------------------------------------------------------        🔺🔺🔺🔺🔺🔺  
   #       [第八级] 分流规则 :  GFW黑名单（ GFWList ）          ( 域名匹配 )
   # ------------------------------------------------------------------------------
   # 
   # [8st-01] -  GFWList                                        # 未启用 
   #                                                                                       
   # ------------------------------------------------------------------------------        
   #       [第九级] 分流规则 :  回国兜底                       ( 域名匹配 )
   # ------------------------------------------------------------------------------
   # 
   # [9st-01] -  ChinaMax                                       # 未启用 
   #
   # ------------------------------------------------------------------------------        🔻🔻🔻🔻🔻🔻    
   #       [第十级] 分流规则 : 兜底                                                        ｜              
   # ------------------------------------------------------------------------------        ｜    白名单    
   #                                                                                       ｜   专属规则   
   # [10st] -   Final                                                                      ｜              
   #                                                                                       ｜              
   # ------------------------------------------------------------------------------        🔺🔺🔺🔺🔺🔺  
   
```   


<br>
<br>

------



# 更详细的 分流选项（可分流哪些APP）

<br>

```yaml  


# [1st-01] -  DNS \ NTP                                                 
 - { name : '📡.<DNS>—GlobalDNS'                                       
 - { name : '📡.<DNS>—ChinaDNS'                                        
 - { name : '📡.<NTP>—GlobalNTP'                                       
 - { name : '📡.<NTP>—ChinaNTP'                         
                  
# [1st-05] -   反私有DNS跟踪（HttpDNS）  
 - { name : '⛔️.<Protection>—HttpDNS'     
 - 
# [1st-06] -  反劫持（Hijacking）  
 - { name : '⛔️.<Protection>—Hijacking'                  
               
# [1st-08]  [1st-09] -  隐私保护（Privacy） 屏蔽广告 
 - { name : '⛔️.<Protection>—Privacy'                                  
 - { name : '⛔️.<Protection>—ADblock'                                  

# [1st-10] -  UDP 
#- { name : '🎲.<Protocol>—GlobalUDP'                                  
#- { name : '🎲.<Protocol>—ChinaUDP'                                   

# [1st-02] -  局域网（Lan）         
 - { name : '💻.<Lan>'              
                                    
# [3st-01] -  智能设备           
 - { name : '💻.<NAS>—Synology'                                        
#- { name : '💻.<NAS>—QNAP'                                            
 - { name : '🔌.<Home>—AqaraGlobal'          
                           
# [3st-02] -  公有云：云盘、云存储                                     
#- { name : '📂.<Drive>—iCloud'                                        
 - { name : '📂.<Drive>—OneDrive'                                      
 - { name : '📂.<Drive>—Dropbox'                                       
 - { name : '📂.<Drive>—GoogleDrive'                                   
 - { name : '📂.<Drive>—MEGA'                                          
 - { name : '📂.<Drive>—Imgur'                                         
 - { name : '📂.<Drive>—InternetArchive'  
                              
# [3st-04] -  被GFW阻挡的，其他下载站云盘                              
 - { name : '⬇️.<P2P>—PT-Server'                                        
 - { name : '⬇️.<P2P>—eMule-Server'      
                                
# [3st-05] -  需加速 才能流畅访问的网站                                
 - { name : '⬇️.<Download>—MacAppUpgrade'    
                            
# [3st-11] -  金融                                                    
 - { name : '💰.<Finance>—Paypal'                                      
 - { name : '💰.<Finance>—Wise'                                        
 - { name : '₿.<Crypto>—Binance'                                       
 - { name : '₿.<Crypto>—OKX'                                           
 - { name : '💳.<Virtual>—Monzo'                                       
 - { name : '💳.<Virtual>—Revolut'             
                         
 [3st-12] -  各国银行                                                  
 - { name : '🇺🇸.<Bank>—US'                                             
 - { name : '🇨🇦.<Bank>—CA'                                             
 - { name : '🇬🇧.<Bank>—UK'                                             
 - { name : '🇦🇺.<Bank>—AU'                                             
 - { name : '🇯🇵.<Bank>—JP'                              
 - { name : '🇭🇰.<Bank>—HK'  
 - { name : '🇸🇬.<Bank>—SG'  
#- { name : '🇳🇱.<Bank>—NL'  
#- { name : '🇩🇪.<Bank>—DE'  
#- { name : '🇫🇷.<Bank>—FR'                         
                  
# [3st-13] -  专属网站（必须要所属国IP才能正常下单的网站，银行除外…）  
 - { name : '🇺🇸.<HomeIP>—US'                                           
#- { name : '🇨🇦.<HomeIP>—CA'                                           
#- { name : '🇬🇧.<HomeIP>—UK'                                           
#- { name : '🇦🇺.<HomeIP>—AU'                                           
 - { name : '🇯🇵.<HomeIP>—JP'     
                 
# [3st-14] - 不支持VPN的网站（除 银行、HomeIP 分流规则以外的 网站）    
 - { name : '❌.<UnsupportVPN>'              
                           
# [3st-20] -  购物                                                     
 - { name : '🛒.<Shopping>—eBay'                                       
 - { name : '🛒.<Shopping>—Patreon'     
                                
# [3st-21] -  游戏平台                                                 
 - { name : '🕹️.<Game>—Xbox'                                           
 - { name : '🕹️.<Game>—PlayStation'                                    
 - { name : '🕹️.<Game>—Nintendo'                                       
 - { name : '🕹️.<Game>—Steam'                                          
 - { name : '🕹️.<Game>—EPIC'                                           
 - { name : '🕹️.<Game>—GOG'                                            
 - { name : '🕹️.<Game>—RockStar'                                       
 - { name : '🕹️.<Game>—EA.Origin'                                      
 - { name : '🕹️.<Game>—UbiSoft'   
                                      
# [3st-22] -  视频 软件                                                
 - { name : '📺.<Video>—YouTube'                                       
 - { name : '📺.<Video>—Netflix'                                       
 - { name : '📺.<Video>—PrimeVideo'                                    
 - { name : '📺.<Video>—Disney'                                        
 - { name : '📺.<Video>—HBO'                                           
 - { name : '📺.<Video>—FOX'                                           
 - { name : '📺.<Video>—AppleTV'                                       
 - { name : '📺.<Video>—Porn'       
                                    
# [3st-23] -  短视频                                                   
 - { name : '🎬.<Short>—TikTok'                                      
 - { name : '🎬.<Short>—Kwai'                                         
 - { name : '🎬.<Short>—Instagram'          
                              
# [3st-24] -  直播                                                     
 - { name : '🎞️.<Live>—Twitch'            
                              
# [3st-25] -  音频                                                     
 - { name : '🎧.<Audio>—Spotify'                                       
 - { name : '🎧.<Audio>—YouTubeMusic'                                  
#- { name : '🎧.<Audio>—AppleMusic'       
                              
# [3st-26] -  社交                                                     
 - { name : '💛.<Social>—Facebook'                                     
 - { name : '💛.<Social>—Twitter'                                      
 - { name : '💛.<Social>—Reddit'                                       
 - { name : '💛.<Social>—Telegram'                                     
 - { name : '💛.<Social>—Whatsapp'                                     
 - { name : '💛.<Social>—Line'                                         
 - { name : '💛.<Social>—Discord'                                      
 - { name : '💛.<Social>—LinkedIn'                                      
 - { name : '💛.<Social>—Clubhouse'                                    
 - { name : '💛.<Social>—Signal'                                    
#- { name : '💛.<Social>—Teams'                                         
#- { name : '💛.<Social>—Snapchat'                                     
#- { name : '💛.<Social>—Tumblr'                                       
#- { name : '💛.<Social>—Pixiv'          
                               
# [3st-28] -  资讯                                                     
 - { name : '📰.<News>—Wikipedia'                                      
 - { name : '📰.<News>—AppleNews'      
                                 
# [3st-29] -  AI                 
 - { name : '💡.<AI>—AppleAI'                                          
 - { name : '💡.<AI>—OpenAI'                                           
 - { name : '💡.<AI>—Grok'                                             
 - { name : '💡.<AI>—Claude'                                           
 - { name : '💡.<AI>—Gemini'                                           
 - { name : '💡.<AI>—Copilot'                                          
 - { name : '💡.<AI>—GlobalAI'     
 -                                     
# [3st-30] -  工具                                                     
 - { name : '🔧.<Tools>—Adobe'                                         
 - { name : '🔧.<Tools>—Github'                                        
 - { name : '🔧.<Tools>—Notion'                                        
 - { name : '🔧.<Tools>—Pinterest'                                     
 - { name : '🔧.<Tools>—Bing/Edge'                                     
 - { name : '🖥️.<Remote>—Rustdesk'                                     
 - { name : '🖥️.<Remote>—Parsec'                                       

# [4st-01] -  大厂                                                     
 - { name : '☁️.<Apps>—Google'                                         
 - { name : '☁️.<Apps>—Microsoft'                                      
 - { name : '☁️.<Apps>—Apple'                                          
 - { name : '☁️.<Apps>—Amazon'                                        

# [2st-01] -  修改IP归属地   
 - { name : '🇨🇳.<ShowIP>—BiliBili'                                     
 - { name : '🇨🇳.<ShowIP>—抖音'                                         
 - { name : '🇨🇳.<ShowIP>—快手'                                         
 - { name : '🇨🇳.<ShowIP>—小红书'                                       
 - { name : '🇨🇳.<ShowIP>—西瓜'                                         
 - { name : '🇨🇳.<ShowIP>—微博'                                         
 - { name : '🇨🇳.<ShowIP>—知乎'                                         
 - { name : '🇨🇳.<ShowIP>—贴吧'                                         
 - { name : '🇨🇳.<ShowIP>—豆瓣'                                         
 - { name : '🇨🇳.<ShowIP>—闲鱼'                                         

# [2st-02] -  回国 - 网盘  视频  社交  媒体  购物  硬件  大厂  其他    
#- { name : '🇨🇳.<Country>—CN.Drive'         
#- { name : '🇨🇳.<Country>—CN.Video'         
#- { name : '🇨🇳.<Country>—CN.Social'        
#- { name : '🇨🇳.<Country>—CN.News'          
#- { name : '🇨🇳.<Country>—CN.Shopping'      
#- { name : '🇨🇳.<Country>—CN.Hardware'      
#- { name : '🇨🇳.<Country>—CN.BAT'           
#- { name : '🇨🇳.<Country>—CN.Other'                                         
    
# [2st-05] -  回国
 - { name : '🇨🇳.<Country>—CN' 
 - { name : '🇺🇸.<Country>—US' 
   
# [6st-01] [7st-01]                                        
#- { name : '🇯🇵.<Country>—JP'                                          
#- { name : '🇬🇧.<Country>—UK'                                          
#- { name : '🇦🇺.<Country>—AU'                                          
#- { name : '🇭🇰.<Country>—HK'                                          
#- { name : '🇹🇼.<Country>—TW'                                          
#- { name : '🇸🇬.<Country>—SG'                                          
#- { name : '🇳🇱.<Country>—NL'                                          
#- { name : '🇩🇪.<Country>—DE'                                          
#- { name : '🇫🇷.<Country>—FR'                                          
#- { name : '🇨🇦.<Country>—CA'        
                                  
# [6st-02] [7st-02] 
 - { name : '🌎.<Region>—North.America'                                
 - { name : '🌎.<Region>—South.America'                                
 - { name : '🌍.<Region>—Europe'                                       
 - { name : '🌏.<Region>—Oceania'                                      
 - { name : '🌏.<Region>—East.Asia'                                    
 - { name : '🌏.<Region>—West.Asia'                                    
 - { name : '🌍.<Region>—Africa'   
                                     
# [7st-01] -  CDN                                     
 - { name : '☁️.<Global>—CDN'                                       

# [8st-01] - GFW黑名单            
#- { name : '🚧.<GFWList>'                                             

# [9st-01]  - 中国兜底 （ ChinaMax ）  
# 与[2st-05]的 '🇨🇳.<Country>—CN' 相同
 
# [10st-01] - 全球兜底  
 - { name : '♾️.<Final>'                                               

           
```

<br>
<br>

⚠️ 注意 ： 上述被注释掉的，其对应的规则和引用源，也一同被注释了。但都完整保留在模版中，是可以启动的。


<br>
<br>

------



# 默认启用的节点

<br>

> 🇺🇸 美国 “中转” 节点

> 🇯🇵 日本 “中转” 节点

> 🇬🇧 英国 “中转” 节点

> 🇦🇺 澳洲 “中转” 节点

> 🇺🇸 美国 住宅节点（ 落地节点 ）

> 🇺🇸 美国 显示IP归属地（ 落地节点 ）

<br>
<br>

------



# 引用的规则库

<br>

  | 规则库 | 链接 | 说明 | 
|---|---|---|
| GeoSite | https://github.com/v2fly/domain-list-community |  | 
| Additional_Rule_For_Clash | https://github.com/Accademia/Additional_Rule_For_Clash |  | 
| blackmatrix7/ios_rule_script | https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash |  | 




<br>
<br>

------


# 规格说明

以下所有模版，统统为 默认 = “白名单翻墙”（ 即，WhiteList 模式 ） ！！！

<br>

### [通用模版] ：同时兼容 Stash \ Clash Meta


| ⚠️ 基础模版 | 总规则数 | RuleSet规则数 | GeoSite规则数 |
|---|---|---|---|
| [[通用模版]-WhiteList-01.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[通用模版]-WhiteList-01.yaml)  | 12.5 万条 |  9.8 万条 | 2.7 万条 | 
| [[通用模版]-WhiteList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[通用模版]-WhiteList-02-Min.AntiAD.yaml) | 1.9 万条  | 1.2 万条 | 0.7 万条 | 
| [[通用模版]-WhiteList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[通用模版]-WhiteList-03-Non.AntiAD.yaml) | 1.7 万条 | 1.2 万条 | 0.5 万条|


### 配置描述 （通用模版）

  - #### 模版 01 ：[通用模版]-WhiteList-01.yaml  
    
    > 最大特色：
    >
    >  - 防护方面最全面 = 3万条反广告 + 4万条隐私保护 （ 基于EasyPrivacy ）
    >
      

  - #### 模版 02 ：[通用模版]-WhiteList-02-Min.AntiAD.yaml 
    
     > 从 模版 01 中，阉割 了哪些规则 ？ 
     >
     >    + 缩减 RuleSet 规则 ：将 “反广告 + 隐私保护” ，从7.7万条 精简到 1500 条（ 基于Geosite ）
     > 
     >    + 缩减 GeoSite 规则 ：将“成人类网站” 的规则，从 1.3万 精简到 仅十几条（ 成人站中 99.99%规则 是用不到的 ）
     > 
     >    + 0添加 代码 （ 只从 “模版 01” 中 阉割规则 ）
     

   - #### 模版 03 ：[通用模版]-WhiteList-03-Non.AntiAD.yaml 
     
     > 从 模版 02 中，阉割 了哪些规则 ？ 
     >
     >    + 缩减 GeoSite 规则 ：删除了所有的 “反广告 + 隐私保护” 
     > 
     >    + 0添加 代码 （ 只从 “模版 01” 中 阉割规则 ）

   - ⚠️ 注意： 后面的所有模版，都是通过在上述三个模版 ，进行 剪裁、阉割 ，从而得到的。

<br>

### [Desktop]  ：专属 Clash Meta模版 （ 删除了 “Stash兼容” ）  

注意：以下所有模版，都是，通过对 上述《通用模版》进行进一步 裁剪、阉割，从而得到的 （ = 0添加 新代码 ）。只适配Clash Meta内核 客户端

<br>

|  适配电脑 💻 💻 💻（白名单）   | 总规则数 | RuleSet规则数 | GeoSite规则数 |
|---|---|---|---|
| [[Desktop]-WhiteList-01.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-WhiteList-01.yaml)  | 23万条 |  20.3 万条 | 2.7 万条 | 
| [[Desktop]-WhiteList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-WhiteList-02-Min.AntiAD.yaml) | 12.4 万条  | 11.7 万条 | 0.7 万条 | 
| [[Desktop]-WhiteList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-WhiteList-03-Non.AntiAD.yaml) 👌 | 12.2 万条 | 11.7 万条 | 0.5 万条 |


|   适配电脑 💻 💻 💻（黑名单）   | 总规则数 | RuleSet规则数 | GeoSite规则数 |
|---|---|---|---|
| [[Desktop]-BlackList-01.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-BlackList-01.yaml)  | 13.2万条 |  10.5 万条 | 2.7 万条 | 
| [[Desktop]-BlackList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-BlackList-02-Min.AntiAD.yaml) | 2.6 万条  | 1.9 万条 | 0.7 万条 | 
| [[Desktop]-BlackList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-BlackList-03-Non.AntiAD.yaml)  | 2.4 万条 | 1.9 万条 | 0.5 万条 |

<br>

### [Mobile] ：专属 Clash Meta模版 （ 删除了 “Stash兼容” ）  

  #### 注意：以下模版，在上述 “电脑端 模版” 基础上，又又再次裁剪、阉割（ 0添加 新代码 ）。进一步 额外阉割了 “10万条的ChinaMax分流规则” （以便 优化功耗。极致省电 🔥 ）

|  适配手机 📱 📱 📱（白名单）  | 总规则数 | RuleSet规则数 | GeoSite规则数 |
|---|---|---|---|
| [[Mobile]-WhiteList-01.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-WhiteList-01.yaml)  | 12.5 万条 |  9.8 万条 | 2.7 万条 | 
| [[Mobile]-WhiteList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-WhiteList-02-Min.AntiAD.yaml) 🔥🔥🔥   | 1.9 万条  | 1.2 万条 | 0.7 万条 | 
| [[Mobile]-WhiteList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-WhiteList-03-Non.AntiAD.yaml) 🔥🔥🔥   | 1.7 万条 | 1.2 万条 | 0.5 万条 |


|  适配手机 📱 📱 📱 （黑名单） | 总规则数 | RuleSet规则数 | GeoSite规则数 |
|---|---|---|---|
| [[Mobile]-BlackList-01.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-BlackList-01.yaml)  | 13.2 万条 |  10.5 万条 | 2.7 万条 | 
| [[Mobile]-BlackList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-BlackList-02-Min.AntiAD.yaml)  | 2.6 万条  | 1.9 万条 | 0.7 万条 | 
| [[Mobile]-BlackList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-BlackList-03-Non.AntiAD.yaml) | 2.4 万条 | 1.9 万条 | 0.5 万条 |


<br>

### 专属的Clash Meta 模版  ，与 通用模版 什么区别？

纯为了适配的 不同的客户端 ！\[通用模版\] 额外支持 Stash客户端。所以，你下载 [通用模版] 后，你需要更多步骤 的 手工配置才能用起来（可配置性更全面）。所以，其代码容量更大，约 2MB （ Clash Meta 专属模版 只有800KB ）。

 - #### \[通用模版\] ： 同时适配 Stash / Clash Meta
   
   > 不仅要填入节点，还需必须要 按照 [《 如何将 VPN节点，加入到本模版，并导入VPN软件 》](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E5%A6%82%E4%BD%95-%E4%BD%BF%E7%94%A8%E6%9C%AC%E6%A8%A1%E7%89%88-%E5%A6%82%E4%BD%95%E5%B0%86-vpn%E8%8A%82%E7%82%B9%E5%8A%A0%E5%85%A5%E5%88%B0%E6%9C%AC%E6%A8%A1%E7%89%88%E5%B9%B6%E5%AF%BC%E5%85%A5vpn%E8%BD%AF%E4%BB%B6) 进行 五个步骤的 手工配置，才能使用。 

 - #### \[Desktop\] : 纯 Clash Meta 模版 ，给 “桌面端” 使用
   
   > 只需 填入节点 ，即可使用 （ [配置教程](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E5%A6%82%E4%BD%95-%E4%BD%BF%E7%94%A8%E6%9C%AC%E6%A8%A1%E7%89%88-%E5%A6%82%E4%BD%95%E5%B0%86-vpn%E8%8A%82%E7%82%B9%E5%8A%A0%E5%85%A5%E5%88%B0%E6%9C%AC%E6%A8%A1%E7%89%88%E5%B9%B6%E5%AF%BC%E5%85%A5vpn%E8%BD%AF%E4%BB%B6) ）
   >
   > 为电脑设备优化
   >
   >   - 启用了 ： ChinaMax 规则  - 用于 更充分的分流 “中国直连“ （ 启用后， 中国分流 准确度 会提升2-5% ）
   >

  - #### \[Mobile\] : 纯 Clash Meta 模版 ， 给 “移动端、路由器” 使用 （低负载）
     
    > 只需 填入节点 ，即可使用 （ [配置教程](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E5%A6%82%E4%BD%95-%E4%BD%BF%E7%94%A8%E6%9C%AC%E6%A8%A1%E7%89%88-%E5%A6%82%E4%BD%95%E5%B0%86-vpn%E8%8A%82%E7%82%B9%E5%8A%A0%E5%85%A5%E5%88%B0%E6%9C%AC%E6%A8%A1%E7%89%88%E5%B9%B6%E5%AF%BC%E5%85%A5vpn%E8%BD%AF%E4%BB%B6) ）
    >
    > 为手机设备优化 ： 
    >
    >   - 通过关闭 “电脑模版” 中的的 冗余规则，达到 “极致省电” 的目的
    > 
    >   - 关闭了 ChinaMax 规则（ 让规则数量 减少10万条，降低功耗 ）
    >
    >   - 效果：只使用 电脑 10% 的规则数量，达到了电脑 98% 的分流效果。
   
<br>


<br>
<br>

------

#  所有模版 ，选哪一个？

<br>

### 设备 ： 📱 手机、平板、路由器、智能电视 （ = 低算力负载 设备 ） 
 
   - #### 首选 :  ✅ [\[手机\]-WhiteList-02-Min.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-WhiteList-02-Min.AntiAD.yaml) ✅
     
     > 规则数量 ：1.2 万条
     > 
     > 入选理由：🔥🔥🔥 超级省电 🔥🔥🔥
 

   - #### 为什么不选 01 模版？
     > 
     > “模版 01” 虽然更全面，但是在手机会极大消耗电力（规则数量膨胀了10倍），续航➗2。
     >
     > “模版 02” 已经可以屏蔽90%的广告，并且电力消耗 与 “模版 03”（无反广告 无反隐私泄漏）基本持平。
    
     总结：在手机，每次网络请求都要匹配10万条规则，是完全没有必要的🤣🤣。纯粹是冤大头！！！ 用1500条规则的反广告就可以解决90%广告问题，从而换来，一倍以上的续航提升，是非常值得的。（而且iOS还有50MB网络内存限制。为了避免网络内存因过载而崩溃，在规则上做“减法”，也是最佳选择 ）
    
      特别提示：如果你是 🍏🍏🍏 《Stash 客户端》 🍏🍏🍏 ，选 “ [通用模版]-02 ”

<br>

###  设备 ： 💻 个人电脑  
 
   - #### 首选 :  ✅ [\[电脑\]-WhiteList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Desktop]-WhiteList-02-Min.AntiAD.yaml) ✅  +  Adguard 客户端
     
     > 规则数量 ：12 万条
     >
     > 入选理由 ：无 （ 中国分流规则 额外增加10万条 ）
 
   - #### 次选 :  ✅  [\[手机\]-WhiteList-03-Non.AntiAD.yaml](https://raw.githubusercontent.com/Accademia/Clash_Configuration_Template/refs/heads/main/[Mobile]-WhiteList-03-Non.AntiAD.yaml)  ✅  +  Adguard 客户端
     
     > 规则数量 ：1.2 万条
     >
     > 入选理由 ：🔥🔥🔥 超级省电 🔥🔥🔥

   - #### 上述组合 意义是什么 ？
      
      >  将 “翻墙分流” 交给 Clash
      >  
      >  将 “内容过滤” 交给 Adguard
        
     Adguard 用来 “ 防止隐私泄漏 + 屏蔽广告” ，效果 比规则1 更好用。经过长期实测，Adguard客户端（默认规则下）的 误拦截，几乎是0，用了一年多，一次误拦截都没碰上。而 blackmatrix7 的 Clash “反广告+隐私保护” 规则的误拦截，一年多碰见了十几次，为此还做了 修复规则。（ 注意，Adguard 正版是 “买断制付费”， 非国产流氓软件 ）  

<br>
  
 - 总之：规则数量，不是 越多越好 ❕❕❕ 
         

<br>
<br>

------

#  本模版，是 “黑名单模式” ？ 还是 “白名单模式” ？

<br>

### 翻墙模式 ？

 - WhiteList  ：只支持 白名单模式 ❕ 🔥 （ 推荐使用 ！ ）

 - BlackList : 只支持 黑名单模式 ❕

 - 通用模版 ：只支持 白名单模式 ❕


<br>
<br>

------

#  本模版，访问 “🇨🇳中国网站” 时 ， 会不会 “绕路” 到海外 ？ 导致 大量消耗VPN流量 ？

<br>

### 💥 几乎不会❕❕❕

<br>


 -  通过识别 🇨🇳 中国IP ： 让99.99% 中国网站 =  🇨🇳 国内直连  

 
<br>

 -  白名单模式下，为了避免，过量消耗VPN出镜流量。本模版，对🇨🇳中国友好 的国际大厂，默认直连模式（但是，其 AI服务、搜索服务、虚拟机云服务、社交服务 除外），包括

    |  |  | 
    |---|---|
    | 苹果 | 不包含 ：AI | 
    | 微软 | 不包含 ：AI 、搜索 、Auzra云服务、Linkedin、Github | 
    | 索尼 | 仅 Playstation | 
    | 任天堂 |  | 
    | WeChat |  | 
    
    注意， 挑选上述国际大厂的特定服务，允许直连国外，不仅仅因为，避免VPN流量 被过度消耗。还因为，必须释放一些正常海外流量给GFW，让GFW忙起来。不然，如果你连接到海外的所有流量中，除了纯VPN流量，其他海外流量都是0 。那特征太明显、太假了😂。 而这 四个国际大厂 + WeChat，正好是都用是100%正常流量，且系统更新、APP更新、游戏更新的流量消耗 都非常大，而且还有众多海外CDN、国内CDN节点 （ WeChat服务器在🇸🇬新加坡，并没有在🇨🇳中国境内 ），非常适合用于 让自己翻墙的 “白名单特征” 不那么明显 ，从而达到 “明修栈道” 的效果 🤣 

<br>
 
 - ### 用户体验：
 
    我本人已经使用本模版 > 1年 ，自用 IPhone > 1000个国内外APP。样本已经比较充足了。体验 = 完全无感。只会在极个别、极个别、极个别 的情况出现问题，但是也完全无感，只有看了后台之后，才能发现。而且这种下，其链接的消耗流量都极低到忽略不计。

<br>
 
- ### 冷门域名，发生了绕路，怎么办？
     
     - 方案 1 : 通过将🇨🇳 国内域名，加入到本模版的DNS分流策略中：即，在“ nameserver-policy ” 字段中 加入新域名。可秒修复 绕路问题 
     
     - 方案 2 : 在模版中，搜索 ChinaMax ，并且启用其包裹着的源代码 ，注意，只启用以下两处的ChinaMax即可（ 相关原理，在 [如下章节](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E6%9C%AC%E6%A8%A1%E7%89%88%E5%86%85-%E5%B0%8F%E8%80%8C%E7%B2%BE%E5%87%86%E7%9A%84-geositecn--geoipcn-%E7%9C%9F%E4%B8%8D%E8%83%BD%E6%BB%A1%E8%B6%B3-%E6%88%91%E7%9A%84%E5%9C%BA%E6%99%AF%E9%9C%80%E6%B1%82%E6%80%8E%E4%B9%88%E5%8A%9E)有讲解 ）
        >   -  启用 nameserver-policy 中的 ChinaMax（ 620行 左右 ）
        >
        >   -  启用 rule-providers 中的 ChinaMax （ 9680行 左右）
        >
        >   -  强烈建议 ：❌ 不要启用 rule 中的 ChinaMax

<br>
<br>


<br>
<br>

------

#  本模版 访问 “🌍海外网站” 时 ， 会不会 “跨国绕路” ？ 比如 是否会出现 “ 美国落地节点 去 访问日本CDN ” 的情况 ？

<br>

|---| 客户端 |---|
|---|---|---|
| ✅ | Clash Meta 内核  | 100% 不会❕❕❕| 
| ❌ | Stash for iOS  | 可能会绕路 | 

<br>

由于，本模版的 “DNS分流策略（nameserver-policy）”  和  “分流规则（rule）” ，两者是 1:1 互为镜像的。使得本模版，可以100%避免，如 “美国落地节点 去 访问日本CDN” 的情况 ❕ （⚠️注意，此功能为Clash Meta内核独占功能）



但是，为了保证本模版在iOS、Android、Win、Mac之间的通用性，所以，此功能默认关闭。

手动激活方法（搜索如下关键词）：
   - 第一步：在模版中寻找 “ ClashMeta_Only ” 包裹的住的代码，激活源代码（取消其注释）
   - 第二步：在模版中寻找 “ Stash_Compatible “ 包裹的住的代码，关闭源代码（删除或注释掉源代码）
   - 上述两步完成后，此功能便激活。

💥💥💥💥 强烈建议，纯Clash meta用户，激活此功能 💥💥💥💥。 从而彻底解决 海外节点 ”跨国绕路“ 的问题。

而Stash for iOS用户，需要等Stash客户端在DNS分流策略中支持 “Rule-Set” 和 “代理集合” 这两个功能后，才能支持。 本人已经向 Stash开发组 提交过多次反馈。而针对此问题，开发组压根 0反馈 、0回复。🤣🤣🤣 100% 纯血版 已读不回 ～

<br>
<br>

------


#  为什么 本模版 不默认 “黑名单模式”   ❓

<br>

想要 **“跨洋体验 = 本地网络”** ，100% 必须白名单❕
 
 - ✅ “富帅” = 闭眼白名单❕
 
 - ❌  “穷哥们” = 没钱买优质线路 ，才会选 黑名单 🤣 
<br>
<br>

### 👍 白名单 的 五大优势 ：

- ###  理由 1 ：白名单 = 速度快❕
     
     > 跨洋连接时，优质线路 = 花钱加塞 ！！！ 手机直连 🇺🇸美国网站，远远没有通过 “优质9929或CN2线路” 进行中转加速快。尤其是晚高峰，优质线路可以到 60 MByte/s, 而 直连 估计连 6 MByte/s可能都保证不了。还会有抖动。
     
<br>

- ###  理由 2 ：白名单 = 足够省心❕ ❤️❤️❤️
     
     > 黑名单 可能会三天两头 补充规则，不胜其烦。

<br>

- ###  理由 3 ：白名单 = 私密性高❕ 🫥🫥🫥🫥🫥
     
     > 只有白名单模式，才能彻底让GFW的 “深度包检测” 技术归零 ❌ ❕❕❕❕ 才能做到，对GFW、上层网关，完全隐秘 “境外行踪” ✅ 。而黑名单 会被GFW一览无余自己的境外足迹。
     
     > 高私密性的VPN都是白名单。不仅仅在中国，即便是在🇺🇸美国， 美国上市公司，像诺顿、麦咖啡 这些美国顶级杀毒软件公司，在零售市场主推的VPN，也都是白名单VPN。其主要营收，早已不是杀毒软件了，而是白名单VPN、全局VPN，核心卖点就是，基于VPN保护自己网络安全，尤其是私密性，防止被第三方深度包检测 或 防止被检测到自己的网络位置。可以认为，卖点是基于VPN加速的安全通道（或称之为 基于VPN的防火墙）
 
<br>

- ### 理由 4 ：白名单 = 规则数量最低❕ 🔥
     
     > 在本模版中，黑名单模式，规则会膨胀到2.7w条规则。而白名单模式，小于1.8w条规则。减少了接近1万条规则。

<br>

- ### 理由 5 ：白名单 = 🇺🇸 美国数字居民 必备❕ 💲💲💲
     
     > 如果想，避免被 中国政府 全球征税 ？比如， 去美国券商 购买“平均年化10%”的美股指数？开 “活期4%利息” 的美国本土银行账户？最保险的办法，就是白名单翻墙。以免🇺🇸美国银行、券商APP 在某次升级后，加入了新的域名链接，导致你的🇨🇳IP露馅，导致资金账号冻结。
     
     > 运营海外短视频账号，也是一样的规矩。
<br>
<br>


------

#  如何让 本模版 只支持 “黑名单模式”   ？

<br>


只需要在配置模版中：

  - 检索 “**GFWList**” 关键词，然后 -✅启用-  “**GFWList**” 关键词包裹着的代码 

  - 检索 “**WhiteList**” 关键词，然后 -❌注释掉- “**WhiteList**” 关键词包裹住的代码 （ 注意：被 “**WhiteList**” 包裹着的代码，都是白名单专属的分流规则 ）

上述两步之后，你就会得到一个 仅支持 黑名单模式 的模版。

即，没有 “分流选项” 的 ， 100% “直连”。



<br>
<br>


------


# 在 苹果手机 iPhone 上，如何让 本模版 🔥🔥🔥 更加省电 ？

<br>

在 iPhone、iPad、AppleTV 上，目前最好用的Clash客户端是 Stash ： https://stash.wiki/

如果想达到 **最大省电效果** 🔥🔥🔥 以及 **避免网络模块频繁崩溃** ，请在Stash图形界面完成如下配置：
    
  - 设置 -> 网络设置 -> 启用混合网络 （ ❌关闭 ）

  - 设置 -> 网络设置 -> 并发连接  （ ❌关闭 ）    
  
  - 设置 -> 网络设置 -> 允许外部访问 （ ❌关闭 ）
  
  - 设置 -> 网络设置 -> 启用外部控制 （ ❌关闭 ）
  
  - 设置 -> 网络设置 -> 启用Fallback DNS （ ❌关闭 ）
  
  - 设置 -> 网络设置 -> 虚拟网卡模式 （ iOS = 系统原生 开销最低 ）
  
  - 设置 -> 网络设置 -> 包含所有网络 （ ❌关闭 ）
    
以上配置后 ，并发连接数，大幅度降低。对应的 “ 功耗、内存占用” 也跟着大幅降低 ！


<br>
<br>




------

#  本模版 会发生 “DNS泄漏” 么？会限制 “DNS解析” 么？

<br>

不会❕❕❕

<br>

 - 本模版 = **0 DNS泄漏**
 
     > 本模版，任何 🌍 国外域名，都不会向 🇨🇳 中国DNS服务器 发起域名解析请求。为此 ，本模版禁用了 ❌ Fake IP 、 ❌ Fallback DNS 机制 
 
<br>

 - 本模版  = **满血版 DNS解析**
 
     > 本模版 ，禁用了 ❌ no-resolve ，从而达到 满血版DNS解析能力！
         

<br>
<br>


  
------


#  如何 使用本模版 ？（如何将 VPN节点，加入到本模版，并导入VPN软件？）


<br>

本模版开箱即用，你只需要 在模版的源代码中，找到下面 6处  。将你的 VPN节点 配置到下面六处后，即可将本模版 导入到 Clash Meta 客户端 / Stash for iPhone ，开始 🌍 网上冲浪。



```yaml 

###  在模版中， 需修改的 “VPN节点配置”

   # -------------------------------------------------
   # 美国（US） -  📍 修改IP归属地显示                                  
   # -------------------------------------------------

    - { name : 'RT-00—[US.ShowIP]—(归属地落地节点信息)
    - { name : 'RT-01—[US.ShowIP]—(归属地落地节点信息)

   # -------------------------------------------------
   # 美国（US） -  🍟 住宅IP（落地节点）                                  
   # -------------------------------------------------

    - { name : 'RT-00—[US.HomeIP]—(美国住宅节点信息)' 
    - { name : 'RT-01—[US.HomeIP]—(美国住宅节点信息)' 

   # -------------------------------------------------
   # 美国（US） -  🇺🇸 中转                                    
   # -------------------------------------------------

    - { name : 'RT-00—[US-Relay]—(美国中转节点信息)'  
    - { name : 'RT-01—[US-Relay]—(美国中转节点信息)'  
   # -------------------------------------------------
   # 日本（JP） -  🇯🇵 中转                                    
   # -------------------------------------------------

    - { name : 'RT-00—[JP-Relay]—(日本中转节点信息)'  
    - { name : 'RT-01—[JP-Relay]—(日本中转节点信息)'  

   # -------------------------------------------------
   # 英国（UK） -  🇬🇧 中转                                  
   # -------------------------------------------------

    - { name : 'RT-00—[UK-Relay]—(英国中转节点信息)'  
    - { name : 'RT-01—[UK-Relay]—(英国中转节点信息)'  

   # -------------------------------------------------
   # 澳洲（AU） -  🇦🇺 中转                                  
   # -------------------------------------------------

    - { name : 'RT-00—[AU-Relay]—(澳洲中转节点信息)'  
    - { name : 'RT-01—[AU-Relay]—(澳洲中转节点信息)'  

```

<br>
<br> 

### 建议步骤（最佳实践）：  

<br> 
  
  - ### 第一步： 只验证一个节点
    
    > 首次验证时，只使用一个VPN节点，将配置信息，复制到以上六个节点中（注意，只做填空，不要修改节点的name 。观察 ：是否能跑通（ = 境外翻墙成功 + 境内直连 ）

    <br> 
    
  - ### 第二步：验证所有节点
    
    > 如果上一步 验证通过，再将不同国家的VPN节点，配置到上面的六个节点上。观察是否能让，不同APP、不同国家的网站（比如 不同国家 的 显示IP网站），有不同的分流。
      
    <br> 
    
  - 即，上述两步，第一步 = “先验证” 能否跑通 。第二步 = “再验证” 能否复杂分流。
    
    > 验证工具 1 ：https://ip.skk.moe/
    
    > 验证工具 2 ：https://ip.skk.moe/split-tunnel 

    <br> 
    
  - ### 第三步，根据自己的节点位置 整理命名
    
    > 如果前两步 已经验证通过，再根据你的节点信息，对 “ 节点名称 + 中转线路名称 ” 做 批量改名（只改name字段，不改其他配置）。
    
    > 如果你下载的是 “纯ClashMeta模版” 即 [Desktop]/[Mobile] 模版 ，到这一步就结束了 。
    > 如果你下载的是 [通用模版] ，请继续完成后面的步骤。
  
    <br> 
    
  - ### 第四步 ，导入到 Clash Meta 或 Stash 前的必备工作 
      
      - 如果你要将配置 在导入到 Clash Meta 客户端， 请在已完成第三步的基础上，完成本步。在源代码中查找：
          
          > ClashMeta_Only 包裹着的代码 ，启用 ✅
          
          > Stash_Compatible 包裹住的代码，关闭 ❌
          
          ⚠️⚠️⚠️ 对于 Clash Meta核心的客户端 ，强烈建议做上述修改。因为，默认配置 = 只会避免 🇨🇳中国流量 绕路 海外VPN，但是无法避免 海外流量 发生 全球绕路，即，无法避免 日本VPN节点 请求 美国CDN的数据。必须做完上述改动，才能在Clash Meta客户端上避免出现上述 全球绕路 的情况！

    <br> 
      
      -  如果你要将配置 在导入到  Stash 客户端 ，请在已完成第三步的基础上，完成本步。在源代码中查找：
          
          > ClashMeta_Only 包裹着的代码 ，关闭 ❌
          
          > Stash_Compatible 包裹住的代码，启用 ✅

          ⚠️⚠️⚠️ 对于 Stash for iPhone，强烈建议做上述修改。因为，默认配置 = 只能做到stash客户端不报错 + 翻墙基本功能正常工作。但默认配置下，链式代理 在stash客户端上，会 退化为 （与落地机）节点直连。必须做完上述改动，才能让链式代理在stash上生效！当然，如果你无需代理链功能，则这一步可以省略。
        
      - 对于第四步的配置，你什么都不做，也不影响 基础的翻墙上网、基础的分流功能。
      - 如果你做完，前四步，则模版 达到 可被部署、可被导入前 的最佳状态。
         
<br>
   
  - ### 第五步（非必要），中国分流增强（防绕路海外）
     
      - 如果 你是电脑设备（非手机） ，且 你访问的 中国网站 发生了 绕路海外VPN的情况，可以考虑启用 ChinaMax 规则
      
      - 在源代码中查找： 
          
          > GFWList 包裹着的代码 ，启用 ✅  
          
          > ChinaMax 包裹住的代码，启用 ✅
          
          > 在 上述启用 的过程中，建议 “不必启用” 如下规则     
          
            ``` yaml
             - RULE-SET        , GFWList_Domain                             , 🚧.<GFWList>
             - RULE-SET        , ChinaMax_Domain                            , 🇨🇳.<Country>—CN  
             # 原因 ：默认白名单下，上述这些规则都是冗余规则。如果启用了，不会起到效果，反而可能会出错
            ```

      - ⚠️ 注意：仅电脑，可以考虑开启 第五步。而在手机，尤其是在iphone，强烈不建议开启 第五步 。因为开启第五步后，规则数量 会暴增10倍，从1.2万条规则，膨胀到12万条。会导致 触发 iOS 50MB网络内存限制的概率增加，从而导致VPN软件崩溃。而且手机耗电也会大大增加！！
         
<br>
   
  - ### 第六步（非必要+只适合穷人），切换到 “仅支持” 黑名单模式
  
      - 启用方法，在源代码中查找：
          
          > GFWList 包裹着的代码 ，启用 ✅ 
          
          > WhiteList 包裹着的代码 ，关闭 ❌
          
          >  在源代码中查找

        ```yaml
             '+.*'                                              : [ 'https://cloudflare-dns.com/dns-query#♾️.<Final>'                             , 'https://dns.google/dns-query#♾️.<Final>'                                 ]    # [10st-01] 
                
        # 将上述，替换为 ：
    
             '+.*'                                              : [ 'https://dns.alidns.com/dns-query#♾️.<Final>'                                 , 'https://doh.pub/dns-query#♾️.<Final>'                                    ]    # [10st-01] 
         ```


        记住，只有纯黑名单模式，建议使用此修改，因为此修改必然会导致一些不在敏感域名列表中的域名会DNS泄漏，所有的黑名单模式，都会导致DNS泄漏

<br>
<br>

⚠️ 注意：以上搜索过程，请使用 “大小写敏感”模式。

⚠️ 注意，以上流程中， 第五步和第六步中，有些修改，仅针对Clash meta内核才有效，如果你是Stash的iPhone用户，由于有些特性Stash无法支持，所以无法修改的，请略过 也能凑合用 （但强烈建议，去Stash作者那里，发起反馈，然他知道他的软件急需修改）。

最后，以上步骤 + 本模版，只适配了 自建线路（自购VPS）的情况。

<br>
<br>

如果是你的VPN节点是订阅的， 建议使用AI 帮你完成 VPN节点添加 ：

  - 把 “ 模版文件 + 本说明文件 + 你的订阅VPN节点的配置文件” ，上述三者，一起扔给AI，让AI帮你完成，并且要告诉AI，不要修改本模版中，除节点配置信息 以外的任何内容。在AI增加订阅节点信息时，要求AI只做 “增量更新” 。
 
 - 如果你使用AI进行修改，强烈建议，需要用Beyond Compare这样的“源代码比对软件”，对AI的修改结果进行比对。已防止AI不听指挥。记住，在2025年，哪怕你用200美金一个月的ChatGPT 5.x Pro / Agent ，对AI生产的结果，依然必须二次验证，不然100%被坑。
 
 - 如果 你比上述更懒，那建议 你找VPN机场主，让他用本模版帮你添加好，再给你。🤣🤣🤣 毕竟 谁收你钱，谁应该就给你服务 

<br>  
<br>

再次强调：

本模版 =  自用级验证 + 24小时常驻后台 ，所以 100%不会出问题（因为功能单一，如有问题，我自己就发现了）

 也就是说，如果你的导入过程中，出现问题，⚠️⚠️⚠️ 99.999% 只可能是你自己的问题 ⚠️⚠️⚠️ 不是模版问题，不要这里发issue ，建议去问AI。本人 不回答 任何 一般性问题。只，处理BUG、升级功能、收集需求。 

<br>
<br>


  
------


#  纯手笨 + 纯新手 ！ 还是不会使用模版，怎么办？


<br>

⚠️⚠️⚠️⚠️ 如果还不懂，建议，使用AI，回答此类问题 ⚠️⚠️⚠️⚠️ 

<br>

如果你不明白本模版如何使用，请将本模版，扔给AI，让AI给你讲解。我只提供模版、补充必要功能、以及响应bug修复，不回答一般性问题。 ⚠️⚠️⚠️⚠️ 

 > 1️⃣ 向AI提问的提示词 ：如何 将自己的VPS节点 添加进 这个模版  并导入Clash Verge Rev软件？

 > 2️⃣ 然后，将本模版作为附件，扔给AI。强烈建议，使用 ChatGPT 5.1 Pro ，让AI 将 “你的节点、存量规则 。本规则” ，上述三者做融合。 并且，你要给AI讲明白，你想达到什么效果。越细致越好。

 > ⚠️ 注意：经过对比，在处理模版到实际规则这一块，Grok 4.1 、 Gemini 3 Think ，都远远达不到 ChatGPT 5.1 Pro 的效果（包括 ChatGPT O3 Agent 目前也不行，其处理 有些emoji 会乱码 ）❕❕❕❕❕

 > ⚠️ 注意：一定要使用 海外AI + 付费AI！千万别用 🇨🇳国产AI， 更 别用海外免费AI ❕ 别用免费AI ❕ 别用免费AI ❕

此模版，本人已在Stash、Clash Verge、其他Clash Meta核心的VPN工具上 ，使用了一年多，而且是24小时不关闭，功能上是没有问题的 ！

再次声明：我只提供模版、补充必要功能、响应bug修复、兼顾需求收集 ，但 100% + 100% 没有以下服务 ，包括 ：
  
  - 💥💥💥💥 不回答 一般性问题 💥💥💥💥
  - 💥💥💥💥 不响应 保姆式请求 💥💥💥💥

 所有 “入门教程” ，都已经平铺在本文当中。能看懂就看，看不懂问AI。本人不响应 保姆请求 和 教学请求。

<br>

How to use this template ? (How to import this template into VPN software?)

If you don't understand how to use this template, please throw this template to AI and let AI explain it to you. I only provide templates, supplement missing very necessary functions, and respond to bug fixes, and do not answer general questions.

<br>
<br>

------


#  推荐的 节点协议 ：

<br>

| 线路 | 推建议协议 | 说明 |
|---|---|---|
| 优质线路  | Vless + Reality + Vision + XUDP | 优质线路使用 Hysteria2 ，100%会降速  | 
|  劣质线路 | Hysteria2 （ 歇斯底里2 ） | 中美的劣质线路（如10美金一年不限流量的线路）使用Hysteria2，往往晚高峰能 10MByte/s，其他协议 0.1 MByte/s  | 

<br>

推荐 “自建 优质节点” 的 首选地区 ：
 
 >  🇺🇸 美国
 
 >  🇯🇵 日本
 
 >  🇦🇺 澳洲
 
 >  🇬🇧 英国
 
 >  🇪🇺 荷兰\德国 

 
<br>

### 请不要再如下条目中，加入 🇭🇰 香港节点 ❕


```yaml
    - { name : '🔰⚡.Line—[Relay.VPS]—Low.Latency'
```
  
  -  因为 🇭🇰 香港IP ，在很多 🇺🇸 美国APP 中，会与 🇷🇺 俄罗斯、🇧🇾 白俄罗斯、🇮🇷 伊朗 、 🇨🇺古巴 等其他流氓国家的IP 待遇相同，被禁止连接。 而本模版中，很多国外APP会使用到上面这个代理集合，来优化访问速度，如果你在这里，填入香港节点，会导致有些对中港澳IP ，以及对 俄罗斯等其他流氓国家IP ，进行风封锁的APP无法使用。
  
  -  未来，香港IP 在全球，只会越来越受歧视，所以 强烈不建议 购买香港节点，作为 “落地节点” 。 
  
<br>
  
### 原则上来说，本项目已经 放弃适配 🇭🇰 香港节点 ⚠️ （ 力求省心 + 0频繁维护 ）


<br>
<br>

------


#  🍎 iPhone 、iPad 用户 必看 ：

如果你是iPhone用户，💥💥💥💥  强烈建议 ： iOS APP <  800个 💥💥💥💥

在iOS、iPadOS上，APP数量超过800个，会导致VPN切换速度变慢，如果超过1000个APP，会导致严重的切换延迟，最长可以高达1小时以上（本人亲测实锤）。而且切换过程中，会一直处于断网状态 😂 。而且手机会变得巨烫，哪怕你退出所有APP，也依旧掉电飞快。 而且，哪怕关闭iOS上所有后台任务，还是问题依旧。这个BUG，已经有很多老外反馈在苹果官网，前后长达十年以上，可苹果压根不想修复（估计能装超过1000个APP的用户太少）。

面对上述问题，最好的方法，就是控制iOS上安装的APP数量。

> 对于快速切换VPN状态（如从蜂窝网VPN -> 切换到WIFI VPN）来说，⚠️ 800个APP是条安全线 ⚠️ 

如果出现此问题，不是模版的问题。这是苹果手机的BUG。

<br>
<br>

------


#  OpenClash 路由器 用户 必看 ：

<br>

本模版，可以 完美兼容 OpenClash 、OpenWRT 路由器。但是我不建议直接部署。我仍旧只建议：

  > 本模版部署在 可信任 的 终端 （如 手机、PC）

  > OpenWRT 路由器 ，只使用 GFWlist黑名单上网（不搞分流），并且部署 < 1-2个节点（做灾备）。


<br>

### 为什么？

为了将 “安全冗余” 拉满  +  “维护成本” 降至最低 ！

因为🇨🇳国产IOT设备，都是不可信的。即，只要你家局域网中的 IOT 设备， （通过反诈插件）跑几个简单的 预设黑名单，就能标记出，你在OpenClash路由器上配置的分流规则中的所有VPN节点IP，然后如果它上报给GFW，那你家所有VPN节点IP都会被阻断。🤣🤣 你马立刻100%傻眼，如果在同步给辖区派出所上门查扣设备，您就喜提3000元罚款吧。而且技术上非常简单，比如，通过如下网页，轻易就能知道到节点信息，然后秒上报给GFW：
 - https://ip.skk.moe/split-tunnel
 - https://ip.skk.moe/multi
 - https://ip.skk.moe/

很多人会说，我家没断网，我一直用的很好，我不觉得有问题。🤣 100% 纯0风险意识。试问，GFW要这么部署，不比 深度包检测 效果好1000倍 ？？？ 你说人家动力有多大 🤣 简直就是分分钟定位所有VPN IP的黑科技（对于非链式代理）。

而且目前。国产路由器、国产光猫已经内置 “反诈插件” 了。下一步，你家的IOT设备，尤其是华为设备，通过OTA升级部署 “反诈插件” ，就只是时间问题。像联通赠送的家庭摄像头、国产智能电视机、扫地机器人、智能中继、甚至你家智能冰箱。这些设备都是“反诈插件”的优质载体。总之，你要记住，你家局域网，不属于可信度高的网络，你在局域网最顶层总出口布置 OpenClash分流，纯属无知者无畏。

而且，你家局域网不是高可信度网络，可不仅仅是反诈插件，局域网内的智能设备，如果感染病毒，那对VPN节点也是巨大威胁。比如，中毒设备 如果通过OpenClash路由器配置的VPN节点疯狂转发垃圾邮件， 那你VPN节点 ，也会立马报销 🤣 。尤其是像智能电视这种可安装第三方APP的设备，非常容易被病毒程序攻击 、被远程安装病毒APP。其易被感染程度，就像你用你安卓手机上的“电视助手APP”，给你家电视装APP一样容易。其实，很多人家里的智能电视，早都已经被入侵了，只是你没察觉。这些被入侵的电视机，只会在必要时会成为DDOS源，在平时，你家电视也大概率会间歇性的发送垃圾邮件（流量消耗极低，你在路由器的流量监控中，根本看不出来有问题）。这些都是99.999%的人观察不到的。像我有个朋友，家里的索尼9系（顶配）电视机，国际大牌，依然会中毒，而且反复 “恢复出厂设置” 多次，依然不管用，每次好个几天，隔一段时间又会被感染了🤣。当然，如果你不是专业级的，你100%完全察觉不出来中毒，因为病毒几个小时、几十分钟才会不定期才发送一批的垃圾邮件。这些病毒，在发送垃圾邮件的过程中，如果匹配到了你部署在OpenClash路由器上的的规则，如果使用了你的VPN节点发垃圾邮件，会导致你的落地节点瞬间被封禁。

所以，无路从哪个角度来看，都强烈 不不不不不不不建议，把所有节点和规则，都配置到  “家庭总出口” 的路由器上。

<br>

### 面对上述情况，怎么办？

分层！ 必须以 “分层” 的方式，部署VPN ！才能，达到 最省心（0维护+抗损毁）的效果。 如下：

 > 第一层：路由器上，只使用 “GFWlist黑名单”  +  “1～2个节点” 。以便能实现基础的外网访问功能。 以便 规则损坏时可以正常上外网，以及智能电视可以访问Youtube。用尽量窄的规则和尽量少的节点，将 损毁代价 + 损毁风险 降到最低。
 
 > 第二层：PC、手机上，才使用 节点全集 + Clash Meta 分流全集。
 




<br>
<br>

 ------

#  我是 俄国、伊朗 等 用户，如何修改模版 ？

<br>

如果你不在中国，而是在俄罗斯、白俄罗斯、伊朗、朝鲜、古巴、中亚五国，等其他**流氓国家**，你 仍旧可以将本模版扔给ChatGPT Pro，让他给你修改。最简单的方法，就是将模版中的 “**第二级**“，从中国改为你所在国。

<br>


If I am not a user in China—such as in 🇷🇺 Russia, 🇧🇾 Belarus, 🇮🇷 Iran, 🇰🇵 North Korea, 🇨🇺 Cuba, or the 🇰🇿 Central Asian countries—how should I modify the template?

If you are not located in China but instead in rogue countries like Russia, Iran, Belarus, North Korea, Cuba, or the Central Asian states, you can still give this template to ChatGPT Pro and ask it to modify it for you.The simplest method is:

  - In the template, replace the “second-level region（ 2st ）” from China to the country where you actually live.



<br>
<br>
<br>
<br>
<br>
<br>


------

------

------

 #  💾  下面章节：讲解原理 +  购买节点 如何避坑
 
------

------

------


<br>
<br>

<br>
<br>



<br>

<br>


# 如何魔改本模版，从而做到 进一步省电？

<br>

首先，如果使用白名单模式，还可以将glwlist相关的规则都注销掉。可以将规则数量，减少7000条

其次，本模版，其实同时内置了两组规则： Ruleset规则 和 Geosite 规则。 如果想进一步省电，请删除其中一套规则（ 并且删除其对应的rule-providers ）。

> 这样可以将，总规则数量，可以再次➗2（规则02的规则数量，从 2.8万 下降到 8000条），同时，几乎不会降低分流能力。从而进步一省电。也就是说，这两者是互为冗余部署的。

> 注意：Stash 对于Geosite规则的处理效率（耗电），远远优于（使用Classical的）Ruleset规则。
    

<br>
<br>

------

# 为什么 本模版 ，在单一分流规则上，同时冗余部署了 两套 远程规则 ？

<br>

为了 省心 + 0频繁维护 ❕

  > 通过冗余部署，两套远程规则（Rule-Set + Geosite ），避免因某一个规则库停止更新（或更新慢），而导致，使用者频繁手动维护yaml。

<br>
<br>

------

# 为什么 “省电” 和 “防止DNS泄漏” 如此重要 ？ 


<br>


🔥 🔥 🔥  **省电** + **避免DNS泄漏**  ，是本模版的 最优先的目标 ❕❕❕❕ ⚠️⚠️⚠️  

<br>

  - 要省电是因为，在iPhone上，往往的VPN软件电量消耗，**占整机电量消耗的20%**（VPN永驻后台不关闭）

    + 所以，必须在分流规则的安排上，就考虑到如何省电 ！！！
    
    + 所以，在本模版规则中，被一般用户，最频繁使用的国内分流（回国分流），被安排在最前面。而且极大精简了前置的广告规则。而命中率更低的海外规则，被安排在了上述两者之后。
    
    + 从而，杜绝要匹配上万条规则、甚至十万条规则，才发现是国内直连的情况。后者这种写法，100%冤大头 ❕❕❕
  
<br>

  - 要避免DNS泄漏是因为，避免让 上层监控路由器（如校园网出口）、运营商、GFW 等 监测到 ，如下两种行为

     + 使用 “国内DNS” ，解析境外域名，但是又没有 境外域名的流量。
     
     + 使用 “境外DNS” ，解析境外域名，但是又没有 境外域名的流量。
     
     + 上述两种行为，**一旦被监测到，会被判断，你100%在用境外节点翻墙** 
     
     + 总之，避免DNS泄漏，是 “白名单模式” 中的第一环，也是最为重要的一环 ❕❕❕❕

    + 想避免DNS泄漏，必须要做到：只有在白名单内的中国网站，才会向🇨🇳中国国内的DNS 发起域名解析请求。不在白名单内的网站，一律通过 VPN节点，转发给 境外DNS进行解析。且两者全程都是DOH加密格式。才能保证100%不会发生DNS泄漏！

<br>
<br>


------


# 本模版，如何在规则级 ，解决 ”省电“ 问题 + 解决 ”iOS网络内存频繁崩溃” 问题 ？

<br>


如何 “省电” ，按优先级排序： 

   > 关闭并发优化选项
   
   > 减少DNS服务器数量
   
   > 减少重复DNS请求 （如 fallback DNS）
   
   > 避免频繁的延迟检测
   
   > 避免高频命中的规则排在最后（如中国直连，不应该排在最后，应该排在最靠前）

   > 对于反广告，尽量不用REJECT （改用REJECT-DROP）
   
   > 减少大而全的反广告规则数量
   
   > 避免引用classical 规则集合，尤其是，必须🈲禁止引用超过1000条以上的classical规则，一定要改用 domain / ipcidr 的yaml远程规则集合。
   
   > 避免基于条件判断的复杂规则

<br>

对于上述 排序，进一步解释：

<br>

1. ### 多DNS查询，可能会导致iOS的VPN频繁崩溃.

    - 在iOS上，多DNS查询会导致内存爆炸（超过iOS的50MB限制），从而导致VPN崩溃。如果遇到这种情况，请删除一个DNS，只使用 1.1.1.1 。多DNS查询，会成倍增加内存使用。本模版使用了2个DNS 1.1.1.1 、8.8.8.8

<br>

2. ### 慢速VPS节点，可能会导致iOS的VPN频繁崩溃.

    - 在iOS上，如果你的VPS节点过于慢，可能也会导致DNS查询时，内存爆炸（超过iOS的50MB限制），从而导致VPN崩溃。如果遇到这种情况，请将DNS查询指定到更换更快的VPS（哪怕带宽低都不怕，只要速度响应快）。
    
    - 本模版，会通过每900秒一次的全自动ping，选取你VPS代理池中，延迟最的VPS代理DNS请求。

<br>

3. ### 以下两个特性要谨慎使用，在iOS会对电池消耗和内存占用导致很大影响

   - tcp-concurrent            : false     
      不建议ture，因为开启后会导致手机费电、并且导致iOS内存占用增加30%，而且耗电严重

    - interval                  :  900      
      不建议太频繁进行 “心跳测试”，这里设置为 15分钟=900秒 测试一次，否则耗电严重

<br>


4. ### 优先使用 REJECT-DROP
  
   - 对于 “反广告 + 隐私保护” ，（从“省电”角度）优先使用 REJECT-DROP，而非REJECT。因为后者会潜在导致app疯狂重试连接服务器。进一步导致手机发烫、极其费电。尤其是上报用户行为的链接。



<br>
<br>


------


# 本模版，如何实现 “就近分配” 逻辑  ？

<br>

 ### 如何实现 ，按地理位置 就近分配 VPN节点 ？

  对于 “有” 地理位置的的网站，如 各国顶级域名的网站、有本国IP地址的网站，本模版通过自制的，如下两套规则集合，实现就近分配VPN节点

   > GeoRouting_For_Domain
  
   > GeoRouting_For_IP

<br>

 ### 如何实现 ，按 VPN节点位置 就近请求 CDN ？

   对于 “无” 地理位置的网站，支持 落地节点 自动选取最近的CDN 获取网站数据数据 。以便 境外流量 能100%避免，如 “🇺🇸美国节点 访问 🇯🇵日本CDN” 等 “全球绕路” 的情况。

   要实现上述效果，本模版通过在 DNS分流策略 中 （ 即，在“ nameserver-policy ” 字段中 ） ， 1:1 复刻 分流规则（Rule）中的 大部分 分流配置 而实现的。也就是说，手动分流DNS请求到指定的VPN节点上（ 如 美国节点），而实现了100%避免，如 “🇺🇸美国节点 访问 🇯🇵日本CDN” 等 “全球绕路” 的情况


<br>
<br>

------


# 本模版，如何解决，白名单模式下，精准分流 “🇨🇳中国境内流量” 不绕路的 ？

<br>

### 原理讲解：

-  首先：🇨🇳中国域名 = 白名单解析
    >  目标：必须让 🇨🇳 中国网站，只能解析到🇨🇳国内IP，避免其解析到境外CDN的 IP。
    >  方法：通过在 “DNS分流策略” 中，使用 白名单机制（geosite:cn）。让国内网站的域名，直连国内DNS，从而解析到国内IP地址。
         
-  其次：🇨🇳 中国IP = 白名单分流
    >  目标：必须让（上述DNS解析后的）🇨🇳国内IP地址，直连中国大陆。
    >  方法：通过在 “分流规则” 中，使用 白名单机制（geoip:cn）。使得 访问🇨🇳国内网站 ，不会绕路到国外。
 
- 最后：而对于，不包含在 “DNS分流白名单” 中的冷门网站，会不会绕路 ？ 
    > 几乎不会！因为，越是冷门小众，100%越是用不起海外CDN（ 穷 + 核心受众在国内 ），或者压根不屑于用海外CDN（比如 医院 大学 政府）。在这种情况下，你在外国DNS请求域名解析，一样返回的是中国IP。只要是🇨🇳中国IP，就会通过geoip:cn分流到 “直连”。
    

通过上述，实现了，几乎0绕路。所以，核心是有一个好的 “🇨🇳中国域名 白名单”，是整个规则设计的关键❕

### 规则集合：

目前，给 🇨🇳中国区做域名分流的远程规则集合 ，主要有以下两个最具代表性的项目 ：

|  | 规则数量 | 链接 |
|---|---|---|
| geosite:cn  | 6800条 |  https://github.com/v2fly/domain-list-community | 
| ChinaMax  | 12万条 |  https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Surge/ChinaMax | 
 

上述两个 规则集合 ，本模版 都没用 ！ 核心原因：精度太差 ！

   > geosite:cn ，包含2000条错误规则、冗余规则。接近500多条境外IP的域名，却被收录成了中国域名。最离谱的是，居然把TikTok，都标记为了中国域名 🤣🤣🤣 。而且，还有超过1300条冗余的.cn域名也被收录。这里还没有计算有些域名已经是完全死链接的状态，也应该被剔除的，却还在滥竽充数的。
   
   > ChinaMax ，错误规则数量，问题更大，包含超过2万条 规则错误（仅做初步排查，并非全部错误规则），具体可以看这里 ： https://github.com/blackmatrix7/ios_rule_script/issues/1615

总之，目前 上述两者, 都做不到100%精准。

<br>

由于本模版，是白名单模式，并且，中国区分流的匹配，被安排到了的境外流量分流之前（几乎是分流过程中 第二靠前的位置）。所以，本模版对于🇨🇳中国区的规则集合，其 容错度极低。必须要求 中国区规则集合 要非常精准才行。而且必须精准到，宁可错漏不能错配。但目前市面上，没有可用的高精准规则集合。

导致 不得已，只能用自己的方案。做了针对geosite:cn修复错误后的规则:

 - https://github.com/Accademia/Additional_Rule_For_Clash/tree/main/GeositeCN

上述这个魔改规则集，将原本geosite:cn中6800条规则，进行清洗后，保留了4800条 100% 准确的规则。足够用了。对于不在上述魔改规则内的域名，直接进行DNS解析，然后上 geoip:cn 进行补门操作，达到100%完美 ！ 由于本模版 无DNS泄漏，所以用geoip:cn 无任何压力。

实际上 ，在本模版中，DNS策略 与 分流策略，共用同一套 ，中国区分流的 规则集合。

<br>

我还是那个观点！⚠️ ⚠️ ⚠️ 规则数量 不是越多越好！！ NB，体现在做减法。在非核心目标上，不断做加法，摊大饼、大而全， 没有意义。本套模版的最核心目标是 “省电”  。其次是（针对上层网关）隐秘行踪。而不是 ，一次性，堆十几万、二十几万规则，导致每此域名请求都要比对十多万规则。这样只会让手机续航➗2。做的都是无用功。

<br>

总之！未来，在Geosite官方修正BUG后（达到本模版需求的精准级别后），本模版会再及时替换回官方的规则集的。

<br>
<br>


------


# 为什么 原版 geosite 、 原版 ChinaMax 会不精准？ 什么级别的精准，是本模版 对 “精准需求” 的 “及格线” ？

<br>

要评价，精不精准，先要弄明白，如何定义精准 ？  或者说，到底什么样的域名，才能被放进 🇨🇳 中国分流规则 当中？

1. 在中国大陆，有根dns的 “域名” ，是否是 中国域名？
    
    > 这里面会包含 🌍 境外域名，甚至被gfw阻断的境外域名

2. 在中国大陆，能直连的 “域名” ，是否是 中国域名？
    
    > 这里面也会包含 🌍 境外域名，但只包含没有被gfw封锁的境外域名

3. 中国公司的 “域名” ，是否是 中国域名？
    
    > 这里面也会包含 🌍 境外域名，但只包含中国公司自己运营的境外域名 ，如快手国际版 kwai、 抖音国际版 tiktok

4. 被中国GEOIP命中的 “域名” （IP归属地显示为中国的域名），是否是中国域名？
    
    > 这里面也会包含 🌍 境外域名。但只包含 在中国cdn服务器的境外域名。


对上述四种，

- 最精准的 = 类别 4  

- 原版 geosite:cn = 类别 3

- 原版 ChinaMax = 类别 1

但以上就是全部标准么？

<br>

答案是否定的 ⚠️ 我们需要的 高精准度的 “中国分流规则集合” ，应该是 还满足如下几个条件：
    
 1. IP归属地 = 中国大陆地区 的域名。即，这个域名的N个IP解析结果中，哪怕有一个IP的归属地是🇨🇳中国大陆地区的，都可以算。
 
 2. 域名后缀，如果是非大陆地区域名 的 ，如.hk .tw .us，这种其他地区、其他国家的，应被排除在外。
 
 3. cdn域名中，凡事带有 eu- \ us- \ hk- ，等明确地理位置的子域名的，也应该被排除在外。
 
 4. 虽然可以满足以上所有要求，但是被收录后，其域名对应的海外APP无法使用的，也应该被排除还外（如 Tiktok、Kwai 所用到的某些域名）

对以上四者 取交集。才应该是 100%精准、100%无错误 的 “🇨🇳中国分流规则” 所需要的域名。才可以被前置使用，从而优化耗电。避免 因前置几万、十几万境外分流规则，把你iPhone的电力耗光。 本模版使用的 清洗后的GeoSiteCN ，正是按照这个标准制作。

<br>
<br>

------


# 本模版  对 “🇨🇳中国分流” 规则集，容错度极低，是缺陷么？

<br>


本模版对中国分流的规则集合，精准度要求极高（或称 容错率极低），不是缺陷，而是设计目标！

本模版 “最”核心目标 只有一个 ：

 - 🔥🔥🔥🔥 省电 属性拉满 🔥🔥🔥🔥

如果想最大化省电，那必须让最高频命中的规则，放在最前面。而“🇨🇳中国分流” 就是最高频命中的规则。所以，此规则集合必须前置。但前置的代价，就是要求规则必须精准！容错度就越低！ 实际上，在分流规则排序中，越靠前必须越精准！

如果将中国区分流规则，放在境外分流之后，那的确可以大大降低对其精准度的需求（大大提高容错度）。而在这种情况下，目前上述两个规则集合，都是可用的。

但这会大大增加命中前的匹配次数，每次命中都要比对几万条、十几万条，才能发现是日常用的，必须直连的 国内IP。100% = 0价值费电！对于 iPhone和其他手机的 “续航” ，完全是 “不必要的代价”

作为一个 “面向手机” 的 Clash模版 。在非核心目标上，必须做减法。

<br>
<br>

------


# 本模版内 小而精准的 GeositeCN + geoip:cn 真不能满足 我的场景需求，怎么办？

<br>

### 有2种 修改方案：
 
 |--|--|方法|优缺点|
 |--|--|--|--|
 | 方案 1 |   仅图形界面操作 | 将你认为绕路的🇨🇳中国APP，添加进旁路  | 只有安卓的客户端，支持此功能 |
| 方案 2  | 修改模版  |  同时使用 GeositeCN + ChinaMax ❕ 在DNS分流策略中， 将ChinaMax分流规则，添加到兜底规则前。 | 容错度 最高，效果 = 随便错 都不怕 🔥🔥🔥 但 内存消耗爆炸 ❕ |
  
<br>


<br>

### 方案2 的优缺点：

  - GeositeCN = “高频使用” 的 “直连国内🇨🇳规则” 。被前置到分流规则的前部，从而避免，要比对（超过几万条规则）境外规则，才发现是平时常用的直连的情况。从而大大降低了耗电❕❕❕
  
  - ChinaMax = “低频使用” 的 “直连国内🇨🇳规则” 。 被后置到 兜底规则之前。做二次排查。由于，海外访问都已经分流走了。剩下的大概率是中国域名了、或非GFWlist敏感的国外域名了。此时，可以说 ，几乎能随便错，随便泄漏，都不怕。
  
   等于说，那 GeositeCN 做一级高速缓存 （高频 + 高精准度），那 ChinaMax 做二级缓存 （低频 + 精准度稍低），
   -  特别注意 ⚠️ 上述两者，仅仅在 Nameserver-Policy DNS （DNS分流策略）中启用 ⚠️，并且 指向 🇨🇳 中国DNS。也就是说，通过Nameserver-Policy DNS（DNS分流策略），如果解析到的是中国IP，才会在后续的 Rule（分流规则）中，通过 geoip:cn 直连。通过上述 多级缓存 多层套娃，从而，最大化的清洗掉ChinaMax中的 个别错误数据。

   虽然，上述的两级缓存机制，避免了 “功耗爆炸” ，但是 “内存爆炸” 无法避免。由于iPhone （ iOS 26 ）目前只有 50MB vpn网络内存。所以，在iOS手机，依旧不建议开启。电脑、路由器，不怕费电的，则可以部署。
  

<br>

### 如何 启用 ✅ 此功能？

  - 启用方法，可以跳转到 如下章节，找寻 第五步 操作 （启用 ChinaMax 规则） ：
  [《 如何 使用本模版 ？》 ](https://github.com/Accademia/Clash_Configuration_Template?tab=readme-ov-file#%E5%A6%82%E4%BD%95-%E4%BD%BF%E7%94%A8%E6%9C%AC%E6%A8%A1%E7%89%88-%E5%A6%82%E4%BD%95%E5%B0%86-vpn%E8%8A%82%E7%82%B9%E5%8A%A0%E5%85%A5%E5%88%B0%E6%9C%AC%E6%A8%A1%E7%89%88%E5%B9%B6%E5%AF%BC%E5%85%A5vpn%E8%BD%AF%E4%BB%B6)

原则上来说，在iphone上，不建议启用此功能，会使得本模版的 模版02，从（关闭GFWlist后的）1.2万条规则，扩展为12万条。增长了接近10倍规则。而且都是极低频的中国域名，估计里面90%的域名，是你这辈子都用不上的中国域名。纯属 让你的 iPhone =  拉低性能 + 纯暖手宝模式。

<br>

### ⚠️ 关于ChinaMax规则：

本模版引用的ChinaMax是经过 粗粒度清洗 的（ 非原版 ChinaMax ），删除掉了1.8万条错误规则（原版11.7万条）。

清洗后的 ChinaMax 项目地址如下：
  - https://github.com/Accademia/Additional_Rule_For_Clash/tree/main/ChinaMax

 🔥🔥🔥 像ChinaMax 这种 ，100%草台级 散装规则。真的是垃圾。看了一下， 想覆盖的 覆盖不到（主流APP 依旧不能100%覆盖），99%的人 压根用不上的网站（如各种抽奖类网站、2345流氓网站、营销网站） 占据巨大容量 滥竽充数。以后最好能让AI 定期 在虚拟机、沙盒中 模拟人真 使用国产APP，然后定期 自动为每个国产APP更新规则集，从而汇总 国产APP规则，进行分流，比ChinaMax这种收集一堆 野鸡个人站、抽奖站、营销战、广告站的规则 强100倍。

<br>
<br>

------


# 关于 Geosite ，给 Clash Verge Rev 、 Stash 开发者社区 的建议

<br>

想一劳永逸解决 GeoSite的问题，必须让Clash、Stash、Surge 这样的软件，能够支持，用户能一键导出 自己的 “域名解析记录” （比如过去两年内）。然后，支持用户 一键测试 ：用本国DNS，测试这些域名 是否指向国内IP。测试后，为用户生成 用户自己本地的Geosite:CN。做到完全贴合用户的日常浏览网站 = 0增加无效规则数量 + 又极致省电。

而不是让用户，在VPN上，时时刻刻都挂着 10多万条的ChinaMax规则。使得每一次网络请求，都比对十几万次，才能命中。这纯脆是0价值费电。

当然，用户也可以将自己的本地的Geosite:CN规则集合，分享给社区，从而使得社区，可以更低成本的完善 规则集合汇总，可以集腋成裘。极大减轻社区制作规则集的压力❕❕❕ 并且不仅仅对中国的VPN社区极有价值。 对 俄罗斯、朝鲜、伊朗 等其他流氓国家的VPN用户（尤其是 几乎0社区的用户群），一样非常有价值。

<br>

多说一句。从使用体验上来看， 像geosite:cn 这种基于泛LBS概念的分流规则， 给 ”dns解析请求“ 分流的价值，至少十倍于 给其他类型的网络请求。因为你像哪个DNS请求，就已经决定了你要访问的IP在哪里（国内还是国外），后面在怎么分流 ，也改变不了这个带来的体验差异。


<br>
<br>

------


# ‼️‼️ 为什么 必须完全禁用 ，官方推荐的 “ Fake IP + Fallback DNS + no-resolve ” 组合？

<br>

防DNS污染，目前，有两种方案（二选一）：

  - ### ❌ FakeIP + Fallback DNS + no-resolve 

    > “Fake IP + Fallback DNS + no-resolve” （不推荐使用）。这是 上一代 防DNS污染 技术 ：其同时向 “国内 国外 DNS” 发起域名解析，然后让国外DNS 给结果纠错，从而避免DNS污染。 

  
  - ### ✅ Redir-Host + Nameserver-Policy DNS
  
    > “Redir-Host + Nameserver-Policy DNS” （推荐使用）。 这是 最新一代 防DNS污染 技术 ：其通过 域名黑名单（如 geosite:cn）控制，只有中国域名才会请求中国DNS，非名单内的域名，一律当作海外域名请求海外DNS解析 。从而避免DNS污染。

<br>

### 🆚 “Fake IP + Fallback DNS + no-resolve” 的优缺点

 1. 缺点 ❌ ： Fake IP 的 VPN特征明显
    
    > APP 内置的 “商业级 反VPN SDK” ，会通过识别Fake IP，识别到使用了VPN，从而强制退出APP（如，某些银行类APP）
 
 2. 缺点 ❌ ：Fake IP 极不省心 、干扰正常使用
    
    > Fake IP 还会造成 大量的兼容性问题，为了解决兼容性问题，还需要给它设置过滤列表（添加各种例外，尤其是在路由器上部署时），需要频繁手动维护，不胜其烦 ❕❕❕

 3. 缺点 ❌ ：Fallback DNS 会造成DNS泄漏
    
    > Fallback模式下的DNS请求，会先去国内DNS请求，然后再去海外DNS验证。这种机制 100%会造成DNS泄漏。
    
 4. 缺点 ❌ ：no-resolve 阉割DNS解析能力
    
    > 官方指导中，还推荐给分流域名都添加 no-resolve约束（禁止DNS解析），那意味着 不能调用IP（GeoIP）进行分流 。🤣 这等于，100%阉割了，基于IP地理位置的分流（ 如 geoip:cn ）的分流 ❕❕❕ 喜提纯种大韭菜❕❕❕


 5. 优点 ✅ ：FakeIP 模式 延迟更低

    > 由于能秒返回 假IP，所以可以隐藏一些 握手延迟。得到性能上的及少许优化（对普通线路，几乎0优化，只有延迟极低的优质的线路才能看到区别）

<br>

总之，以上，别说四大缺陷了，上述 任何一个缺陷，都 = 0 接受度 🤣   。 

<br>

### 🆚 “Redir-Host + Nameserver-Policy DNS” 的优缺点

  1. 优点 ✅ ：消除 FakeIP 引发的一切 VPN特征
     
      Redir-Host 返回的是真实IP，不会触发APP内部 反VPN SDK的安全机制
  
  2. 优点 ✅ ：消除 FakeIP 引发的一切 兼容性问题
     
      Redir-Host 兼容性 100% ，尤其对于UDP P2P等游戏场景、其他低延迟UDP场景。在FakeIP下必须逐一手工维护排除列表。而在Redir-Host模式下，0维护 = 100% 省心 ！

  3. 优点✅ ： 0 DNS泄漏 + 0 全球绕路
     
      在新一代的技术方案中，Clahs Meta内核，通过大力增强DNS分流策略（nameserver-policy）的分流能力，使其分流能力，能够1:1镜像 分流规则（Rule）中的几乎所有规则。（提示：不要镜像，Reject相关的规则和IP分流规则，只镜像 “可以到达VPN节点” 的 “域名分流规则” ），以便，达到如下效果：
     >    🌍 国外网站 的 DNS解析，之使用 🌍 境外VPN节点 转发（不发国内，也不发给 其他VPN节点）
     
     >   🇨🇳 国内网站 的 DNS解析，直连 🇨🇳 国内DNS解析
      
       从而 ，避免了 DNS 泄漏，同时，也不会出现 全齐绕路的情况（ 不会出现  🇺🇸美国VPN节点 访问 🇯🇵日本CDN服务器 的情况）

  4. 优点 ✅ ：满血版 DNS解析
      
       全程无需调用 no-resolve ，通过 geoip:cn , 将分流的精准度拉满。将漏网之鱼降到个位数以下（需配合nameserver-policy + 中国域名名单）

  5. 缺点 ⚠️ ：Redir-Host 握手延迟无法隐藏 （感官上 可忽略不计）
      
       需要等待 国外DNS返回真实IP后，才能进行后面的请求。无法隐藏握手延迟。

<br>

经过上述对比，可以看到，两种方案的差异。明显，新方案： “Redir-Host + Nameserver-Policy DNS”  更胜一筹。新方案之所以厉害，是因为其充分利用了远程规则集。而老方案  “FakeIP + Fallback DNS + no-resolve” ，对远程规则集的 利用效率 = 0% 。

可以说，像 geosite:cn 这样的 “基于地理位置的域名分流名单” 逐渐成熟，是 业界 从 “FakeIP + Fallback DNS + no-resolve” 技术方案， 过渡到 “Redir-Host + Nameserver-Policy DNS” 技术方案 的 必要条件之一。在新方案上， “域名名单” 的 精准度和命中率，是新方案能否发挥效能的基础条件。新方案通过 预设的基于地理位置的域名名单，做到精准分流，同时 防DNS污染 + 防DNS泄漏。而上一代 防DNS污染技术方案  “FakeIP + Fallback DNS + no-resolve” ，只能通过同时调用 国内和国外DNS ，并用海外DNS结果做修正即可。所以必定DNS泄漏，或者因无法使用GeoIP，导致分流不精准。从而造成了上述四大缺陷！

目前，老技术方案 “FakeIP + Fallback DNS + no-resolve” ，已经老旧过时了 ！其唯一的好处，可能就是对握手延迟有一点点帮助。当然，对于俄国、朝鲜、伊朗那些流氓国家的用户，老方案，即 “FakeIP + Fallback DNS + no-resolve” 方案，可能还有一些过渡性价值，毕竟 在那些流氓国家 ，其类似geosite:cn这样的项目，并不足够完善。还不能完全达到  “Redir-Host + Nameserver-Policy DNS” 技术方案 对 所在国 的 域名合集中 “精准度”的要求。（实际上 很多人并不知道， 在流氓国家中，🇷🇺俄罗斯 、🇮🇷伊朗 是有自己geosite社区 和 对应魔改版的，而剩余其他国家 则几乎没有形成社区）

如何写一个  “Redir-Host + Nameserver-Policy DNS”  最小实现？
  - [《 Redir-Host + Nameserver-Policy DNS 最小化实现 》](https://github.com/Accademia/Additional_Rule_For_Clash/tree/main/GeositeCN#-%E6%9C%80%E4%BD%B3%E4%BD%BF%E7%94%A8%E5%BB%BA%E8%AE%AE)

<br>

此处不得不吐槽一下。都到了2025年12月份，居然 全网 “讲如何翻墙” 的 youtuber 中 90% 的频道， 还在推荐  “ Fake IP + Fallback DNS + no-resolve ” 方案 ？还说 这是最完美的组合？我都笑傻了。 🤮🤮🤮 就这水平，趁早还是把频道关了吧  🤣🤣🤣  完全误人子弟。 正是因为，有这些 垃圾youtuber 以讹传讹，才会让 诸如 Stash 这样的作者，觉得 自己软件的 Fallback模式 神功护体 宇宙无敌 🤣🤣🤣 拒绝让 Stash 的 DNS策略分流（nameserver-policy） 拉平到与 Clahs Meta同样的水平，继续抱着 “ Fake IP + Fallback DNS + no-resolve ” 当传家之宝 。绝对是 100%不可接受！
 



<br>
<br>




----------



# 本模版的 下一步改进会是什么？

<br>

为了继续保持，本模版在 iOS、MacOS、Win、Android 之间的通用性。本模版会等待 Stash 更新，以便 支持 “Clash Meta内核” 已经支持 的如下特性：

 - ### 在 “DNS分流策略” 中，全面支持 “批量分流”

     - 即，nameserver-policy 可以使用 ：
      
        ``` yaml
        “RULE-SET:远程规则” :
            - 'DOH链接#代理集合'  
            - 'DOH链接#代理集合'  
        “Geosite:XXX“ :
            - 'DOH链接#代理集合'  
            - 'DOH链接#代理集合'  
        ```
 
<br>

 - ### 在代理声明中，全面支持 “dialer-proxy链式代理”
    
    - 最新的 Clash Meta内核，已经完全删除了 Relay 链式代理 。而 Stash 又只能支持Relay链式代理。这两者 100%互斥 ❌ 在 链式代理 功能上。
    
    - 这导致，目前本模版，在链式代理上，使用了非常、非常、非常垃圾的 🤮🤮🤮🤮 折中写法 🤮🤮🤮🤮 ，以便让两者都能“不报错”（在Stash上 只能做到不报错，不等于有完整功能。在Clash上 目前可以完整功能）。
    
    - 一旦Stash支持 “dialer-proxy链式代理” 、“inline/override” ，本模版会立马更新到“内聚性”更高的写法上。

<br>

 - ### 在代理集合中，全面支持 “PASS”
 
    - 通过此功能，可以临时 关闭指定规则。如：通过临时关闭放广告规则， 让代账户登录不被反广告规则干扰。目前 Stash上是没有这个功能的，但是Clash Meta 此功能工作完美。

<br>

上述改进之后，本模版将初步进入完美状态。

已向Stash多次反馈 🔥🔥🔥 开发者 压根 已读不回 🔥🔥🔥。有能联系上开发者的，希望能顺手反馈一下。大家一起向Stash开发者，饱和式反馈。以便能 “加速” 本模版 快速进入  “完美状态”。

<br>

PS：如果Stash已经兼容上述功能，而本模版尚未改进，希望也能在本项目中发 issue，以便我能知道。本人没有加加任何群聊，无精力实时关注动向。

<br>
<br>

----------


# 避坑 ： 软件端 （ Stash for iOS ）   

<br>

以下 五大功能，是本模版需要用到，Stash for iOS 不兼容的 （ 但 Clash Meta 完美兼容 ）。

目前，虽然**不影响 本模版 基础分流** 进行日常翻墙上网，但是会使得本模版，缺失很多核心功能。无法做到想做到完美。必须需要Stash开发者补齐这 5 个功能短板（至少要补齐 前4个功能！）


<br>

### 1. 💩💩💩💩💩 Stash **无法 “批量分流” DNS查询** 到 指定的DNS服务器
   
  Stash 无法按照（RULE-SET、Geosite）分流 🇨🇳 中国域名 的 DNS查询 ，到 🇨🇳 中国大陆的DNS服务器
    
由于 Stash并不支持在DNS的nameserver-policy: 中 做如下声明 

    ``` yaml
        “RULE-SET:远程规则” :
            - 'DOH链接#代理集合'  
            - 'DOH链接#代理集合'  
        “Geosite:XXX“ :
            - 'DOH链接#代理集合'  
            - 'DOH链接#代理集合'  
     ```
   
   所以导致了，不可接受的核心问题，在Stash上
        
   - 在Stash，由于无法实现 “DNS分流策略（nameserver-policy）” 和 “分流规则（rule）” ，两者之间 1:1 互为镜像。所以，使得Stash在禁用FakeIP功能后，100% 会发生 全球绕路的情况 ❌❌❌ ，即，100%会发生 “美国落地节点 去 访问日本CDN” 的情况 ❕ 我认为，这是基础功能中的基础功能。❌❌❌❌❌❌❌ 这种功能缺失，这是100%不可接受的。要知道，DNS策略分流，比普通的分流规则，重要十倍以上。因为当你去用哪个VPS对应的DNS解析的时候，IP所在国家就已经确定了，你后面再怎么写rule分流规则，都改变不了这个IP的地理位置。DNS的策略分流功能 弱于 Rule 分流规则功能，完全就是本末倒置❕❕❕❕❕❕ ❌❌❌❌❌❌❌ 并且。这还强行拉高了VPS节点的性能，必须买哪些跨国性能极好的VPS（如每年120美金的的搬瓦工PlanV2）才能避免瓶颈。

        - 在Stash，由于不支持规则集合批量分流，导致必须要手动展开geosite:cn,但是导致了，本模版多了7000多行。❌❌❌
        
        一旦Stash的nameserver-policy支持 “RULE-SET:远程规则#代理组” ，本套模版将立刻删除这些手动展开的规则。以确保 模版拥有最低的行数。
    
以上问题，我反馈了很多次给Stash开发组，🤣🤣🤣 压根没人理。 💥💥💥💥 100% 已读不回套餐吃满了算是。而Clash Verga rec客户端（Clash Meta核心），而Clash Meta 完美支持 ✅ ✅ ✅ ，不会有这个问题。
   
<br>

### 2. 💩💩💩💩💩 Stash 的 即不支持dialer-proxy链式代理， 也不支持 UDP代理链，更不支持QUIC代理链
<br>

 而诸如 苹果智能，等AI软件，有大量UDP流量必须调用支持链式代理，因为：

  - 这些AI工具，对IP的合规性要求极高，会间歇性封禁 机房IP！！必须使用home ip的节点，作为落地节点，才能稳定访问这些AI工具。但往往，真HomeIP的节点（双ISP节点）的洲际网速速度都不高，不适合跨境直连。所以，必须使用链式代理功能，通过中转节点去访问这些HomeIP的节点。

  - 而且，这些AI工具，还会大量使用UDP流量，所以导致了，支持UDP流量的链式代理，在此场景下是刚需。

  而目前Stash并不能支持 ❌❌❌dialer-proxy链式代理❌❌❌ 。而在 “ Vless + Reality + Vision + XUDP ” 的节点上，更不能支持UDP、QUIC的链式代理。上述问题，已经向开发者多次反馈后，开发者压根不回复 不响应 ❌（不知道怎么想的）。而Clash Meta 完美支持 ✅ ，不会有这个问题。

<br>

### 3. 💩💩💩💩💩 Stash 的 代理组 不支持 PASS 规则

<br>

这导致了无法通过 PASS 临时关闭规则。比如： 临时关闭 反广告规则以便反广告规则干扰正常登陆。Stash更新了一堆复杂的 、 大多数人都用不上的、高仿Surge的 功能，也不更新这个功能，实在无法理解。
    
 同样，上述问题，已经向开发者多次反馈后，开发者压根不回复 不响应 ❌ （不知道怎么想的）。而Clash Meta完美支持 ✅ ，不会有这个问题。


<br>

### 4. 💩💩💩💩💩 Stash ，**无法支持  “远程规则 内预设的 REJECT、REJECT-DROP、DIRECT”**

<br>

所有在远程规则集中，内置的 REJECT、REJECT-DROP ，都会被Stash忽略。这个看起来不大的问题。持续了得有 N年 了。
    
- 这会导致 “切换IP归属地” 的规则（ https://github.com/Accademia/Additional_Rule_For_Clash/tree/main/FakeLocation  ），出现隐私泄漏的情况。

同样，上述问题，已经向开发者多次反馈后，开发者压根不回复 不响应 ❌ （不知道怎么想的）。而Clash Meta完美支持 ✅ ，不会有这个问题。

   
<br>

### 5. 💩💩💩💩💩 Stash ，即**无法 “关闭DNS的IPv6解析”** ，**也无做到 “全透明转发IPv6流量”**。

<br>
    
这导致了（在关闭Stash的FakeIP功能后），如果在Stash中 “关闭” IPv6路由，那么如下软件，都会出现出现了连接不上的情况：【因为下述两个软件，只会使用从DNS解析到的IPv6疯狂发起链接（而不尝试IPv4），而IPv6路由又被关闭了。】
    
- 在 Grok APP中，使用文字提问
    
- 在 苹果智能设置页面 ，链接登录ChatGPT账号 
    
这还导致了（在关闭Stash的FakeIP功能后），如果在Stash中 “开启” IPv6路由，那么如下软件，都会出现出现了连接不上的情况：【因为Stash的“IPv6路由”支持功能并不完整，导致的此问题】
    
- 在 局域网中 ，无法观看 挂载到Apple Homekit摄像头的实时视频（苹果家庭APP）
   
上述两者，相互互斥 （ Stash功能缺失是导致其互斥的核心原因 ）。上述问题，已经向开发者多次反馈后，开发者压根不回复 不响应 ❌（不知道怎么想的）。而Clash Meta完美支持 ✅ ，不会有这个问题。
<br>

### 总之，面对以上功能缺失❌。如果有人能联系上Stash开发者，请一起转达❕  人多力量大❕ 以便于，让 Stash 在核心功能上，补齐与Clash meta 之间的短板。


<br>
<br>

------


# 避坑 ：设备端

<br>

请不要使用以下任何设备，进行翻墙。因为，主流的国产设备，都内置了 🦠🦠🦠🦠 **反诈插件** 🦠🦠🦠🦠，会直接导致你的翻墙节点，被实时监控 ：
  
  > 国产安卓
  
  > 鸿蒙系统
  
  > 运营商光猫（非桥接模式）
  
  > 国产路由器
  
  > 国产笔记本预装的windows电脑


<br>

 ### 关于 **国产路由器**、**国产光猫** ： 
    
- 要知道，从2024年开始，🇨🇳中国大陆 所有的营业厅送的光猫、路由器 （和零售的国产路由器），都内置 🚧 **反诈插件** 🚧 ，
    
    > 反诈插件，是默认激活的。只有在桥接模式下才会关闭反诈插件。
   
    > 反诈插件，会通过 “深度包检测” 技术，将你的上网行为，实时上报给GFW。
    
    > 反诈插件，还会定期扫描你的内网设备，并上报。
    
    > 只有在桥接模式下，才会关闭反诈插件。但在2025年开始，全国所有运营商，都不给用户开放设置桥接模式了。
    
    > 总之，你拿到的不是一台路由器、光猫，而是买了一台监控软件，放在家里。
        
- 建议，运营商的光猫关闭路由模式 改为桥接模式（闲鱼上有第三方 能提供 路由器改桥接功能）。自费购买 进口品牌 路由器，如 华硕路由器（进口品牌，目前没有内置反诈插件）。
        
<br>

### 关于 **国产手机** ：
    
- 2022年开始（安卓13），所有国产手机都内置了 🚧 **反诈插件** 🚧 。
    
    > 功能比路由器内置的反诈插件还要更强，可以直接扫描你手机内的所有APP和所有数据。翻墙软件，被归类为 **有害软件** 。理论上，你手机内所有的数据，都可以上报给GFW。隐私性 = 0.
        
- 测试你手机有没有 反诈插件 的方法：
    
    > 关闭所有网络连接后，能不能修改手机名 ？ 比如把手机名改成 “8口交换机” 或 其他名字。如果 断网后， 不让你改名。恭喜你，你手机100%内置反诈插件。建议只能换三星苹果等进口品牌的手机。
        
- 总之，不要购买 ❌ 国产手机。
    
    > 如果你真想支持国产厂商，可以买国产手机的海外版，比如出厂默认搭载 Google Play 应用商店的的海外版小米手机或一加手机，那些都是没有内置反诈插件的。相对比较安全。
    
    > 而且国产手机（包括三星手机），在反取证方面，几乎是0。一旦你手机，落入警方之手，可以被警方任意解锁，任意窥视！
    
    > 唯一完美的解决方案 =  只有 iPhone （ 无法被警方强行解锁，也没有反诈插件 ）
    


<br>
<br>

------



#  避坑 ： 节点端 （ VPS商家的套路 ）

<br>

1. ### 优先选择 ：**“ 外国人运营 + 大厂 ”** 的VPS，做中转节点 ：
    
    > 如：VPS hosting（ 此为 搬瓦工的上游 ）
    
    > 如：搬瓦工 
   
   等等，这些大厂中使用CN2、9929、10099线路的节点。

<br>

2. ### 尽量不买 ：**“ 🇨🇳 中国人 ”** 运营的VPS 。坑非常多，例举几点：
    
    - 国产厂商，**雷军附体** ❕
        
         号称9929线路。还会大字表明 “无限流量”。但小字标明 “峰值50Mb带宽”……，稍微不注意，就被坑了。对比 VPS hosting 这些国外大厂，都是 2.5G - 10G带宽， 瞬时峰值可以拉的非常高。像搬瓦工120美金每年的日本线路，晚高峰带宽可以长时间稳定在40-50MByte/s。而国产厂商，无限流量 但 “峰值50Mb带宽”的线路，往往带宽只能稳定在3～4MByte/s（晚高峰会更慢）。
    
    - 国产厂商，**各种虚标** ❕
        
         包括线路稳定性（可连通性），也跟老外的厂商无法对比，比如像 **MoeCloud**（ https://lite.moe/ ），号称自己英国线路强无敌。但实测经常会间歇性断联。频繁的时候，一周断好两三次，一次好几个小时。
    
    - 国产厂商，**吃相难看 + 套路满满** ❕
        
         比如，有些国产厂商，会针对测速软件进行优化。妥妥的中国人的小聪明尽显无疑。比如 像 **saltyfish** （ https://portal.saltyfish.io/ ）这样的华人厂商 ，会在你测速的时候拉满带宽，但是当你下载大文件时间超过1分钟以后，瞬间把你带宽降低非常低。使用脚本进行测速的时候根本看不出来。关键也不会在购买页面说明，先骗你上车，然后换脸。全是套路。
    
    - 国产厂商，**没有契约精神** ❕
        
         在很多电报群中，还有翻友袒露，像 **saltyfish** （ https://portal.saltyfish.io/ ），还会应为你提问态度不好或在工单中辱骂客服，直接封你号，哪怕你的VPS没到期，封号后也不退款。 一副 **“钱我已经骗到手，你能拿我怎么样”** 的骗子嘴脸 🤣 。毫无契约精神。要知道，这种国产厂商 封号删机器，并不是因为你的VPS 滥发垃圾邮件 参与DDOS 等违规使用，而是只是因为客服不高兴，因为你让我不爽了。一副 **“我就是 人肉GFW、鸿蒙转世灵童 的嘴脸”** 🤣🤣，相信这不是saltyfish一家有的问题。其他 一人公司的🇨🇳厂商，不胜枚举。
    
    - 国产厂商， **连哄带蒙**❕
        
         就像鸿蒙后门一样。你也永远没法知道，对方是否跟🇨🇳政府有合作。或者是因为他是一人公司的技术能力太差，被GFW的人已经挂了木马，
    
    - 总之，别买国产❕
        
         最好的避坑方法，就是不买中国人厂商的VPS，只卖老外的。当然，也不绝对，不是所有海外华人都是坏人。还是有一些华人厂商 拥有高性价比稳定服务的。比如 香港节点 就是特例。如 apernet对比搬瓦工同质量的线路，搬瓦工可能会贵几倍。

<br>

3. ### 中转节点 更多的坑
   
    除了要带宽好，还要，尽量能选  ”可付费购买多IP“ 的VPS。以防止被GFW封禁后，能够有 ”备用IP“  做应急处理。 当然，如果VPS厂商支持 “免费换IP“，那就更好了。但往往这样的厂商，IP质量比较差（比如 搬瓦工 通过机房迁移，可以实现免费换IP，但的确IP质量比较差，稍微严格点的网站，可能都会被弹窗）

<br>

4. ### 落地节点 更多的坑
   
    要测试IP的干净程度，最好是双ISP 家庭宽带IP、住宅IP 或者 手机网络IP。但还要检测其国际出口 或落地国的出口是否足够大。大部分这种IP的节点，出口都很小，50M或者200M顶天了。而且。如果真的是 “美国的车库级机房” 你还可能会遭遇 频繁断流。坑比较多。

<br>

5. ### 最后，一分钱一分货
  
     哪怕是像搬瓦工这样的外国人运营的大厂，也会有坑。比如同样参数的日本线路。年费120美金2TB月度流量的版本 和 年费35美金 250GB月度流量的版本。后者 “在中国某些地区” 带宽峰值，只有前者1/5（在晚高峰时）。虽然，购买页面的参数描述，两者是一样的。😂 只能说，一分钱一分货。想用得好，的确要花成本。

<br>
<br>

------

#  避坑 ： 其他日常问题

<br>

### 1. **不要将自己的节点借给别人**。 
  
要知道, ”跨异地城市“的多设备 连接境外 “同一个VPS”，会被GFW重点监控。最好只在自己同城家庭内部  分享节点。

   - 节点不外借，就像车不外借一样。你放心，你借出去的节点，被用坏了，要修要处理的人、被麻烦的人，只会是你自己。对方绝对不会给你出一分钱、一份力，而且大概率还会心里埋怨你，为什么你的节点不好用。你是不是故意给弄坏不让人家用的。 🤣🤣🤣🤣 如果人家用你的节点，导致人家外国银行账号被封控，或者密码被窃取。那你就等着领骂吧。你们要闹掰了，人家把你给的VPN，举报到🚨，您100%被训诫，没准还喜提 “治安处罚“， 再帮👮完成 ”500软妹币的KPI”。虽然不入刑，但 以后无行政处罚记录证明 ，100% 不是白纸。而且 您此后就被辖区挂上号 ， 喜提 活佛 大好人 ❕❕
    
   - 尤其这种电脑小白，其大概率会用windows。在Win上有相当多的盗版软件，其内置电脑病毒，会后台默默发垃圾邮件。一旦接入节点。会立马被VPS厂商关闭你的机器，甚至封停账号。这也就是为什么像联想、华为这样的大厂，一般不给员工笔记本电脑Admin账号的密码，就是不让员工装盗版。不然 用公司官方的IP发垃圾邮件？或者通知Adobe 微软 被盗版了？谁也受不了。
   
<br>

### 2. 设置影子端口
 
 **单一节点**，除了准备**多个IP**，最好也能通过gost**多设置几个影子端口**（端口转发）。因为现在GFW封禁都是精准封禁，即便被封，往往都是先从封禁端口开始，这会备用端口就能派上用场了。以防止境外节点失联后，无节点可应急的情况。


 
<br>
<br>

------

# 答疑 

<br>

### 我看不懂上文中的 xxx 怎么办？

 > 把文章拷贝给AI（ChatGPT Pro 、Gemini Pro 、Grok Think ） ， 让AI来解答 🔥
 >
 > 注意，一定要使用 海外AI + 付费AI！千万别用 🇨🇳国产AI， 更 别用海外免费AI ❕ 别用免费AI ❕ 别用免费AI ❕

再次重申，我不回答任何一般性问题。只响应 ：BUG 、 修正 和 功能完善 ，这三处。

本项目也没有任何群、电报号 ，打着本项目名义 推销节点 的 🤣 都与本项目无关。


<br>
<br>

------


# geosite 规则统计表

<br>

以下表格列出了，当前 Clash 分流模版中，用到的每个 geosite 标签及其对应的规则数量（包括文件中引用的子规则），表格顺序与配置中出现的顺序一致。最后一行给出所有规则的总数。

更新 ： 2025-10-22
来源 ： https://github.com/v2fly/domain-list-community/tree/master/data

| 分类 (geosite) | 规则数量 | 归类 |
|---|---|---|
| category-httpdns-cn | 96 | [1st-01] - 反DNS跟踪 |
| private | 243 | [1st-02] -  局域网 |
| category-ads | 1517 | [1st-09] -  屏蔽广告 & 隐私保护 |
| ookla-speedtest | 13 | [2st-00] -  测速 |
| synology | 20 | [2st-01] -  智能设备 |
| onedrive | 11 | [2st-02] -  公有云： 云盘 、云存储 |
| dropbox | 16 | [2st-02] -  公有云： 云盘 、云存储 |
| mega | 3 | [2st-02] -  公有云： 云盘 、云存储 |
| imgur | 3 | [2st-02] -  公有云： 云盘 、云存储 |
| category-pt | 196 | [2st-04] -  P2P(海外) |
| paypal | 489 | [2st-11] -  金融 |
| wise | 2 | [2st-11] -  金融 |
| binance | 36 | [2st-11] -  金融 |
| okx | 6 | [2st-11] -  金融 |
| ebay | 725 | [2st-20] -  购物 |
| patreon | 4 | [2st-20] -  购物 |
| xbox | 79 | [2st-21] -  游戏 |
| playstation | 4 | [2st-21] -  游戏 |
| nintendo | 248 | [2st-21] -  游戏 |
| steam | 88 | [2st-21] -  游戏 |
| epicgames | 31 | [2st-21] -  游戏 |
| gog | 13 | [2st-21] -  游戏 |
| rockstar | 5 | [2st-21] -  游戏 |
| ea | 324 | [2st-21] -  游戏 |
| origin | 9 | [2st-21] -  游戏 |
| ubisoft | 8 | [2st-21] -  游戏 |
| youtube | 351 | [2st-22] -  视频 |
| netflix | 28 | [2st-22] -  视频 |
| disney | 317 | [2st-22] -  视频 |
| primevideo | 23 | [2st-22] -  视频 |
| hbo | 25 | [2st-22] -  视频 |
| fox | 488 | [2st-22] -  视频 |
| apple-tvplus | 8 | [2st-22] -  视频 |
| category-porn | 12915 | [2st-22] -  视频 |
| tiktok | 21 | [2st-23] -  短视频 |
| instagram | 148 | [2st-23] -  短视频 |
| snap | 7 | [2st-23] -  短视频 |
| twitch | 32 | [2st-24] -  直播 |
| spotify | 23 | [2st-25] -  音频 |
| twitter | 24 | [2st-26] -  社交 |
| telegram | 19 | [2st-26] -  社交 |
| whatsapp | 13 | [2st-26] -  社交 |
| line | 20 | [2st-26] -  社交 |
| reddit | 12 | [2st-26] -  社交 |
| discord | 28 | [2st-26] -  社交 |
| linkedin | 12 | [2st-26] -  社交 |
| clubhouse | 3 | [2st-26] -  社交 |
| signal | 8 | [2st-26] -  社交 |
| tumblr | 1 | [2st-26] -  社交 |
| pixiv | 11 | [2st-26] -  社交 |
| apple-intelligence | 5 | [2st-29] -  AI |
| openai | 18 | [2st-29] -  AI |
| xai | 2 | [2st-29] -  AI |
| anthropic | 6 | [2st-29] -  AI |
| google-gemini | 23 | [2st-29] -  AI |
| category-ai-!cn | 109 | [2st-29] -  AI |
| adobe | 390 | [2st-30] -  工具 |
| github | 32 | [2st-30] -  工具 |
| bing | 38 | [2st-30] -  工具 |
| notion | 8 | [2st-30] -  工具 |
| pinterest | 104 | [2st-30] -  工具 |
| **总计** | **19461** |  |



<br>
<br>

------


# 许可与声明

<br>

- 本代码使用MIT协议分发

- 参与编写：OpenAI Chatgpt 5-pro Agent

<br>
<br>

------



# 效果

<img width="477" alt="最终效果" src="https://github.com/user-attachments/assets/eb5704bc-450a-400f-b6f8-2e1ee0f3f40c" />


