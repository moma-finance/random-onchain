# Moma privilege whitelist random algorithm

🎉🎉🎉  Congratulation for the following addresses.

>0x50E519e289f76097B04F9921D1BFB5231d5a4a8
0xa73aC33E9eb19e735f6233Ac348c429b1E0Dd9e
0x057AA475a96418DD12E94b658Fc722bF77fc4871
0x528cD3a3db61d0e325BCD486bAEEe8E731720Af
0x22d59F487189eB0a0534947C00780ae193eC207
0xB5106250202Cc53eed500ce06ceCc8984319d5bB
0x42d6629c599d47b955db7a8764b17d42d1dddcb
0xC6a2361cD991dd31e69c92Da7ebf322bb0cE4a2f
0xb5dD9A630AF578Ff1183c1E1B6aD6A5f51F0023
0xe7D8b70fce45aa791b7755C6EA4943b5acDd22c
0xD7d9e248C78c3822E2aD77b76BE25A45C11d2A03
0xcc1cAA3252eb24Ca1F3d1fA3a037f6CD42D662A
0x9eecBB1ff509f297325cB292F3340342D4383F5e
0xA27AA0E66C21Ab6b68E832E2d1Bd1D8620818FD
0x92706Fc51201d4C0EbddA8df7d9954c8A093Fe8
0x27c705589A57E109aDeb738D7446Ac26f54E11a5
0xc9f0143E0fcd93de2745DEd6c06120Ec2824f61C
0x7df953D6BE5Fd9532a7E829cDF72d2A9AB27000
0x1E16f946Cd430467425869014Ae25f85413003c4
0x2b036A1A5A65aB99bfc3b6C1c0F4E9c12FaE899
0x4e7243c2681857f05891be7e916049402dd7406
0x3F4D5ABdCE02D7D014733a2abd1FF4e023EC620
xA202AD0c98309882B838290e6ad156Bb51D7B7e9
0xDfc9eBd1962aE51C7Ea59EEa42d6991Abb53d6F
0x3d5145C527E7e7e6d4e97c60b2e6e75ec792a50
0x068ed8781419a98d5dfd3dcf856b0acb40e26033
0xeF4AeBA3Bc7Ea0b08F43B9468dcd546cA1321a79
0xc35D8eac9b63CB96E97fBCf9a3DA97Ca38518E77
0x1b3AE48F6200B20164DB3Cc2d0Bd4c1B829c63A2
0xf7054231cB6c2b266E10BA65cf805b0b5B92d82
0xF42aD66F4b66628584f2E97421A008d62A8f116c
0xA268fbE8e0e385BC97b2fb91a4fc8E346f1c92D
0x7D41abfD292a51b5aD1D346B592128f94d17fCBC
0x25dDe5917A0588d2b8E821a66F196fB0719B047
0xC0C2429B8008b35de73B53acA235C1d5591c412
0xc61CC53572f07062731b21685F07fb1d71495fC
0x435fcD37f72eF03dc5617d1090A6e7EA215726BF
 0x1aE0111b44Cc9dB31956533bd7da6dA8003D60d
0xa5Cb77A17379A17c3f3DC0E422ea969e9aF2f356
0x83a1f862f0b23a6A8bEaAEc6a92b201102B4F9ab
0xE40de2b86813F454E937c7f84453A15b0B88B65
0x340dBFf051837387Dd7e3468B30bAAA3B0e8d54
0x96cf8D095C6366780f44BC08e82c6368b93F3355
0x01923f1AD323d0e2B87b461125935469a70427F
0x21ef5E9d3bD810D22193E406FF31Ff486621447F
0xcE148372369B5B75aa47709Bec0B59C8215e0935
0xCB2528F7cA156e39A281bAF14D875C3d973352cD
0xCFbA850249Ab4Ae3f8961EcfCa5440D2BdD5cA3
0927b6D4D3D8B0eBe9bBf04181F563c547B6B579f
0xF00f256173E1e3270d72f492eF14F60Dc3746DB

You can run this on jsfiddle.

https://jsfiddle.net/Sirormy/49cbrhq1/1/


