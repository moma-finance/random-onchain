### Lucky winners of LC holders

🎉🎉🎉 Congratulation for the following addresses.

```
0x1da5407a15e082e5f538e1c9f1bf3dcf812d1e15
0x8a830c7db314dae2b93b8dc4c263240e97c02468
0x6cef4e034f349db138210733e127188cc5deaf4e
0x62fbbd8d413ae47e97f96c58b08d989e193c27c7
0x75458b96ae82553b2fa55f67e262cfea373b7996
0x5fa797f9dbc8053b6aab7153c27d1a870f418f6e
0xc53a9720211ad3370fae5837371462b1eb1de0db
0x73672c743b2784d9c5971564481c7a7cc3c51bcd
0x0f1e2e83055b65d541bb2b488f285ec541483637
0x91709c57bdcb8c55993c39855e85eeda6e728a71
0xa31a515de43710cadadf65146956d4a8250f1c51
0x124b5d4c2bd5607d6613e66cfb512c5b1194f2e4
0x7d08a1ce2624d8893dbe5b7eb9600dc7138f51e0
0x7057c2f18a21f23030f32a2bcf57d73dd550a329
0x336a57ceebf7b04abbfd2a87e6c29ff6d6c0421e
0xae5d29a3825b10802f3d811065edea61cba1010b
0x78fbedb25c5c6ce79c8e285401a18d5ada98338e
0x16f610963685142e3090dc7408f2c7a187a85419
0xa422f988500f7ef8d8e7e4b105576cd94cc5000d
0x449679d9c9e84b92640e33fe88b58d0185123b0f
```

You can run this on jsfiddle.

https://jsfiddle.net/chrisWen/pj4nyszv/3/

