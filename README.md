# FTChinese Reprint API Guideline
For now, there are only two APIs for your to access FTChinese content for reprint. 
## Latest Headlines
It shows the latest headlines that can be syndicated for reprint. An Example here: 

```
{
    "meta": {
      "title": "Reprint API",
      "description": "Reprint API",
      "adid": "",
      "theme": "default"
    },
    "sections": [
      {
        "type": "block",
        "title": "Latest News",
        "name": "",
        "side": "none",
        "sideAlign": "right",
        "lists": [
          {
            "name": "New List",
            "type": "",
            "title": "中国经济",
            "url": "",
            "language": "",
            "description": "",
            "style": "",
            "float": "none",
            "showTag": "no",
            "showTimeStamp": "no",
            "preferLead": "longlead",
            "sponsorAdId": "",
            "sponsorLogoUrl": "",
            "sponsorLink": "",
            "sponsorNote": "",
            "feedItems": "5",
            "feedTag": "中国经济",
            "feedType": "story",
            "items": [
              {
                "headline": "城镇化的方向和挑战",
                "eheadline": "",
                "image": "http://creatives.ftacademy.cn/picture/9/000121769_piclink.jpg",
                "longlead": "王丹：中国新型城镇化目的不是为了土地私有化或者彻底消除城乡差异，而是要方便土地、人口和资本在城乡间的自由流动，发挥两个市场的优势。",
                "tag": "中国经济,城市化",
                "area": "china",
                "industry": "",
                "author": "王丹",
                "timeStamp": "1628524800",
                "type": "story",
                "id": "001093503"
              },
              {
                "headline": "中国新一波疫情加剧经济放缓担忧",
                "eheadline": "China Covid outbreak linked to Delta variant weighs on economy",
                "image": "http://creatives.ftacademy.cn/picture/5/000122585_piclink.jpeg",
                "longlead": "中国周一报告新增94例新冠本土确诊病例。传染性极强的Delta变种引发严厉抗疫措施，而数据显示中国经济复苏开始受到压力。",
                "tag": "中国经济,新型冠状病毒",
                "area": "china,asiapacific",
                "industry": "",
                "author": "韩乐,白艾德,马思潭",
                "timeStamp": "1628524800",
                "type": "story",
                "id": "001093501"
              },
              {
                "headline": "非洲国家接受中国贷款的风险",
                "eheadline": "The risks of China’s African lending",
                "image": "http://creatives.ftacademy.cn/picture/3/000122583_piclink.jpeg",
                "longlead": "中国发放的双边贷款虽然有益，但贷款条款不透明可能让债务国在寻求其他债权人贷款时陷入困境。",
                "tag": "新兴市场,中非关系,世界银行,国际货币基金组织,中国经济",
                "area": "china,usa,asiapacific,africa",
                "industry": "finance",
                "author": "克莱尔•琼斯",
                "customLink": "",
                "timeStamp": "1628524800",
                "type": "story",
                "id": "001093499"
              },
              {
                "headline": "从跨周期角度理解当下政策语境",
                "eheadline": "",
                "image": "http://creatives.ftacademy.cn/picture/5/000120685_piclink.jpg",
                "longlead": "蔡浩、李海静：7月中央政治局会议再提“跨周期调节”，引发市场广泛关注。什么是“跨周期调节”？在当下宏观经济背景下又有什么政策内涵？",
                "tag": "中国经济,货币政策,跨周期调节,房地产",
                "area": "china",
                "industry": "",
                "author": "蔡浩，李海静",
                "timeStamp": "1628179200",
                "type": "story",
                "id": "001093471"
            },
            {
              "headline": "如何防止碳减排中的“搭便车”？",
              "eheadline": "",
              "image": "http://creatives.ftacademy.cn/picture/0/000121420_piclink.jpg",
              "longlead": "吴金铎：“碳中和”、“气候中性”等承诺，大多数是软约束。如何建立硬约束？碳边境治理机制将改变国际贸易体系，加大发展中国家转型成本。",
              "tag": "碳减排,碳交易,碳中和,中国经济",
              "area": "china",
              "industry": "",
              "author": "吴金铎",
              "timeStamp": "1628179200",
              "type": "story",
              "id": "001093443"
            }
          ]
        }
      ]
    }
  ]
}
```

#### What are the fields for? 
For your reprint business, you only need to look at the **items** array. Please note that all the fileds might be empty, null or undefined. It's important to **always verify all the fields** for availability and correct format when programming, to avoid fatal errors. And here are the fields that matter: 
* **headline**
The headline of the article in string format. 
* **eheadline**
The English headline of the article in string format. Depending on your syndication contract, the English headline might be empty.  
* **image**
The image url of the story. You might not have the legal authorization to use the image, in which case the image field will be empty. 
* **longlead**
The lead for the story. 
* **tag**
Topics mentioned in the story. 
* **area**
Regions and countries mentioned in the story. 
* **industry**
Industries mentionsed by the story. 
* **author**
The author or authors of the story, in string format. 
* **timeStamp**
The unix time stamp of the story publishing or updating time. If the story is updated, the timeStamp will be updated as well. 
* **type**
For reprint, the type will always be story. 
* **id**
The unique id of the story. Use this to get the detail information for the story. 

