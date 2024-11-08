**目录**

* [前言](#_label0)
* [(一) WiFi 漫游](#_label1)
	+ [(1\) 无漫游场景](#_label1_0)
	+ [(2\) 有漫游场景](#_label1_1)
	+ [(3\) 协议支持](#_label1_2)
* [(二) 普通家庭 WiFi 组网](#_label2)
	+ [(1\) 常规 WiFi 使用](#_label2_0)
	+ [(2\) 有线路由](#_label2_1)
	+ [(3\) 有线中继](#_label2_2)
	+ [(4\) WiFi 串并联](#_label2_3)
	+ [(5\) 无线桥接](#_label2_4)
	+ [(6\) WiFi 信号放大器](#_label2_5)
* [(三) 胖瘦 AP](#_label3)
	+ [(1\) 胖 AP](#_label3_0)
	+ [(2\) 瘦 AP](#_label3_1)
* [(四) 大范围 WiFi 网络组网](#_label4)
	+ [(1\) mesh 组网](#_label4_0)
	+ [(2\) AC \+ AP 模式](#_label4_1)
* [结尾](#_label5)
 



---


**liwen01 2024\.10\.27**


[回到顶部](#_labelTop)## 前言


无线 WiFi 的优点是方便、灵活，可以接入各种设备。缺点就是信号容易被干扰、信号覆盖范围有限。下面几个问题应该很多人都有遇到过：


1. **为何很多洗手间的 WiFi 信号都不太好？**
2. **市面上的穿墙路由器真的就比其它路由器效果好么？**
3. **为何有时候 WiFi 信号强度很好，但网速却很慢？**
4. **如果房间比较大，需要怎样才能实现 WiFi 全屋覆盖？**
5. **如果是独栋多层的楼房，又要如何组建 WiFi 网络？**
6. **商场、公司、学校等人员密集场所，它们的 WiFi 又是如何组建？**
7. **什么是 WiFi 漫游、它有什么好处、又要如何实现 WiFi 漫游功能？**
8. **什么是胖 AP，什么是廋 AP？AC\+AP 又是什么？**


因为企业 WiFi 组网比较复杂，这里主要介绍家庭无线 WiFi 组网方案，主要包括：**路由器的串并联、WiFi 信号放大器、mesh 组网、AC\+AP 模式组网**。它们各有优缺点又各有适合的应用场景。


[回到顶部](#_labelTop):[悠兔机场](https://xinnongbo.com)## (一) WiFi 漫游


WiFi漫游 (WiFi Roaming) 指的是当一个移动设备 (如智能手机、平板、本电脑等) 在一个由多个无线接入点 (AP) 覆盖的网络中移动时，设备能够无缝切换到信号更强或更合适的接入点，而不中断网络连接或影响应用程序的运行。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214506408-12876665.png)
比如在大的商场、写字楼、图书馆等环境，我们拿着手机，从 AP1 所在区域，移动到 AP2、再到 PA3 这个区域。


### (1\) 无漫游场景


在没有漫游功能的时候，当跨区域时，只有等一个 AP 区域的信号弱到断开连接之后，才会主动去连接另外一个区域的 AP，用户可以明显地感觉到手机网络变慢变卡，最后断网，且要等上几秒之后才能恢复。


### (2\) 有漫游场景


在 AP1 \~ AP3 是支持漫游功能时，当要跨区域的时候，手机能够根据 AP 之间的信号强度、信噪比、AP 负载、移动数据和位置变化去自动切换所需要连接的 AP，效果就是用户一般感觉不到明显的网络卡顿，APP 的数据也不会中断。


### (3\) 协议支持


要实现 WiFi 漫游功能，需要 AP 和用户设备同时都支持 802\.11k/v/r 协议


* **802\.11k**：无线资源测量协议，可帮助终端快速搜索附近可作为漫游目标的 AP。
* **802\.11v**：无线网络管理协议，用来解决AP之间的负荷均衡，以及终端节电等功能。
* **802\.11r**：快速漫游协议，用于加速手机或者电脑在漫游时的认证流程。


要实现 WiFi 的漫游，还需要组建合适的网络。


[回到顶部](#_labelTop)## (二) 普通家庭 WiFi 组网


### (1\) 常规 WiFi 使用


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214518792-1696671607.png)
现在大部分家庭使用 WiFi 的模式是外面通过光纤接入到屋内，先接入光猫，这一部分主要是由运营商提供，比如国内的联通、电信、移动。


有些光猫也兼备路由器的功能，但是它的接口和接入的设备有限，整体性能也比较弱，而且很多家庭的光猫是放置在弱电箱里，所以整体信号不太好。


目前大部分人都是从光猫接根网线，接到一个路由器上，日常使用 WiFi 都是通过这个路由器来实现。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214530448-1488636000.png)
上图这种房间布局是比较常见的，一般将路由器放置在客厅电视柜上，为所有房间提供无线 WiFi 网络。


当把路由器放在客厅电视柜上的时候，客厅、餐厅、厨房可以享受到最佳的WiFi信号，远离客厅的书房、主卧、主卧洗手间因为中间隔了墙壁，WiFi 信号会被衰减，所以整体信号会比较弱。


为了使主卧和书房都有比较好的 WiFi 使用体验，如果去市面上购买一个穿墙路由器，能否解问题呢？


使用穿墙路由器实际效果正常不会很理想，市面上的穿墙路由器只不过是一个噱头。因为在中国《微功率短距离无线电发射设备目录和技术要求》有规定


* **2\.4GHz频段(2400–2483\.5 MHz)**：最大发射功率限制为 100 mW(20 dBm)，等效全向辐射功率(EIRP)为 20 dBm。
* **5GHz频段(5150–5350 MHz)**：室内使用最大发射功率限制为 200 mW(23 dBm)。
* **5GHz频段(5725–5850 MHz)**：最大发射功率限制为 25 mW(14 dBm)。


在其它国家和地区也有相应的限制，最大发射功率被限制，不管路由器有几根天线，它的穿墙能力都不可能有显著提升，除非它违反规定增强了发射功率。


具体原因可以查看之前的文章《[wifi基础(一)：无线电波与WIFI信号干扰、衰减](https://github.com)》


### (2\) 有线路由


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214544264-819826816.png)
对于上面这种户型，如果要使书房、主卧、主卧洗手间都有良好的 WiFi 信号，可以使用路由器串并联的方式来解决这个问题。


路由器串并联可以是通过有线的方式来串并联，也可以通过无线的方式来实现。


有线的方式信号会稳定很多，但是需要布置网线，如果房间之前有布网线推荐使用有线路由的方式。


有线路由的方式对路由器没有特殊的要求，任意两个路由器都可以实现。如果家里有多个路由器，可以将性能较好的作为主路由器，性能交差点的最为副路由器。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214555064-975963993.png)
* 将光猫出来的网线接到路由器1的WAN口，常规方式设置路由器上网。
* 将路由器1任意一个LAN口，接到路由器2的WAN口，也是常规方式设置路由器上网。


这样就实现了两个路由器的串联，它们各自独立分配 IP，一般它们处于不同网段。


这种方式，就算路由器1与路由器2设置相同的 WiFi 名字和密码，它们也不能实现漫游功能。


### (3\) 有线中继


两个路由器串并联，通过不同的接线，可以实现不同的模式。如果主路由器1 LAN 口接到副路由器2的 LAN 口，这种模式需要做一些特殊的设置。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214605507-140558407.png)
* 将主路由器1 LAN 口接到副路由器2的 LAN 口
* 将副路由器2 的 DHCP 功能关闭
* 到路由器2 的 LAN 口设置处设置 LAN 口 IP，该 IP 与路由器1同一个网段，且不与路由器1的其它设备相冲突
* 路由器2无线设置按正常设置就可以


这种模式，路由器1与路由器2的设备是处于同一网段，因为两个路由器的IP分配工作都是由路由器1来实现。同样的，它们也不支持漫游功能。


### (4\) WiFi 串并联


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214617288-182849725.png)
如果家里有多个闲置的路由器，选一个性能好的做主路由器，可以同时串并联多个路由器来解决 WiFi 信号不好的问题。


这种方式的限制就是需要布网线，优点就是对路由器的要求低，且可以各种不同品牌的路由器同时使用，可以将家里闲置的路由器很好地利用上。


### (5\) 无线桥接


WDS(Wireless Distribution System，无线分布式系统)是一种允许多个无线接入点(AP，Access Point)通过无线方式相互连接的技术，目的是扩展无线网络的覆盖范围。通过 WDS，多个路由器或 AP 可以彼此无线桥接，而不需要通过网线连接。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214626952-48590359.png)
这种方式是在路由器2中去设置 WDS 功能，根据设置引导去连接路由器1。


这种方式的好处就是可以不用布线，缺点就是信号容易被干扰，效果没有有线路由的好。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214636642-1250174790.png)
对于最开始的房屋布局，我们应该要将路由器2放置到洗手间外面才能实现最佳的效果。因为路由器2 所有对外的所有数据都要通过路由器1传输出去。但因为它们是通过无线连接的，所以路由器2与路由器1间的信号不能太差。


如果将路由器放置到书房或是主卧里面，就会出现路由器 WiFi 信号强度很好，但是网络数据很慢的情况，主要原因是路由器2与路由器1间信号不好通信丢包严重导致速率严重下降。


### (6\) WiFi 信号放大器


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214646305-1883568675.png)
WiFi 信号放大器，也叫 WiFi 扩展器或 WiFi 中继器，是一种通过接收现有 WiFi 信号并将其重新广播来扩展 WiFi 覆盖范围的设备。它能够解决家中或办公区域中 WiFi 信号弱、死角等问题，确保无线网络覆盖更广的区域。


它的工作原理是：


* **信号接收**：放大器通过内置的无线网卡，接收来自主路由器的 WiFi 信号。
* **信号放大**：放大器将接收到的 WiF i信号进行放大或重复(中继)，以增强信号的强度和覆盖范围。
* **信号转发**：放大后的信号再次通过放大器的无线电广播出去，覆盖到原本信号无法到达的区域。


整体而言，使用 WiFi 信号放大器的效果并没有使用多个路由器中继的效果好，但一般 WiFi 信号放大器相比于路由器体积会小些，而且价格要便宜。


[回到顶部](#_labelTop)## (三) 胖瘦 AP


### (1\) 胖 AP


上面我们介绍的，也是我们日常比较常使用的路由器，它都是属于胖 AP(Fat AP)。


胖 AP 它是一种独立工作的无线接入点，它具备较为完整的网络管理和控制功能。它可以自行进行认证、加密、管理无线信道和带宽分配，并执行许多其它功能，因此它可以在不依赖外部设备的情况下独立提供无线网络服务。


它的优点是：**独立性强，适用与小型网络**。


它的缺点是：**配置相对复杂**。对于复杂场景，比如大型写字楼，需要在不同位置放置很多个 AP，网络管理员不太可能每个 AP 去独立配置管理，所以就出现了瘦 AP(Thin AP)。


### (2\) 瘦 AP


瘦 AP 是一种功能简化的无线接入点，主要依赖于一个集中管理的设备——通常是无线局域网控制器(WLC)。瘦 AP 本身只负责基本的无线信号转发功能，而所有的复杂管理和控制功能(如认证、加密、频谱管理等)都交由 WLC 来处理。


**瘦AP的特点是：**


* **集中管理**：通过无线控制器统一管理多个瘦 AP，使得大规模部署更加容易，并且可以进行集中配置和故障排查。
* **简化设备**：瘦 AP 硬件相对简单，因为不需要集成完整的管理功能，从而降低了每个 AP 的成本。
* **适用场景**：瘦 AP 通常应用于大型企业、校园或高密度无线网络环境中，在这些场景下，多个 AP 的管理通过控制器集中进行，便于维护和扩展


[回到顶部](#_labelTop)## (四) 大范围 WiFi 网络组网


如果对上网体验要求高，且要实现 WiFi 漫游功能，可以使用 mesh 组网方式或是 AC\+AP 模式。


WiFi 漫游功能，可以让你在房间、楼层间移动的时候实现 WiFi 自动切换，用户基本上无法感知到网络的切换，网络也不会中断。对于家庭使用，mesh组网是个不错的选择。


### (1\) mesh 组网


WiFi 的 mesh 组网通过多个无线节点(通常是 mesh 路由器或 AP )相互连接，形成一个自我修复的网状网络，使得每个节点都能与其他节点通信并动态调整网络路径，以优化信号覆盖和流量传输。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214656565-1822092029.png)
**(a) WiFi mesh 组网的核心概念**


**多跳传输**：在 mesh 网络中，数据可以通过多个节点传递到目标设备。这种方式有效地扩展了 WiFi 信号的覆盖范围。即使某个节点离主路由器较远，仍可以通过其他中继节点进行数据传输。


**自我修复(Self\-Healing)**：如果某个节点失效或断开连接，mesh 网络会自动寻找新的路径，使网络保持正常运行。这种冗余性使得网络更加稳定和可靠。


**节点协作**：所有的 mesh 节点(mesh AP 或路由器)相互通信，并能够动态调整信号传输的路径和信号强度，以确保网络性能最佳化。这种协作机制可以减少网络拥堵并优化流量。


**无缝漫游**：由于 mesh 网络中的节点都属于同一个网络，用户设备可以在各个节点之间无缝漫游，而不会中断网络连接。这对于覆盖大范围的家庭、办公楼、酒店等场景尤为重要。


**(b) WiFi mesh 组网的结构**


**主节点(Primary Node/Gateway Node)**：这是连接互联网的主路由器或接入点，通常位于用户的互联网入口处。所有的网络流量最终都会经过主节点进行互联网通信。


**从节点(Secondary Nodes/Child Nodes)**：这些节点与主节点或其他从节点连接，用于扩展网络覆盖。每个从节点都能与多个其他节点通信，并动态调整网络路径以优化连接。


**设备通信**：设备(如手机、电脑等)可以与任意一个距离较近的节点连接，而不必强制连接到主节点，从而保证稳定和快速的连接。


**(c) mesh 组网的优势**


**广覆盖**：通过多个节点扩展网络，消除信号盲区。


**无缝漫游**：设备可在各节点间自由切换，无断线。


**自我修复**：节点失效时，网络会自动调整路径，保证稳定性。


**易扩展**：添加新节点简单，适合大范围网络覆盖。


**稳定性能**：动态调整信道和路径，优化网络流量。


**(d) mesh 组网的缺点**


**成本较高**：设备价格昂贵，尤其是需要多个节点时。


**带宽下降**：多跳传输会导致带宽逐步降低。


**延迟增加**：多节点传输会增加网络延迟。


**配置复杂**：需要精心规划节点布局，且企业级网络配置复杂。


**兼容性问题**：不同品牌的 mesh 系统可能不兼容。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214707884-2031931135.png)
mesh 可以是有线组网也可以是无线组网，有线模式需要拉网布线，无线模式整体性能较差。


mesh 组网需要给路由器独立供电并放置在一个遮挡较少的位置，多少也有些影响美观。但是如果换成 AC\+AP 的模式就不存在这个问题了。


另外需要特别注意的是，**各品牌商的路由器之间 mesh 组网可能会存在不兼容的情况，所以最好是使用同一个品牌的 mesh 路由器来组网**。


### (2\) AC \+ AP 模式


在 WiFi 组网中，AC(Access Controller)\+AP(Access Point)主要用于大型或企业级的无线网络环境。这种模式通常由一个或多个AP和一个AC组成，目的是集中管理和优化无线网络。


**(a) AC(Access Controller)**AC 是无线网络的集中控制器，负责管理和配置所有接入点(AP)。它协调AP之间的工作，进行负载均衡、无线信道管理、认证、接入控制等。


可以简单理解为：这里的 AC 就是上面介绍的路由器，AP 就是路由器的天线，AP 负责无线信号的收发，AC 负责无线的管理。变相的把 WiFi 天线布置到房间的各个位置上。


**(b) AC 主要功能有**：


**集中管理**：通过AC，可以在一个地方配置和管理所有的 AP，简化网络管理。


**负载均衡**：AC 可以监控 AP 的负载情况，并在用户移动时将其重新分配到负载较低的 AP。


**无线信道管理**：AC 优化无线信道的使用，减少干扰，提高网络效率。


**安全管理**：进行集中化的认证和加密管理，提高网络安全性。


**(c) AP (Access Point)**


AP 是无线网络的接入点，负责将无线信号转换为有线信号，反之亦然，允许无线设备连接到网络。


**(d) AP 主要功能有**：


**无线覆盖**：AP 提供无线信号覆盖，支持无线设备的接入。


**数据传输**：AP 将无线设备的数据传输到有线网络，或者将有线网络的数据传输到无线设备。


**信号强度调节**：AP 可以调整其发射功率，优化无线覆盖范围。


**(e) AC\+AP模式的优势**


**高效管理**：通过集中控制和管理，简化了无线网络的维护和配置工作。


**灵活性**：可以根据实际需要扩展 AP 的数量，增加无线覆盖范围。


**优化性能**：通过 AC 的干预和管理，提升了网络的性能和稳定性。


**增强安全**：集中化的安全策略和认证机制提升了整体网络的安全性。


![](https://img2024.cnblogs.com/blog/555985/202410/555985-20241027214717660-911394818.png)
AP 有面板式和吸顶式两类，家用一般是使用面板式，可以直接嵌入墙体，跟插座一样。吸顶式的多用在写字楼等场所，直接放置在天花板处，整体比较美观。


另外，这类 AP 一般都支持 POE 供电，也就是可以直接使用网线进行供电，少了另外拉电的麻烦。


整体而言，AP 的性能会比 mesh 组网稍微差一点点，如果是家庭或是小范围使用，推荐使用 mesh 组网，mesh 相对 AC\+AP来说价格也便宜点。


如果是写字楼，学校等需要大面积覆盖的场景，还是推荐使用AC\+AP的模式，方便控制和管理。


[回到顶部](#_labelTop)## 结尾


上面内容简单地介绍了下目前家庭比较常用的 WiFi 组网方案，这些方案具体的使用配置，可以参考具体品牌商设备上的介绍。下一篇将介绍 WiFi 认证与加密相关基础知识。


上面内容，如有错误，欢迎评论区提示指出，不胜感激。


 


\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-End\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-如需获取更多内容请关注 **liwen01**公众号