```js
/**
     * This is an random algorithm for choosing the moma privilege whitelist addresses.
     *
     * To be fairly, We specify a blockheight on ETH in the future
     * and the blockheight hash will be the seed for the random algorithm.
     * This is truely decentralized and pseudo random.
     * The blockheight hash will be hashed via MD5 for the random seed, and choose one account,
     * and re-hash the hash will generated the next account until all the accounts generated.
     */

    // address list
    const memberList =  ['0x7dBb250540968196800193262dF767DAC3C9d71D','0xfD05f0D167d01228225bD232fD6Ef823aD7743f','0x1b3AE48F6200B20164DB3Cc2d0Bd4c1B829c63A2','0x770Ede7DcF172af5511345d637885019DC62fCE','0x41C0Cd2EEbA336159b5374Ed1bd3aE1579dFe539','0xe408fbF01e45227491EA27e610473b999164d63','0x9D65438F86A21B83322ca9C094c7C71D6741083A','0xEEe84f290b17915c1AfAcd5878c294f9b7fb35c','0xd709755F57FF1D277Ec4E256E0cCA6335B55d027','0xb854e584370bAEb017289E05AF9256acFB9c153','0xe3Deff60EEA92e10F332cFdeC50053907cb1ca36','0x3F4D5ABdCE02D7D014733a2abd1FF4e023EC620','0xa5Cb77A17379A17c3f3DC0E422ea969e9aF2f356','0x911ccf5F6C7BD5fb25188D41A536890c3c8fAE5','0x63c1e553014905b1C8852e0570b1c019cdDcCBA','0x5d0287472ac8fE3Ae3fA8461C6f2f0401eff01EE','0x012D282ad974518db24d876063cf8adeb84E994','0xFBF54Ca4920a056f5741064d935f89210Dea7cbd','0x3b0c62DA39423dc6E4D4af5797fc21374d2D8D3','0x9Ba6baA919BAc9Acd901dF3Bfde848FE006D3caE','0xC0C2429B8008b35de73B53acA235C1d5591c412','0x95c00D2cF32EdBa4CFec2Ef6086829942aAD70A0','0xDfc9eBd1962aE51C7Ea59EEa42d6991Abb53d6F','0x25fd0f00acf01f2fee8be0e3d3373fbd5a4df978','0xbD2349f0BFf23FBeEA70Cd14D923Ed08c5e480F','0x057AA475a96418DD12E94b658Fc722bF77fc4871','0xCFbA850249Ab4Ae3f8961EcfCa5440D2BdD5cA3','0x528cD3a3db61d0e325BCD486bAEEe8E731720Af','0x6806c6A629c1e9706ae509e211beCFB25795c809','0x5fB45a090fA369bF17079C3c138EE241CAaD38E','0xc9f0143E0fcd93de2745DEd6c06120Ec2824f61C','0x3eb4875c7D631284A5ACeBF4F98532d023e3Fd1','0xE75e02DE9b5559F2eDBc673f500A5009d9e091ac','0x3F5D2058971DFd0103EbF5E423620B5A42Db357','0x068ed8781419a98d5dfd3dcf856b0acb40e26033','0x5CAf053A1c29beA426dC637858789c06f71D2E0','0x0F3306e70df05b0AeD26b6F54Ecdd4952C3e905f','0x22d59F487189eB0a0534947C00780ae193eC207','0x45A5F6C9372ef4644f5C45DAb0b1A7619F4cF981','0x2a53E397fd6bf1B0cBa7556810f8BC5a5737E34','0x5580490eBd5a993533657D1106a82e4Dca49B59','0x7787dfDA574b9A902f17df01Fd35cE5D9BFF8Fb3','0x639E482F52d9F8655E2FD4b3b2244c5CaEba81c','0xA73Ad1e1526fB3cab260a9124E303fb6457b26d8','0x4e7243c2681857f05891be7e916049402dd7406','0x642d38840ebFDA55911F83B1Cf8b5FCB1D5fce36','0x5C42AE825dC83be4440E6575C600Ca340d78Db8','0x7FF4F8FE1dBbBA8Dc27103359BF96e97a4d44114','0x503BB7A8482075351584257E2a31E444C0AeB6F','0xfAA1d64eD53C1E377497C7a1E363e510217C7112','0xBdDBd0DffcBD54c8dfF0B5694cad8986C922969','0xA27AA0E66C21Ab6b68E832E2d1Bd1D8620818FD','0x468C1bAfc5114C99Bca5C12Dcfb48D1Ee6De9C1A','0x2b036A1A5A65aB99bfc3b6C1c0F4E9c12FaE899','0xD11071888B94E8AB6eA2314D37fE0910a2493e00','0x67Cb5d79e84c1A70b6ed5f5D67e69b615D3d92C','0xCB2528F7cA156e39A281bAF14D875C3d973352cD','0x2a28e243FcB4Ea076588089329aa8B24c638d81','0x27c705589A57E109aDeb738D7446Ac26f54E11a5','0x01405A2B567635dbe6F673ef58322a3CFec4402','0x1000ac8D491985734688a99Da2599C333599FAE2','0x76798549243CF31a24895a75A2827859414B0B8','0xcc1cAA3252eb24Ca1F3d1fA3a037f6CD42D662A','0x83a1f862f0b23a6A8bEaAEc6a92b201102B4F9ab',' 0x1aE0111b44Cc9dB31956533bd7da6dA8003D60d','0x1aE0111b44Cc9dB31956533bd7da6dAE8003D60d','0x49Eb7671bF8898FF3c75E51dBCeae07443227AB','0xC6a2361cD991dd31e69c92Da7ebf322bb0cE4a2f','0x61a3245948506be577b7d1bfd662b300be0dc8f','0xe0a6F0AD4036427d1F5eb1504d79D7d087354197','0x7676E92cE3485974C5fA770a6Aa47cD461463E7','0x7D41abfD292a51b5aD1D346B592128f94d17fCBC','0x92ACF17BF6E675736e8eF05a55B99519cc922F7','0x6546939a76a86d761D945354D225780F61CF5E29','0xF535eA02BDc46D4fB933AC48306CA8a1FC7073f','0x42d6629c599d47b955db7a8764b17d42d1dddcb','0x0EAC1BE5c2Bf16B9aE3DAd30F7815C466dB6Af8f','0xfbF026F5991b379577AE7c07eF8ce92AC564d30','0xa53E0f2a5AaD1e6600E4D678B641A79CBC6e8863','0xe7D8b70fce45aa791b7755C6EA4943b5acDd22c','0x3E860904CAcdd5442AbfD82C2Eaf3548Aeeb8A13','0x57d5b384D776c49bB22627b327cA782252672E7','0xde9C0a3947C6B8034f8D339D546a4c96C83d028e','0x6be504ca1913733953194ef999029ace1a49E06','0x9450585189fA40e0cE0D8F18922afF6FB8d1B698','0x8E9DFDDa22EaDbBA7E1e243385f4cFE4Db9c0b7','0x96cf8D095C6366780f44BC08e82c6368b93F3355','xA202AD0c98309882B838290e6ad156Bb51D7B7e9','0x01923f1AD323d0e2B87b461125935469a70427F','0x9383C01934a9D24edDebeF4350ea919f3093Fe81','0xf7054231cB6c2b266E10BA65cf805b0b5B92d82','0xFBd91945Bc37e9Cf41E504A20F40B5963E1C07d1','0x7e1659ebbdf7bf29930f596626c194cab7d1f83','0xc35D8eac9b63CB96E97fBCf9a3DA97Ca38518E77','0x4bcecc562b2887463409894298da42194d60758','0x2973940325da2E092a03c5e2C1D88E8f00ceEA97','0xaa969c700e165c8a48a932ebb74e5ce527fa382','0x88236B97582B73898190Af4d5C6AA3f0AbE0D62d','0x6D45fc8f241a325c9F44513DBd73a1e1C896Ad4','0xBA104910a51ebf027e0fa402F420A2D02F089c43','0xCb01CDA6fE56F2a51778e86B882CcF5Ef78b031','0xb74BaA6b6a772121aBF9683d16080d503C93361','0x2FfA1bA65C24CC4aEDCb7bD7F9Bd4561aDe4e5Ed','0xDA304a24f9EeeAceEf854c232B1fC779919DD04','0xF42aD66F4b66628584f2E97421A008d62A8f116c','0x7df953D6BE5Fd9532a7E829cDF72d2A9AB27000','0xB5106250202Cc53eed500ce06ceCc8984319d5bB','0xD116681971aa2245ED7c79770Ec72249cf904f2','0x21ef5E9d3bD810D22193E406FF31Ff486621447F','0xCF546F25249715aff0AdFB96904db3775234134','0x5aB52d1673aBdca08C826d6bFd52CD1d1F4C2c90','0x92706Fc51201d4C0EbddA8df7d9954c8A093Fe8','0x9eecBB1ff509f297325cB292F3340342D4383F5e','0xCfBC6A76a4b462911787529F144561CBCde165a','0xc61CC53572f07062731b21685F07fb1d71495fC','0xC00178B222A2137bF19900E3069F9aF2b90d3265','0x9Bf0a6caD60daaD36Bfea079187F4BE67973574','0x89e4DdC8fFceAf8Cc83e05407e5b2102Fca96Ced','0xE40de2b86813F454E937c7f84453A15b0B88B65','0xcE148372369B5B75aa47709Bec0B59C8215e0935','0xf6794De888d9671F6269baCFbB9771bb5B2Ce22','0x8f86C1a39Ada0833069f7cC271b0eBb429D09700','0xa73aC33E9eb19e735f6233Ac348c429b1E0Dd9e','0xAb40f530223C063242eE80F2FB1D0a74A5919','0x5C7A822744fDc608a5257Bf5bEB249E7cbFF6C9','0xC06F0c794A0265071618DD9d461dE3351f2b98aa','0x50E519e289f76097B04F9921D1BFB5231d5a4a8','0xB217f1D7093b021B7dE9dd603D498CE3A16e293C','x68aFBc341ed614E804b93e80c679C569Ee97432F','0x78529a5325a7CbFe0208A6fE99A829EA28b9946','0x1C71d26056FF31899E9902c91Ffd5Df3e7785CF8','0xD80E1D7d80a15046b04Bd8D6dfe88230e6D0c6c','0xDC0484a5727B0598003129Fbd2d0891A243D68a0','0x21982C6f1bcC45bc01Df877694227aAd3F44258','0xD7d9e248C78c3822E2aD77b76BE25A45C11d2A03','0x67b981b23340DF1ABFAA2F3d1db90F0F9C5c924','0x1E16f946Cd430467425869014Ae25f85413003c4','0x06279b272258344B8B0246DC112Df6d9fd14f08','0xBe3F0f199156DC1fA2Ac4F17D5752809315841F5','0x8dc243fdE4A786dd10d5E01C48560cEeE283A75','0x661cad15D35C64b4394381BAc14CA142B150738','0xdc6f58fab8913fa96b5a1c2c53400a6030b93d6d','0xf99b8874214EC22040BA5D260f105F88870Cf86','0xeF4AeBA3Bc7Ea0b08F43B9468dcd546cA1321a79','0x3d5145C527E7e7e6d4e97c60b2e6e75ec792a50','0x435fcD37f72eF03dc5617d1090A6e7EA215726BF','0x145109949f6A5E9068714AA8376a862E6E26bfE','0x7cC5E2bffbD7cfaF1FB68Cd7ccbCB74Ab2C35559','0xAB3216fAA08675689F4667F98Ebe747623EEFF6','0x3aa3c3dc3ab770927aa860441d63d7dbe8e2f804','0x340dBFf051837387Dd7e3468B30bAAA3B0e8d54','0x25dDe5917A0588d2b8E821a66F196fB0719B047','0x2F36671Fba3A42A392AF26556895C26D8cEdb0E5','0xbA09a4e37C52aFC1F3D77f563DCc71Da6DaaF0e','0xE2516BDaf6997D9110B09a56a06855bBBA49cfc5','0x3c96A826d4A33bb9930f3E941c43FD1876dCF1F','0x9499dc3402f38694C2Daa30D4ade7e578425FDc2','0x819FFdcDfA53f8d7996B6382543949333604D8a','0x7521dfCD2cC044D91d8D5C6c6a2495083D0a8249','0xb5dD9A630AF578Ff1183c1E1B6aD6A5f51F0023','0x9AC382F25178E594Aef547661C0ba1f48Ea5569D','0xF00f256173E1e3270d72f492eF14F60Dc3746DB','0x4337f74E2CB296A768D6fc8b37Ed56E3F97a611e','0927b6D4D3D8B0eBe9bBf04181F563c547B6B579f','0xA268fbE8e0e385BC97b2fb91a4fc8E346f1c92D','0xf3accb7910a4ab3b3dea05cc82b8dbe2b06e9c4b']
   
   // total number to be randomed
    const selectedAddrNumber = 50
    // selected addresses
    const result = [];

    // ETH block height 12132888 hash (haven't mined)
    const ethHash = '0x9e4c6ebe8275cefabc7287ff10590d22ca3f73766ae20a448e2979f5acb64c2a';

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