#### How to access the headline list? 
We'll share the access url and token later, after completing the legal process. 



## Detail

Let's look at an example

```
{
  "id": "001093516",
  "cheadline": "分析：航运成本涨得更猛了",
  "clongleadbody": "从亚洲向欧洲发货的运价飙升在最近几个月格外迅猛，而这可能反映了整个海运市场的广泛通胀趋势，而不是个别瓶颈。",
  "cbody": "<p>过去一年，从亚洲向欧洲发货的运价飙升，这一涨势在最近几个月更是迅猛。以下是由Xeneta编制的图表，该机构专业追踪在远洋航运船舶上预订40英尺集装箱空间的成本数据：</p>\r\n<div class=\"pic\"><img src=\"https://thumbor.ftacademy.cn/unsafe/picture/2/000122642_piclink.jpg\"></div>\r\n<p>自4月底以来，每个集装箱的运价已上涨约6000美元。</p>\r\n<p>跨越印度洋和苏伊士运河运送货物不仅变得更加昂贵，而且服务也变得更差。咨询公司毕博(BearingPoint)专业从事供应链管理的合伙人埃米尔•瑙斯(Emile Naus)称，出口商满腹怨言：</p>\r\n<p>“我们接到了许多报告，称即使支付了高额费用，集装箱仍未能装船。这无疑导致一些客户过量供应产品，以求维持欧洲的库存水平。结果是仓库容量将会出现问题，而这无疑会导致牛鞭效应，实际上会导致进入2022年之后航运量出现更多不确定性。”</p>\r\n<p>据物流数字化机构project44介绍，从中国到欧洲航线的延误也在增加：</p>\r\n<div class=\"pic\"><img src=\"https://thumbor.ftacademy.cn/unsafe/picture/3/000122643_piclink.jpg\"></div>\r\n<p>在许多制造行业，疫情初期影响商品生产和分销的障碍似乎已被克服。在Twitter上拥有大量追随者的独立宏观交易员马克•道(Mark Dow)在上周五的Twitter Spaces上告诉我们，他现在认为，美国已经达到了一个临界点，即新冠感染病例上升基本上不会抵消经济反弹的影响。原因在于，到了这个阶段，企业已经学会了应对，以至于他们可以轻松承受病例不断增加的影响。</p>\r\n<p>然而，我们在亚洲至欧洲航线上看到的情况可能反映了整个海运市场的更广泛通胀趋势，特别是因为从东亚到美国西海岸的货运价格近几个月也出现攀升。</p>\r\n<p>的确，在月度环比基础上，运价上涨了20%——高于东亚至欧洲航线的价格涨幅（尽管从上海发运一个40英尺集装箱到洛杉矶的运价仍远低于从中国东部港口到汉堡或鹿特丹的运价）。以下同样是来自Xeneta的数据：</p>\r\n<div class=\"pic\"><img src=\"https://thumbor.ftacademy.cn/unsafe/picture/4/000122644_piclink.jpg\"></div>\r\n<p>运力不足仍然是一个问题。但分析师们认为，推动近期运价涨势的因素之一是中国新冠感染病例增加。以下是project44营销副总裁乔什•巴拉齐尔(Josh Brazil)的分析：</p>\r\n<p>“船舶仍然延误的事实，加上现在中国主要制造业中心的新冠变种病毒感染病例正在上升，表明随着我们接近黑色星期五和假日购物季，下游可能会受到深远影响……</p>\r\n<p>……2021年的少数确定因素之一是地方性延误，以及情况可能在一夜间发生变化的事实。”</p>\r\n<p>现在的大问题是，疫情期间一直存在的拥堵状况现在加重了，这会造成多大的影响？我们已经看到了全球股市的一些紧张情绪。我们会开始看到它对商品生产产生某种实质性影响，抑或企业会变得更善于建立库存？我们将在未来几周内找到答案。</p>\r\n<p>从较长期看，分析师们日益认为我们会看到生产回流(reshoring)；企业纷纷表示，他们会把供应链转移到离本土更近的地方。以下是毕博的瑙斯的看法：</p>\r\n<p>“运输成本增加，加上交货周期漫长所蕴含的风险以及对贸易限制增加的担忧，现在正迫使企业重新评估采购决策，这有可能为在更接近市场的地方从事生产打开大门。”</p>\r\n<p>不过，回流说起来容易做起来难，所以我们将密切关注企业是否真的朝这个方向投资。</p>\r\n<p>译者/和风</p>\r\n",
  "eheadline": "There’s yet another surge in shipping costs",
  "ebody": "<p>The price of shipping goods from Asia to Europe has soared over the past year. But, over recent months, the rise has been particularly dramatic. Here’s a chart put together by Xeneta, an outfit that specialises in data on what it costs to book space on one of the 40ft containers across the world’s oceans:</p>\r\n<p>That’s about a $6,000 rise in shipping costs per container since the end of April.</p>\r\n<p>Not only has it become far more expensive to ship goods across the Indian Ocean and up the Suez Canal, the service has become poorer. Emile Naus, a partner specialising in supply chain management at consultants BearingPoint, says exporters are full of complaints:</p>\r\n<p>We have had numerous reports that containers are being left off vessels even after paying the high rates. This has certainly caused some customers to over supply products, to try and maintain stock levels in Europe. The result is that there will be an issue with warehouse capacity, and the bullwhip effect this will undoubtedly cause will actually lead to more uncertainty in shipping volumes well into 2022.</p>\r\n<p>According to project44, a data logistics outfit, delays on the China to Europe routes are rising too:</p>\r\n<p>In many manufacturing industries, the hurdles to making and distributing goods seen during the earlier days of the pandemic seem to have been overcome. Mark Dow, an independent macro trader who has a large following on Twitter, told us on last Friday’s Twitter Spaces that he now thinks the US has reached a point where rising Covid-19 numbers would do little to offset the economic rebound. The reason being that, by this stage, businesses have learnt to cope to the point where they could easily stomach the impact of rising caseloads.</p>\r\n<p>Yet what we are seeing on the Asia to Europe route may reflect broader inflationary trends across the market for ocean freight, especially since prices for freight going from East Asia to the US West Coast have also picked up in recent months.</p>\r\n<p>Indeed, month on month, the rise in freight costs has been 20 per cent – higher than for the European route (though the cost of shipping a 40ft container from Shanghai to LA is nowhere near as expensive as the journey from China’s East Coast to Hamburg or Rotterdam). Data, as before, via Xeneta:</p>\r\n<p>Lack of capacity remains an issue. But analysts think that one of the factors driving the trend of late is a rise in Covid-19 cases in China. Here’s Josh Brazil, vice president for marketing at project44:</p>\r\n<p>The fact that ships remain delayed and now Covid variant outbreaks in major Chinese manufacturing hubs are on the rise, indicates that there may be far-reaching down-stream consequences going into Black Friday and holiday shopping seasons . . . </p>\r\n<p>...One of the few givens in 2021 is endemic delays, and the fact that conditions can change almost overnight.</p>\r\n<p>The big question now is how big the reverberations of this intensification of the logjams we’ve seen throughout the pandemic will be. We’ve already seen some edginess in global stock markets. Will we start to see it having a material impact on goods production, or have firms become better at building up inventories? We shall find out in the coming weeks.</p>\r\n<p>Longer term, analysts increasingly think that we’ll see reshoring, with businesses saying they’ll shift supply chains closer to home. Here’s Naus’ take:</p>\r\n<p>A combination of increased shipping costs, combined with the risks that are embedded in long lead times and the fear of increased trade restrictions, is now forcing the re-evaluation of sourcing decisions, potentially opening up production closer to the market.</p>\r\n<p>Reshoring is easier said than done though, so we will be keeping a close eye on whether companies are really putting their money where their mouth is.</p>\r\n",
  "cauthor": "英国《金融时报》 克莱尔•琼斯",
  "tag": "航运,港口,供应链,吞吐量",
  "industry": "airline",
  "area": "china,usa,asiapacific,europe,Shanghai,Brazil",
  "pubdate": "1628611200",
  "last_publish_time": "1628640922",
  "story_pic": {
    "cover": "http://creatives.ftacademy.cn/picture/3/000110873_piclink.jpg"
  }
}
```
What are the fields for? 
* **id**
The unique id of the story. You used this to get the detail information for the story. 
* **cheadline**
The Chinese headline of the article in string format. It is the same as **headline** in the headline list API mentioned above. 
* **clongleadbody**
The lead for the story. It is the same as **longlead** mentioned above. 
* **cbody**
The Chinese body text in HTML. If you are rendering it on a web site or in a web view of an app, just use it directly. 
* **ebody**
The English body text in HTML. This field might be empty if you don't have the syndication authorization for English content. 
* **cauthor**
The Chinese author in String. 
* **tag**
Topics mentioned in the story. 
* **area**
Regions and countries mentioned in the story. 
* **industry**
Industries mentionsed by the story. 
* **pubdate**
Unix time stamp of the date that of publishing. Note that the time will be 00:00, so use it only for the date, not time. 
* **last_publish_time**
Unix time stamp of when the story is last updated or edited. Sometimes a story might be updated months after it is first published. In this case, you might want to display something like "Published on Jan 1st, 2021, updated at 13:30PM Aug 30th, 2021". 
* **story_pic**
The pictures that are supposed to be shown as of a cover of the story. Just look for the **cover** property for the image url. If you don't have authorization of the image, this will be empty. In that case, you might need to find a story image using your own authorized image service, such as Getty Image. 

#### How to access the detail info? 
We'll share the access url and token later, after completing the legal process. 