```js
/**
     * This is an random algorithm for choosing the Lucky winners of LC holders
     *
     * To be fairly, We specify a blockheight on ETH
     * and the blockheight hash will be the seed for the random algorithm.
     * This is truely decentralized and pseudo random.
     * The blockheight hash will be hashed via MD5 for the random seed, and choose one account,
     * and re-hash the hash will generated the next account until all the accounts generated.
     */

    // address list
    const memberList = ["0x547336a81573b149b9e28bec3a33534fedd3c6a4","0xed71046f3f1b5130609df6f5a0468415548c5b2c","0xc31437bfb826695442b7c7353c7ef9e6f2389f21","0x3f6baa29c18070e1cd20f81168906fb4544d9e86","0x7417e3bcde8726908895152a8f3925a756b1894d","0xaf124b08ebdb366c004361f310bf4cc8ac012db6","0x091e0181545caf986075e62dbb3af931937d66ed","0x7eb135ac7c92ef2ea84c0ca5241f8c869f40d57a","0x1f0f5d02ce4043615e7d540d80969bc5575b592b","0xa326a017767443ea5fb8021f2904be7609c34adc","0xe786c0aee7f4348ee05a0734b2ec44ac71b812be","0xa4f8322e04f38f1b60e44f3f5e9b0a54f34d3af2","0x76322f53b91cb8849dfb2007ed862940934b3520","0x84c97f2cefd07f40343c4873b8bd86394e25f0dc","0xa8e8c5adf3e714c682150d2f81ac8d5bfa2050b0","0x662e2984f46d191c28b16cd62439d9dca8b3d6e0","0xbd85fe9456e6acaaefcd8a80d157c24a9c707120","0x336a57ceebf7b04abbfd2a87e6c29ff6d6c0421e","0x71eaaaaabb876dec15e2a8b6c169e95aa76d6b51","0x152b858ca8e0e0e33a20bd862587e26605719b0c","0x6fd804a998bc7d5d112262a732510c3d63caea0f","0xe408fbf01e45227491ea27e610e473b999164d63","0x1a01e529c5910be6885aebb67c3e2b0063132669","0xbbc523178cb17c5996be5f0e63f67ba8df8e6829","0xb6291676ba9c8f2a8744311857550d6a4fa09b63","0x2961b02dce896d5a63b57997a1ae124736de2cf1","0x6c1cc0c522f4e6c53c667ec3a09080016926d870","0x3d3a165036db7836901c5e58703ecf27a3c33f72","0x449679d9c9e84b92640e33fe88b58d0185123b0f","0x6e2463d0a8d8f2729a6e28798af7bda770a99a1c","0x988d5689281e0805eedc105956b51aee15f085a5","0xccf0b3bb70ba43383099632dec931760c0523c78","0xa002a9b5adec606cef8e62e1add06ecabc6016de","0xa94c6516e2bde1c9e0597c6f00e47905ffe4f640","0xe0d6c60f65d39c59435defbf2ddb3094c4e71564","0x6cef4e034f349db138210733e127188cc5deaf4e","0x94f56029b2dab6c19b3fec80387d1d744c8f811f","0xa24f5177ba221d232f0a71c00c1486417003936b","0x9c3cd3bf78771ef45059c11e7edfe8cec2d8d931","0xa3141ccb226e557bb50baa1fa61e8f98b6f93934","0xe783e44abab54a6ce2084d9bee83eca5a1ca2e63","0x15082daefc5e43dcfd1328e60a4735931abf73f8","0x0bd0c9401e80dd5bbf17d6ef3ec11ca7403a7b50","0xd8b7c7ffdf60a040e4567814e1930045a65e5fe5","0x8728c811f93eb6ac47d375e6a62df552d62ed284","0x4504051dd0fae21d475ee689e435569aa412cfd2","0x764a41fb769a1ff9bae1e561a5fadabf32d86f62","0x984615867070374a0c6090adc5609990bf3b620e","0x05a5fde0bb75263678c2b41186dbebda4d001f7a","0x3316de43472c80157189b78d55dde2bda082a952","0x1a1d4d486da086db1912b46b18bee6281114c8c9","0x087e930fbd6d3c02fd5df2653a5c53864d2544b8","0x97b77658af6b9642bdf624773e23c5728ff4e2fa","0xef367d7051ffea135b0e6373bd820e3b9bd4afff","0x59858733cf5c4ba6c8d67f568cc2cd299814c260","0x6dd3d478476ae72b8ef9a73c75d54a4ee0dc8e53","0xf144fcebdb84fd3bc070108673d6290940aad756","0x5608d20d31d496ec1a060fffd1d7b579aaa7c166","0x7284da6d6424630e8413d0e99533668f468b3fdd","0x8de5c22ed4902b6b795120304db7db5e70b90367","0x6636634f83198b3c0d3170797b6c0a4a9de6932e","0x73ba1f2ebf10695059bf03dffadf1f91caa69bdc","0x378be4e804774c9eee2110ae60dc4a5b4b3f67f7","0x94a6a15e6693f5bab746f5700c64014ad06ded43","0xb224946c9111b08189d8ba371dc10bc8a086afa6","0x2415c64242e0662ee81c597c3d49baf7abb59752","0x0174985e54dc765c88a68494e3f42c263912e3f2","0x608564e9a4fac4b4736ecff963b0b73ef5d3c3c0","0x3484fb916eea590f231f994bbe27028cc58013aa","0x8e1700e063d4341930c0d071c168d17e506caca9","0xbf197ed412dc301867f3c6c82e80024348d0d67e","0xe92da269bbf46e3c5f194dc65a1f59b09b793a10","0x09c7a05635b9e755369871cd49bd8b400dc5df1d","0xb28f7d9fdaf92c57f736060fa32154754c73d256","0x1cf5d43a025c9c9ec7f74c98bc14cf9e9dd451ee","0x831987a1bfe8858972b82ab770b03ee6d94a974f","0x54cb9b1642a0e74a5b0df60a6b5a46f3f86288c6","0xf51514c27f6b46ec9e9f6bb08b0f589762d50a1d","0x4555ff1256c5d5a91ebf161361d5bf4a215783f5","0x5789584469dbea9b1e6484eb5abe7f36d20ae54a","0x35d8688332f22affa5508be93adf2f550d3aac41","0x92b1f9a6562e50b1cf32dfd234d62c16591e10c1","0x67ee0c63a37667d8cd55e9d02712d8826dc0cc8a","0xf97bfaed84676a853c67f7e394396a6bfa048e65","0x9c7d3135fbe752b3d73d962685dc2f21e3863cb9","0x73672c743b2784d9c5971564481c7a7cc3c51bcd","0x087e146e8b9c8181b02d460e86eac352ca33f16a","0xa6d34040965060a351f857906c344d869991e04e","0x4c3a9d7e0ad6da7f4e5f6b98eced4382a2ed3429","0xe3a034e7938ec7bff6e4cfc718dce461f9defc2e","0x4b34d40dde7662852f493e1343d185c2bd0565ee","0x579fded77faabef2c969662de2d5b96fe9a16e00","0x9f386cf63d749e65328f3e2519e474b60edb86c1","0x37d04c7b571482ea1b16d778604e18f8f3e195d7","0x58675d3aa3b1afdc7705a97ad7a9c86088373acc","0x7a93018c1b41c970db18c531c60b5fdeb126d248","0x0fd5e9ef5af57e642d7d67e742e8ca899a668c46","0x5e01eeb5717489532b3cfec2f676e74b9eea4a3c","0xdce5774d32eec7a0e7c727ca6e4865922c506002","0x7cb01773130a45fe22452d34094c5dac98d86948","0x7c089b41eeadff9b3d89fb76ef87155112e3f1ca","0x5aa1eba0c0ece56e198c289ac413ba4bd4bfa700","0x1e083b190bc6d3ba7af1e11bbaaf68b03be48114","0xa422f988500f7ef8d8e7e4b105576cd94cc5000d","0xdc4b871756c892afbb9c9a2ae7cdf38bbd2f25b8","0x1c0f3523a85bea1518f34af636a6351fdba4a8e6","0x323b06f8a39c87645b6a717884a8113861114f2b","0x4cdc770e8bcaf897a7e96ce68d44c76f72ac2fc3","0xeb07d82497cb04a4c037bc0abde5c6d50e5e24fd","0x4819ad67cd561d0eddcaa832edd16b75e9ea7ca3","0x3edb09d96eafdadd22ed6137036b8a9b9303ff6f","0xd3c5e9dca16841de51341cc300bb9b0c6707982e","0x29b0c066b34688fdbec10b43dace4782b9970635","0x1e1c8535f79aaeb030c47427966a3674fccddc17","0x94117b3b675024aae07f0ef864cbadf044ff3bfc","0x38b1af52cc99c9ab9308b9be7f0c69c31dd0350b","0x87b2e973b394215a1e651ebeb630360337f318a7","0x7a8832e7377b8a0911f9fb594ac4b741a8d10836","0x83087bb0d018595b903bce5f957ad861a9f31c5c","0x1529fc5961281730a22c72d16d41fd4dda1a61eb","0x59b54862d487d0032c82f8db804eef8868e978ee","0x4d90cd83c0aac70628607a3b808ac452a06c155c","0xa9a4a3783be7a95bfac09d7f5665ba361b19d1a7","0x64fae0196cd4753346ec02e8576978b158cd5ecd","0xaaf5d77af3933685034ff7695774f7a47c3fb519","0x08c5efd2fc32012637ea7f70d086275abcf0feb2","0xb67c6bc2b1aff0da257bb90bc35c9bcff6cd8523","0x8ca10faa308f347588f760cecedca200dae1cf3f","0x7057c2f18a21f23030f32a2bcf57d73dd550a329","0xd11e3e1fb16da822b172b331630c3e2c93bf559a","0x0bfe8b2bda40aa61d6fcfd5a7f036fb935c66f14","0x98e6fd92fecc50a1bcf0845d09552fecbe1ed58d","0xdced5b1d40971144819baaad85582170c7778d17","0x20431ec0e151b62f90e2c0e7db22c1aee6607357","0x2d4b2e68c42fb25b88d2d748bc3503889d8ac65d","0xae5d29a3825b10802f3d811065edea61cba1010b","0x232bc923edf1f4f7243522f619d34a6aa0580514","0xd293114b9ca90896d486983d64c4a6523f855bbb","0x8917c561124dd820aad3db87365ca5b3e7ebdd9e","0x5fa797f9dbc8053b6aab7153c27d1a870f418f6e","0x4522dc5cf98f34c3867b0c415148d9516f42f0c4","0x0e5818a8c2fb842852ccc1ae101d831caefb8d23","0x9c6d8bccc0179ff9e0bfc2ba76565a32849bfe76","0x2f3986e87a121f629331f4cb898b4ceabe0f236b","0xe1e7809200eb4d4326f145c8aa24bfc947139ddb","0xaa0fadc33651125313a8b32d9f792813f6a5bcd6","0xe827fde3e5ea659587d37437c859ac82812e371b","0xad2cd72b0988def5ad46eec96483d59a823b8cac","0x47eb4b5371b65e3c67bcf655c58c2f3a05dc4a94","0xe63b9868a4e46f161ed05d4546dbb06201606311","0x1aa68932b83da224155d68f32f1b5225c98331b6","0x8a830c7db314dae2b93b8dc4c263240e97c02468","0x0f1e2e83055b65d541bb2b488f285ec541483637","0x3f233acc95567ce4922494f2cb466cfb36c22e11","0xa6f8473a1912e17cd2f022b40150dca0ae658872","0xb4b940d7641f0b8c261ca31823f829e4781f8e94","0xe34a97cef354577f7f5f2f0b0230b3dd33a766c0","0x720396b8032dc205fe9f21c268c84f0e85da96af","0x736c3165e9f8eb0a8ff4b3846c34a3292aaa0fea","0xed6a6de0b7300d2475eb9c7b847fd3bd0fa712cd","0xea428ed20c2ed2687ed099e11989679789e7f503","0x391d1726fe37ae5f6c4a6a9fc5cecf795eef6169","0x5e9c664e51c58f5b912f1062ea4c68c16080d2c8","0x14786310da605118e09b20079b1bacf3e6bc499a","0x4b85caaef196c9a6b773e7b1a517c573c82480ee","0x124b5d4c2bd5607d6613e66cfb512c5b1194f2e4","0xe2ac58af9a9348416833df8c72d430ec957f5031","0x4398b105b08343015aa1a113be8f382191589100","0xe9840f9d80edf94da2c1e70af0a498df90258330","0xf74709b52c0e108ecfe56fa364175a779d3c059a","0xd1f3d67f856b3ceef1e7ca302d29c452a6affe1f","0x8f4e5df66b24dfe486787d9c5b21666e5f5da0a1","0x013356e757d42a5f8a107732a96b28a22372f2dc","0x78b74e053d0ff2c646ecede5db4be7820368a35c","0x05580b7f012c40f0ed632cac5452baf95e1628bc","0x767a4ddf3c666658d13f490cf47fd117f4bd0883","0xfbc83354c73b4d93c81ffa910892194e69241f24","0x9d63b1ad4a48c4c007b75c07950ed6a697d56745","0x2764a735b32b1df4287fb5d7b556f8004d82abb0","0xe0a013a77c2efef233dbcf2175fc2681baee47e5","0x1860a619d26f4998c3c5fac85738ecd912bf34b5","0x2f9f8172efcc1355e5a18449d9b5b1041b3e4f8f","0x93cb1193f316f218eb2daf0c7b958913da39b699","0xad615f88d4483b80dd415a0cf533c027d6ecde01","0x70d7cd6c25d2c4f375cfd6d525ac390d03917060","0x30cabe45fbd375fa653bf7e9b283d24309264271","0x492304b35e839278dbac40428bc5b0f456c85804","0x59153815b6ae6558743d8d33922e35165418c647","0xdc3bdb21870c0789c71d889bc6a84c14ad778c99","0x3f271833fcf32092de39fdbfb5b6acf35efb398c","0xbf277a67adc411b86553410b5ae0dc5df1027f01","0x0da47a3f0c62a44c4b5fbada03563529c2807474","0x9e94f475f354c9ac806ae558a99f51675eaa60dd","0x23c14e77e980e8d90851c72678ec5f4255af7874","0x165af709d0770886bf0e46a727cc46ef40f558f1","0xa218a214e35cf339eed1e3e0fd9ed996dc792624","0x395f23d33e981d6e1b5930571955c7358b3a14e8","0xf1caf8cbcec5d193aef9dedf8cfd80b58f156146","0x33231c4171e4d6a864c05b6db61467ec2424efa5","0xf93398d57c34aea3238e9e893122d021f49682af","0x0a3b4905b0a7bd42645c8f0bda9f3bc213f09610","0x72eeb2f7ddc963bbdc35c3114c45f1449edec685","0xc8e7ef5783f1432c41c683ef4733333cd85a4c74","0x971eb3a97ceadbcbeedbada059a310e6485849e8","0x5edf12bbe15db61aaca7ce44f4f00bd49475ec60","0xe98a708e30a86674a85654c891f715ec3fa0c461","0xa2fbcefa58d2fa7a96838eef4e8b76c4a6afe73c","0x52cef6d24c46e0bc5792fd0b32e0d581ae243f8b","0x53b043c02ec234f5d1c03ce3f07c0dffb9d48cb9","0xa5910df0ea874ae66ededef0dc2bf2dd0aac3304","0x47a3a77755fea1a84a459f98a0b2aac858e50ee1","0x038dd7d1fac33e24ce5b813364be85e9e4a86f10","0x9f3ac73c80772e53f980dea54874a18324b0d1be","0xab1ef6a2bd769dce3da9cd96e8f16f00f50ee6e6","0xa6ba594aaa2037d48935235a02456aacf419060a","0x503387a6e6759787e281e811bf1d97a0416ac73b","0xa31a515de43710cadadf65146956d4a8250f1c51","0xdd69b023be4947b9d53962f0af324ceb2a456fc2","0x10833709e91ed5cad88967f1364ab88b712fd32d","0x665d0d2bcb316814af5ec7e110c8f9429ecb0bdf","0xe7156eea06ee667a03782f15fd3c68023563767d","0x996340c05889bf55cadb6294d0aef48344b064d3","0x14e0693e3273712c16b4da59012eab8c3bd77f9b","0x391f7561ac737a43c44c9bf807f82eac09329da0","0x46ecf089877dd0d0d58e5ec3d1dcabf7fd867815","0xebf6caf61daf53dc92b6a9b030cf642fd4c1103c","0xf33958f5cba4f00bbb6c2f571f8738548aa15c8d","0x9193b116ac46d2cb34b66ea4dd5d60254e8443eb","0xf83deeb38dec221c54cecae2e2def112c93aed6c","0xc3b00cf5a879c1b02dbb48956f5857e9a249e317","0x8e4835a38a364f09ee6d5146d9193a62da328f05","0x0f39fdb49375dd267c5a34b8e099cf2685ff4d53","0xe87914dd6ef2b762d8ea3928dae8abc6030bedca","0xc35e82f13724c7889b821e070ee126a430b04217","0x707c119e330fe6bbba0d09ff05badb4ada296b9a","0x621c2a554e0f1db85deafd37f29748c99995f02c","0x106adc03064f16b7a80385c948e373852a256ab2","0xecd8c7abae05083c7bf368e022a311c24a11870f","0xc53a9720211ad3370fae5837371462b1eb1de0db","0x8df1ddace4619fd1c2e4e7a55000338f794860ec","0xa27673d26d145fe704be1dd494cbcc9bb327d6de","0x1bf26a07737c5e772a1efc6e36c1ac1f0b2b8dbd","0x1ded3c31ec30a1c651c7d1eca0f7db3ad76d15ef","0x7d08a1ce2624d8893dbe5b7eb9600dc7138f51e0","0xbdf99dc3a9f83fc99f5b6f89c584bdd15ce79bd2","0x195dbd4b988ad2f9f64fa1b9517cbdbad65c2032","0x75458b96ae82553b2fa55f67e262cfea373b7996","0x636645ec6df10dcf57cec532910de7b6f40c4afa","0x45da129bb3524ac5bab539651321b67723664c77","0x09b9669d4f467259dbbda29b5b6ef96fd0aba520","0xc69f29c28eb5b8920f7b7f624d325d70b4dcc68e","0xe0e926989e5714e4e186f44f612603062dd7205e","0x50dc8bad9d414a2a910a8206dc42f54d2eb44aac","0x7a15a903f0e69a282d3969dc5b1f496cd2f97618","0x59af3280b832a1149039d5771d3d9719e042c57b","0xa6a51898716f1631035bc87c00636c91ddfa40e1","0xabed5ae10ebe2d1c179cfb2bcd5621426db47f76","0x331e15719e5b1e9dc8a70e4ce441c6040a81973f","0x6f5fb6fd532c7dce365adc45a4956a5ebe9c9c43","0x60a966924805e76268558b6dfb8c29e3469c3039","0xb4a7769e66bfa799e6dbada2dbe0bb1d95fa09f1","0xd25770d1f1c543d77d7117d6c2695533b024c9b9","0x4ff243ae32051fd9dbf7f62394bfc8ff297b17d6","0x1da5407a15e082e5f538e1c9f1bf3dcf812d1e15","0x87e1c1336d79c2431b7f65b41708ea7724beb968","0x22a93539e28418b7e481d6ad3b288570e349270c","0x7ccc224b0fec2095810034aaf411f6400860a626","0xedcfd46f4352d5f54460df1d02053b4311a5b0c3","0x6798a4be28e12b6346466f60f7e94c9becbf8fe2","0x2746ea53c0398963fbe47a9d09d13b6d1424e4f0","0x232fdc658332cc82b9c5faffdb5b01a59964790c","0x5c17c577df4e9ef66bc9b866854419f68dd1e5fb","0xfa6b74d5cf75f8f016bacd466af9465939ae4464","0x6fb4e5f10976d8463c13dfb3779ee7b6f56e9535","0xd39392e26615af87727eabad031f453c81f6de47","0x8b020236e39b5940bda3741c0ca553f20112607a","0xe0042de454cc6dabe3aca1742d62233980f9a636","0x3ebf904a8ced5fb00349def97460aea477bcf86c","0xfe5ac92b76a82badf65ebdeb6dfdc25870b9c567","0xd74f2b65a1bd98f12df3871cfdc6b81a36f7e1b8","0xc1166d060f85112b61b2894bfdfa40fa218f80f1","0xaa82c64b5799b4dfd7cc973adb9166a22882eaa1","0xed90fb9b4407ca92a16ab3a8cf6f27a3c508fee8","0xd26a0a35321c6793e47eb602f1676c915caf111c","0x3ea37a9ead12f5401109cf8ca3b1448be7eb4706","0xec5cf969c43fc0b79bea91208c4dc431d36ce613","0x11ddb6cbf950a3e086e8d2c146e7270c204c65f4","0x58b1b7a4614b126f32421c2e47a9398f0c01eae5","0x255749ce8ab1dd14c09787e7405a15ff17c24459","0xabbb90ac2412542b6a71961edd05100203c1ccea","0x87041f4952f40587ecfa69a0747a66a820f6248c","0xdb2c94bb68eabd4c5034eb77556f8c0cb3501f70","0xdb3f4e5950fdca443d0a247a82d6829a2687c772","0xb955db051bf09a645c26730752e28f5e3776088f","0xc013122ef9df0e92c7654878908c47f63a77c247","0x7d43237e2cf6bb7ebd94bc6d772ab5bed22d5d5c","0x1c28073c81aaf9d701787c81d755b86ece4964ff","0x266c7e681928a7980d3782549a6fba02954ad343","0xb19d09f423215c2e8d4b17f9040f0d6fdbe8979d","0x65fb3b9597233e82181e48cb8049fa6d8aa90a99","0x544d45e001f3795b3f5278b7ab8b65014fa66033","0xddbb3abbff1b53da88146a0aff05da3ce7b723f6","0x665bf4b986614b4820d6612a9f6d5d57e45cd080","0x94f401c68b0786d4bdc6af5f8c04c4330b301cc9","0xcd49e58a78176a201c940ab7af41cd5709cd16f6","0x31c2db456164719aec621a307e1538bb49a1c245","0x91709c57bdcb8c55993c39855e85eeda6e728a71","0x5c2236dc7a282d722e5c6cc100133065e231c7ec","0x9da962e0013f0fb18e236e956770c8fca036fb69","0x62fbbd8d413ae47e97f96c58b08d989e193c27c7","0x79d9f7874ed660017aa6dbf0ddc5b3a3212e1860","0xd42f7148d63e567126f3f436b745c3ada2f2afa6","0xf61f4971ec5ab94d62f2e9e600d17daf512f0c06","0x66016b95a53b198dcee8ecb91b13cdfbcbf0f9d3","0x89e74d2fff9e54af9531de44cc11bf24b8b115a4","0x92acc9b1b73a385b91319c9e5f916a28cac32a75","0x69187183e33161ec98f77f9154feb61de56fb53a","0x02704cfdcaa744573fd09689c51fff5c193c4c72","0xb8ccaa56e940c8a91ad3a6a7b0f9bd5473d0b9d6","0x50d79b218607661d3669ee378bf880c264b1568d","0x2c94493de987305cb781df23d2084c160a3a8b2c","0xb1e6cf9f87a0cdc408e83d81602da27f0dcb6636","0x46e78e1498a647eafbc9fb303bb8b7b373b56b55","0xd079d2e8ba2938317acaccb9686e31ba8f6ddbc5","0xa3585126e97d17de94a77289c18cb7cd03f19bfa","0x6a3237bafbd5040bd06bc35281816ae538ae2a78","0x6f2752bcf04ad3bd569f8523c146701088db8b2a","0x306e9899bae8041f33edf74a66337d0c0a2b1a79","0x2550fa32d1e8b5518ed8dc504c71a98f10576204","0x37d037e11179ac734697763cc915e06c1ff8dda6","0x16f610963685142e3090dc7408f2c7a187a85419","0x9160631e2d921deeb7ea438b9af1336aa81bb7b7","0xf9fed4b7a8a6b410fb6b1d76459b66d05c613e49","0xb6ab1d2dc494303e6bc80443f73d1a129aeed085","0x812abc741326f05289a66013b86bd80d99ba530a","0xcb8def876e8e81a5d6a4338c53e8430f37451805","0x1b3163d14c7bd42d5f10fd0e7388e318ac9f14a8","0x8064c7d9002cabcb50e3fade0a1b7824b59bcc21","0x0d7ac1cfac50e060976e0bdbc8db5af7448b6f89","0x78fbedb25c5c6ce79c8e285401a18d5ada98338e","0xd8412e72561ad7a4b68607a2f53f0b667916c2b1","0x9e0a67ffe1d5ab74d9a58faf39f53e409d30136d","0xca38e418975eee5d82b622e19096088ca6d95b68","0x229dd79002a59a1cff530f0da0f769de94c6e8b2","0x7dce8ccc7571ca6f324b56e1716d1c953149a936","0xbaf64c7f55c7d951e93b1c7a1f6839c6f6c2120b","0xc59b04e3da7f303b34f27bea63bbc52d0bc927a6","0x66ecd2cfa285acd3ed272a733cf886d35428f72f","0xf064ad63a7b1a62856da540f94182be5163a1366","0xfbd617a6a5c0418ccb8c1a35f3ef4fbe0cb8b4ac","0x2472c5e9d512bd3cc33a533614ee7085d8190d01","0x55f2d4e778931eced6105379c9e4aaf57365a7a7","0x2db347b7dc44d72f6be817b13abe367ff80cfcb0","0x5795f6226d425d29d8fef61c1a826252c1819488","0x026f5122fde2ae7348ac8d20ff1c04088d21b91f","0x2e1448d33822190dce2318c231bdd3dace6ee071","0x1c30d1125f04d1e8471ec036dbf225380f0b614d","0x513b1979be1f0aee44348677589b523f00d5fcfb","0xf6c8ac00cd108fdec13652df376b0f9dac4673ce","0x99c5c8515501f64f33917bc7180637a1901bab5e","0x1be171f1df83ee948aad26367af4b617d236d4da","0x3674a15c4e8c31e75ffa0d85f6091e687f09573a","0x4b99f6913b994813f2bfc50fd9fdad4fedbac10e","0xaf8acd3256216f098398ec575912b32c815d4a8a","0xf38eab041c65db99d8bffff04bee058a91ccdb64"]

   // total number to be randomed
    const selectedAddrNumber = 20
    // selected addresses
    const result = [];

    // ETH block height 12962760 hash (haven't mined)
    const ethHash = '0xbb716a3096c16a594addf66056b96584f776b0f10b9ad1b2f60eaf0077d1b107';

    /**
     * Hash to Decimal
     * @param {string} hash
     */
    const hashToDec = (hash) => {
      return parseInt(hash.slice(hash.length - 3, hash.length), 16);
    }

    /**
     * Generate reward list via hash seed
     * @param {string} hash
     */
    const generateResult = (hash) => {
      let dec = hashToDec(hash);
      while(dec >= memberList.length){
        dec %= memberList.length;
      }
      result.push(memberList[dec]);
      memberList.splice(dec, 1);

      if(result.length < selectedAddrNumber){
        generateResult(md5(dec));
      }
    }

    /** MD5 Section **/
    function safeAdd (x, y) {
      var lsw = (x & 0xffff) + (y & 0xffff)
      var msw = (x >> 16) + (y >> 16) + (lsw >> 16)
      return (msw << 16) | (lsw & 0xffff)
    }
    function bitRotateLeft (num, cnt) {
      return (num << cnt) | (num >>> (32 - cnt))
    }
    function md5cmn (q, a, b, x, s, t) {
      return safeAdd(bitRotateLeft(safeAdd(safeAdd(a, q), safeAdd(x, t)), s), b)
    }
    function md5ff (a, b, c, d, x, s, t) {
      return md5cmn((b & c) | (~b & d), a, b, x, s, t)
    }
    function md5gg (a, b, c, d, x, s, t) {
      return md5cmn((b & d) | (c & ~d), a, b, x, s, t)
    }
    function md5hh (a, b, c, d, x, s, t) {
      return md5cmn(b ^ c ^ d, a, b, x, s, t)
    }
    function md5ii (a, b, c, d, x, s, t) {
      return md5cmn(c ^ (b | ~d), a, b, x, s, t)
    }
    function binlMD5 (x, len) {
      /* append padding */
      x[len >> 5] |= 0x80 << (len % 32)
      x[((len + 64) >>> 9 << 4) + 14] = len

      var i
      var olda
      var oldb
      var oldc
      var oldd
      var a = 1732584193
      var b = -271733879
      var c = -1732584194
      var d = 271733878

      for (i = 0; i < x.length; i += 16) {
        olda = a
        oldb = b
        oldc = c
        oldd = d

        a = md5ff(a, b, c, d, x[i], 7, -680876936)
        d = md5ff(d, a, b, c, x[i + 1], 12, -389564586)
        c = md5ff(c, d, a, b, x[i + 2], 17, 606105819)
        b = md5ff(b, c, d, a, x[i + 3], 22, -1044525330)
        a = md5ff(a, b, c, d, x[i + 4], 7, -176418897)
        d = md5ff(d, a, b, c, x[i + 5], 12, 1200080426)
        c = md5ff(c, d, a, b, x[i + 6], 17, -1473231341)
        b = md5ff(b, c, d, a, x[i + 7], 22, -45705983)
        a = md5ff(a, b, c, d, x[i + 8], 7, 1770035416)
        d = md5ff(d, a, b, c, x[i + 9], 12, -1958414417)
        c = md5ff(c, d, a, b, x[i + 10], 17, -42063)
        b = md5ff(b, c, d, a, x[i + 11], 22, -1990404162)
        a = md5ff(a, b, c, d, x[i + 12], 7, 1804603682)
        d = md5ff(d, a, b, c, x[i + 13], 12, -40341101)
        c = md5ff(c, d, a, b, x[i + 14], 17, -1502002290)
        b = md5ff(b, c, d, a, x[i + 15], 22, 1236535329)

        a = md5gg(a, b, c, d, x[i + 1], 5, -165796510)
        d = md5gg(d, a, b, c, x[i + 6], 9, -1069501632)
        c = md5gg(c, d, a, b, x[i + 11], 14, 643717713)
        b = md5gg(b, c, d, a, x[i], 20, -373897302)
        a = md5gg(a, b, c, d, x[i + 5], 5, -701558691)
        d = md5gg(d, a, b, c, x[i + 10], 9, 38016083)
        c = md5gg(c, d, a, b, x[i + 15], 14, -660478335)
        b = md5gg(b, c, d, a, x[i + 4], 20, -405537848)
        a = md5gg(a, b, c, d, x[i + 9], 5, 568446438)
        d = md5gg(d, a, b, c, x[i + 14], 9, -1019803690)
        c = md5gg(c, d, a, b, x[i + 3], 14, -187363961)
        b = md5gg(b, c, d, a, x[i + 8], 20, 1163531501)
        a = md5gg(a, b, c, d, x[i + 13], 5, -1444681467)
        d = md5gg(d, a, b, c, x[i + 2], 9, -51403784)
        c = md5gg(c, d, a, b, x[i + 7], 14, 1735328473)
        b = md5gg(b, c, d, a, x[i + 12], 20, -1926607734)

        a = md5hh(a, b, c, d, x[i + 5], 4, -378558)
        d = md5hh(d, a, b, c, x[i + 8], 11, -2022574463)
        c = md5hh(c, d, a, b, x[i + 11], 16, 1839030562)
        b = md5hh(b, c, d, a, x[i + 14], 23, -35309556)
        a = md5hh(a, b, c, d, x[i + 1], 4, -1530992060)
        d = md5hh(d, a, b, c, x[i + 4], 11, 1272893353)
        c = md5hh(c, d, a, b, x[i + 7], 16, -155497632)
        b = md5hh(b, c, d, a, x[i + 10], 23, -1094730640)
        a = md5hh(a, b, c, d, x[i + 13], 4, 681279174)
        d = md5hh(d, a, b, c, x[i], 11, -358537222)
        c = md5hh(c, d, a, b, x[i + 3], 16, -722521979)
        b = md5hh(b, c, d, a, x[i + 6], 23, 76029189)
        a = md5hh(a, b, c, d, x[i + 9], 4, -640364487)
        d = md5hh(d, a, b, c, x[i + 12], 11, -421815835)
        c = md5hh(c, d, a, b, x[i + 15], 16, 530742520)
        b = md5hh(b, c, d, a, x[i + 2], 23, -995338651)

        a = md5ii(a, b, c, d, x[i], 6, -198630844)
        d = md5ii(d, a, b, c, x[i + 7], 10, 1126891415)
        c = md5ii(c, d, a, b, x[i + 14], 15, -1416354905)
        b = md5ii(b, c, d, a, x[i + 5], 21, -57434055)
        a = md5ii(a, b, c, d, x[i + 12], 6, 1700485571)
        d = md5ii(d, a, b, c, x[i + 3], 10, -1894986606)
        c = md5ii(c, d, a, b, x[i + 10], 15, -1051523)
        b = md5ii(b, c, d, a, x[i + 1], 21, -2054922799)
        a = md5ii(a, b, c, d, x[i + 8], 6, 1873313359)
        d = md5ii(d, a, b, c, x[i + 15], 10, -30611744)
        c = md5ii(c, d, a, b, x[i + 6], 15, -1560198380)
        b = md5ii(b, c, d, a, x[i + 13], 21, 1309151649)
        a = md5ii(a, b, c, d, x[i + 4], 6, -145523070)
        d = md5ii(d, a, b, c, x[i + 11], 10, -1120210379)
        c = md5ii(c, d, a, b, x[i + 2], 15, 718787259)
        b = md5ii(b, c, d, a, x[i + 9], 21, -343485551)

        a = safeAdd(a, olda)
        b = safeAdd(b, oldb)
        c = safeAdd(c, oldc)
        d = safeAdd(d, oldd)
      }
      return [a, b, c, d]
    }
    function binl2rstr (input) {
      var i
      var output = ''
      var length32 = input.length * 32
      for (i = 0; i < length32; i += 8) {
        output += String.fromCharCode((input[i >> 5] >>> (i % 32)) & 0xff)
      }
      return output
    }
    function rstr2binl (input) {
      var i
      var output = []
      output[(input.length >> 2) - 1] = undefined
      for (i = 0; i < output.length; i += 1) {
        output[i] = 0
      }
      var length8 = input.length * 8
      for (i = 0; i < length8; i += 8) {
        output[i >> 5] |= (input.charCodeAt(i / 8) & 0xff) << (i % 32)
      }
      return output
    }
    function rstrMD5 (s) {
      return binl2rstr(binlMD5(rstr2binl(s), s.length * 8))
    }
    function rstrHMACMD5 (key, data) {
      var i
      var bkey = rstr2binl(key)
      var ipad = []
      var opad = []
      var hash
      ipad[15] = opad[15] = undefined
      if (bkey.length > 16) {
        bkey = binlMD5(bkey, key.length * 8)
      }
      for (i = 0; i < 16; i += 1) {
        ipad[i] = bkey[i] ^ 0x36363636
        opad[i] = bkey[i] ^ 0x5c5c5c5c
      }
      hash = binlMD5(ipad.concat(rstr2binl(data)), 512 + data.length * 8)
      return binl2rstr(binlMD5(opad.concat(hash), 512 + 128))
    }
    function rstr2hex (input) {
      var hexTab = '0123456789abcdef'
      var output = ''
      var x
      var i
      for (i = 0; i < input.length; i += 1) {
        x = input.charCodeAt(i)
        output += hexTab.charAt((x >>> 4) & 0x0f) + hexTab.charAt(x & 0x0f)
      }
      return output
    }
    function str2rstrUTF8 (input) {
      return unescape(encodeURIComponent(input))
    }
    function rawMD5 (s) {
      return rstrMD5(str2rstrUTF8(s))
    }
    function hexMD5 (s) {
      return rstr2hex(rawMD5(s))
    }
    function rawHMACMD5 (k, d) {
      return rstrHMACMD5(str2rstrUTF8(k), str2rstrUTF8(d))
    }
    function hexHMACMD5 (k, d) {
      return rstr2hex(rawHMACMD5(k, d))
    }
    function md5 (string, key, raw) {
      if (!key) {
        if (!raw) {
          return hexMD5(string)
        }
        return rawMD5(string)
      }
      if (!raw) {
        return hexHMACMD5(key, string)
      }
      return rawHMACMD5(key, string)
    }

    generateResult(ethHash);
    console.log(result);


```











