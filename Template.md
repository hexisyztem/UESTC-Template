<!-- <div align=center>
<img src="th1.jpeg" width="120%" height="120%">
</div>

<div align=center>
<font size=10>UESTC-hexisyztem</font>
</div>

<div STYLE="page-break-after: always;">
</div> -->

> UESTC_Default ---- hexisyztem
> 未测试版本

- [字符串部分](#%e5%ad%97%e7%ac%a6%e4%b8%b2%e9%83%a8%e5%88%86)
  - [KMP](#kmp)
  - [ExKMP ( $Z$ 函数 )](#exkmp--z-%e5%87%bd%e6%95%b0)
    - [$s$ 字符串关于 $s$ 字符串的 $Z$ 函数](#s-%e5%ad%97%e7%ac%a6%e4%b8%b2%e5%85%b3%e4%ba%8e-s-%e5%ad%97%e7%ac%a6%e4%b8%b2%e7%9a%84-z-%e5%87%bd%e6%95%b0)
    - [$t$ 字符串关于 $s$ 字符串的 $Z$ 函数 (待更新)](#t-%e5%ad%97%e7%ac%a6%e4%b8%b2%e5%85%b3%e4%ba%8e-s-%e5%ad%97%e7%ac%a6%e4%b8%b2%e7%9a%84-z-%e5%87%bd%e6%95%b0-%e5%be%85%e6%9b%b4%e6%96%b0)
  - [回文自动机](#%e5%9b%9e%e6%96%87%e8%87%aa%e5%8a%a8%e6%9c%ba)
  - [AC自动机](#ac%e8%87%aa%e5%8a%a8%e6%9c%ba)
  - [Manacher](#manacher)
  - [最小表示 (待更新)](#%e6%9c%80%e5%b0%8f%e8%a1%a8%e7%a4%ba-%e5%be%85%e6%9b%b4%e6%96%b0)
- [数学部分](#%e6%95%b0%e5%ad%a6%e9%83%a8%e5%88%86)
  - [BSGS 大步-小步](#bsgs-%e5%a4%a7%e6%ad%a5-%e5%b0%8f%e6%ad%a5)
  - [MillerRabbin 素数测定](#millerrabbin-%e7%b4%a0%e6%95%b0%e6%b5%8b%e5%ae%9a)
  - [Pollard-Rho算法 (大整数质因子分解)](#pollard-rho%e7%ae%97%e6%b3%95-%e5%a4%a7%e6%95%b4%e6%95%b0%e8%b4%a8%e5%9b%a0%e5%ad%90%e5%88%86%e8%a7%a3)
  - [矩阵相关](#%e7%9f%a9%e9%98%b5%e7%9b%b8%e5%85%b3)
    - [矩阵的逆](#%e7%9f%a9%e9%98%b5%e7%9a%84%e9%80%86)
    - [Gauss 消元](#gauss-%e6%b6%88%e5%85%83)
  - [循环矩阵](#%e5%be%aa%e7%8e%af%e7%9f%a9%e9%98%b5)
    - [快速求解循环矩阵乘积](#%e5%bf%ab%e9%80%9f%e6%b1%82%e8%a7%a3%e5%be%aa%e7%8e%af%e7%9f%a9%e9%98%b5%e4%b9%98%e7%a7%af)
  - [扩展欧拉定理](#%e6%89%a9%e5%b1%95%e6%ac%a7%e6%8b%89%e5%ae%9a%e7%90%86)
  - [类欧几里德算法](#%e7%b1%bb%e6%ac%a7%e5%87%a0%e9%87%8c%e5%be%b7%e7%ae%97%e6%b3%95)
  - [线性基](#%e7%ba%bf%e6%80%a7%e5%9f%ba)
    - [线性基求交](#%e7%ba%bf%e6%80%a7%e5%9f%ba%e6%b1%82%e4%ba%a4)
    - [线性基求并](#%e7%ba%bf%e6%80%a7%e5%9f%ba%e6%b1%82%e5%b9%b6)
    - [区间线性基](#%e5%8c%ba%e9%97%b4%e7%ba%bf%e6%80%a7%e5%9f%ba)
  - [数论函数](#%e6%95%b0%e8%ae%ba%e5%87%bd%e6%95%b0)
    - [数论分块](#%e6%95%b0%e8%ae%ba%e5%88%86%e5%9d%97)
    - [积性函数](#%e7%a7%af%e6%80%a7%e5%87%bd%e6%95%b0)
      - [常见的积性函数](#%e5%b8%b8%e8%a7%81%e7%9a%84%e7%a7%af%e6%80%a7%e5%87%bd%e6%95%b0)
    - [狄利克雷卷积 ($Dirichlet$ 卷积)](#%e7%8b%84%e5%88%a9%e5%85%8b%e9%9b%b7%e5%8d%b7%e7%a7%af-dirichlet-%e5%8d%b7%e7%a7%af)
      - [例子](#%e4%be%8b%e5%ad%90)
    - [$Fibonacci$ 函数相关结论](#fibonacci-%e5%87%bd%e6%95%b0%e7%9b%b8%e5%85%b3%e7%bb%93%e8%ae%ba)
  - [数论相关简单结论](#%e6%95%b0%e8%ae%ba%e7%9b%b8%e5%85%b3%e7%ae%80%e5%8d%95%e7%bb%93%e8%ae%ba)
    - [筛法](#%e7%ad%9b%e6%b3%95)
    - [容斥](#%e5%ae%b9%e6%96%a5)
  - [多项式算法(待更新)](#%e5%a4%9a%e9%a1%b9%e5%bc%8f%e7%ae%97%e6%b3%95%e5%be%85%e6%9b%b4%e6%96%b0)
    - [FFT(待更新)](#fft%e5%be%85%e6%9b%b4%e6%96%b0)
    - [分治FFT(待更新)](#%e5%88%86%e6%b2%bbfft%e5%be%85%e6%9b%b4%e6%96%b0)
    - [FWT(待更新)](#fwt%e5%be%85%e6%9b%b4%e6%96%b0)
    - [NTT(待更新)](#ntt%e5%be%85%e6%9b%b4%e6%96%b0)
    - [多项式求逆(待更新)](#%e5%a4%9a%e9%a1%b9%e5%bc%8f%e6%b1%82%e9%80%86%e5%be%85%e6%9b%b4%e6%96%b0)
  - [线性规划(待更新)](#%e7%ba%bf%e6%80%a7%e8%a7%84%e5%88%92%e5%be%85%e6%9b%b4%e6%96%b0)
    - [单纯形(待更新)](#%e5%8d%95%e7%ba%af%e5%bd%a2%e5%be%85%e6%9b%b4%e6%96%b0)
    - [KKT(待更新)](#kkt%e5%be%85%e6%9b%b4%e6%96%b0)
    - [拉格朗日乘子法(待更新)](#%e6%8b%89%e6%a0%bc%e6%9c%97%e6%97%a5%e4%b9%98%e5%ad%90%e6%b3%95%e5%be%85%e6%9b%b4%e6%96%b0)
  - [常见积分表(待更新)](#%e5%b8%b8%e8%a7%81%e7%a7%af%e5%88%86%e8%a1%a8%e5%be%85%e6%9b%b4%e6%96%b0)
  - [常见生成函数(待更新)](#%e5%b8%b8%e8%a7%81%e7%94%9f%e6%88%90%e5%87%bd%e6%95%b0%e5%be%85%e6%9b%b4%e6%96%b0)
  - [BM 线性递推](#bm-%e7%ba%bf%e6%80%a7%e9%80%92%e6%8e%a8)
  - [Lucas 定理](#lucas-%e5%ae%9a%e7%90%86)
    - [扩展 Lucas 定理](#%e6%89%a9%e5%b1%95-lucas-%e5%ae%9a%e7%90%86)
  - [中国剩余定理 (待更新)](#%e4%b8%ad%e5%9b%bd%e5%89%a9%e4%bd%99%e5%ae%9a%e7%90%86-%e5%be%85%e6%9b%b4%e6%96%b0)
  - [置换群计数问题](#%e7%bd%ae%e6%8d%a2%e7%be%a4%e8%ae%a1%e6%95%b0%e9%97%ae%e9%a2%98)
    - [Burnside 引理](#burnside-%e5%bc%95%e7%90%86)
    - [Polya 定理](#polya-%e5%ae%9a%e7%90%86)
    - [min-max反演](#min-max%e5%8f%8d%e6%bc%94)
- [动态规划](#%e5%8a%a8%e6%80%81%e8%a7%84%e5%88%92)
  - [树上依赖背包(待更新)](#%e6%a0%91%e4%b8%8a%e4%be%9d%e8%b5%96%e8%83%8c%e5%8c%85%e5%be%85%e6%9b%b4%e6%96%b0)
  - [可逆背包(待更新)](#%e5%8f%af%e9%80%86%e8%83%8c%e5%8c%85%e5%be%85%e6%9b%b4%e6%96%b0)
  - [SOSdp](#sosdp)
  - [wqs二分](#wqs%e4%ba%8c%e5%88%86)
- [图论](#%e5%9b%be%e8%ae%ba)
  - [斯坦纳树](#%e6%96%af%e5%9d%a6%e7%ba%b3%e6%a0%91)
  - [虚树](#%e8%99%9a%e6%a0%91)
  - [树哈希](#%e6%a0%91%e5%93%88%e5%b8%8c)
  - [支配树(待更新)](#%e6%94%af%e9%85%8d%e6%a0%91%e5%be%85%e6%9b%b4%e6%96%b0)
  - [prufer 序列 (待更新)](#prufer-%e5%ba%8f%e5%88%97-%e5%be%85%e6%9b%b4%e6%96%b0)
  - [LGV 引理 (待更新)](#lgv-%e5%bc%95%e7%90%86-%e5%be%85%e6%9b%b4%e6%96%b0)
  - [二分图匹配问题](#%e4%ba%8c%e5%88%86%e5%9b%be%e5%8c%b9%e9%85%8d%e9%97%ae%e9%a2%98)
    - [最长反链(待更新)](#%e6%9c%80%e9%95%bf%e5%8f%8d%e9%93%be%e5%be%85%e6%9b%b4%e6%96%b0)
    - [霍尔定理](#%e9%9c%8d%e5%b0%94%e5%ae%9a%e7%90%86)
    - [最小点覆盖方案构造](#%e6%9c%80%e5%b0%8f%e7%82%b9%e8%a6%86%e7%9b%96%e6%96%b9%e6%a1%88%e6%9e%84%e9%80%a0)
    - [HopcroftKarp算法(二分图匹配)](#hopcroftkarp%e7%ae%97%e6%b3%95%e4%ba%8c%e5%88%86%e5%9b%be%e5%8c%b9%e9%85%8d)
- [数据结构](#%e6%95%b0%e6%8d%ae%e7%bb%93%e6%9e%84)
  - [双栈模拟 (待更新)](#%e5%8f%8c%e6%a0%88%e6%a8%a1%e6%8b%9f-%e5%be%85%e6%9b%b4%e6%96%b0)
  - [长链剖分(待更新)](#%e9%95%bf%e9%93%be%e5%89%96%e5%88%86%e5%be%85%e6%9b%b4%e6%96%b0)
    - [求距离为k的儿子个数(入点的时候减去，离开的时候加)](#%e6%b1%82%e8%b7%9d%e7%a6%bb%e4%b8%bak%e7%9a%84%e5%84%bf%e5%ad%90%e4%b8%aa%e6%95%b0%e5%85%a5%e7%82%b9%e7%9a%84%e6%97%b6%e5%80%99%e5%87%8f%e5%8e%bb%e7%a6%bb%e5%bc%80%e7%9a%84%e6%97%b6%e5%80%99%e5%8a%a0)
  - [可持久化数据结构](#%e5%8f%af%e6%8c%81%e4%b9%85%e5%8c%96%e6%95%b0%e6%8d%ae%e7%bb%93%e6%9e%84)
  - [区间LCM](#%e5%8c%ba%e9%97%b4lcm)
- [几何](#%e5%87%a0%e4%bd%95)
- [杂项](#%e6%9d%82%e9%a1%b9)
    - [long long范围内任意模数乘法(利用自然溢出)](#long-long%e8%8c%83%e5%9b%b4%e5%86%85%e4%bb%bb%e6%84%8f%e6%a8%a1%e6%95%b0%e4%b9%98%e6%b3%95%e5%88%a9%e7%94%a8%e8%87%aa%e7%84%b6%e6%ba%a2%e5%87%ba)
    - [状态压缩下的子集枚举](#%e7%8a%b6%e6%80%81%e5%8e%8b%e7%bc%a9%e4%b8%8b%e7%9a%84%e5%ad%90%e9%9b%86%e6%9e%9a%e4%b8%be)
    - [高维前缀和(子集求和)](#%e9%ab%98%e7%bb%b4%e5%89%8d%e7%bc%80%e5%92%8c%e5%ad%90%e9%9b%86%e6%b1%82%e5%92%8c)
    - [不平衡分块](#%e4%b8%8d%e5%b9%b3%e8%a1%a1%e5%88%86%e5%9d%97)
    - [股票问题](#%e8%82%a1%e7%a5%a8%e9%97%ae%e9%a2%98)
    - [思维是否各维度可以独立](#%e6%80%9d%e7%bb%b4%e6%98%af%e5%90%a6%e5%90%84%e7%bb%b4%e5%ba%a6%e5%8f%af%e4%bb%a5%e7%8b%ac%e7%ab%8b)
    - [位运算问题](#%e4%bd%8d%e8%bf%90%e7%ae%97%e9%97%ae%e9%a2%98)
    - [极大区间统计(问区间内有多少个子段)](#%e6%9e%81%e5%a4%a7%e5%8c%ba%e9%97%b4%e7%bb%9f%e8%ae%a1%e9%97%ae%e5%8c%ba%e9%97%b4%e5%86%85%e6%9c%89%e5%a4%9a%e5%b0%91%e4%b8%aa%e5%ad%90%e6%ae%b5)
    - [找规律](#%e6%89%be%e8%a7%84%e5%be%8b)
    - [求N(1<=1e18)项数列的值](#%e6%b1%82n11e18%e9%a1%b9%e6%95%b0%e5%88%97%e7%9a%84%e5%80%bc)

# 字符串部分

## KMP

参数：  
*f &nbsp; : &nbsp; 失配数组 ---- f[i + 1] = p + 1 表示 [0 ~ p] 是 [0 ~ i] 的最长后缀  
*P &nbsp; : &nbsp; 模板串(从下标 $0$ 开始)
*T &nbsp; : &nbsp; 待匹配串(从下标 $0$ 开始)

``` C++
void find(char T[], char P[], int f[]){
    int n = strlen(T), m = strlen(P);
    getfail(P, f);
    int j = 0;
    for(int i = 0; i < n; i ++){
        while(j && P[j] != T[i]) j = f[j];
        if(P[j] == T[i]) j ++;
        // if(j == m) printf("%d\n",i-m+1);
    }
}

void getfail(char P[], int f[]){
    int m = strlen(P);
    f[0] = 0; f[1] = 0;
    for(int i = 1; i < m; i ++){
        int j = f[i];
        while(j && P[i] != P[j]) j = f[j];
        f[i+1] = (P[i] == P[j]) ? j+1 : 0;
    }
}
```

## ExKMP ( $Z$ 函数 )

### $s$ 字符串关于 $s$ 字符串的 $Z$ 函数
参数：  
*s &nbsp; : &nbsp; 模板串(从下标 $0$ 开始)  
*z &nbsp; : &nbsp; $Z$ 函数，$Z_i$表示以 $i$ 号下标作为开头的子串，与 $s$ 串所能匹配的最长长度  

``` C++
void z_function(char *s, int *z) {
  int n = strlen(s);
  for (int i = 1, l = 0, r = 0; i < n; ++i) {
    if (i <= r) z[i] = min(r - i + 1, z[i - l]);
    while (i + z[i] < n && s[z[i]] == s[i + z[i]]) ++z[i];
    if (i + z[i] - 1 > r) l = i, r = i + z[i] - 1;
  }
  return ;
}
```

### $t$ 字符串关于 $s$ 字符串的 $Z$ 函数 (待更新)

## 回文自动机

参数:  
**nex &nbsp; : &nbsp; Trie树  
*fail &nbsp; : &nbsp; fail失配后缀链接  
*cnt[maxn] &nbsp; : &nbsp; 此回文串出现个数  
*num &nbsp; : &nbsp; fail树的深度  
*len : &nbsp; 回文串长度  
*s &nbsp; : &nbsp; 存放添加的字符  
last &nbsp; : &nbsp; 指向上一个字符所在的节点，方便下一次add  
n &nbsp; : &nbsp; 已添加字符个数  
tot &nbsp; : &nbsp; 节点个数  

``` C++
const int maxn = 100005;// n(空间复杂度o(n*ALP)),实际开n即可
const int ALP = 26; //字符集大小
 
struct PAM{ // 每个节点代表一个回文串
    int nex[maxn][ALP]; // nex指针,参照Trie树
    int fail[maxn]; // fail失配后缀链接
    int cnt[maxn]; // 此回文串出现个数
    int num[maxn]; // fail树的深度
    int len[maxn]; // 回文串长度
    int s[maxn]; // 存放添加的字符
    int last; //指向上一个字符所在的节点，方便下一次add
    int n; // 已添加字符个数
    int tot; // 节点个数
 
    int newnode(int w){ // 初始化节点，w=长度
        for(int i=0;i < ALP;i++)
            nex[tot][i] = 0;
        cnt[tot] = 0;
        num[tot] = 0;
        len[tot] = w;
        return tot ++;
    }
    
    void init(){
        tot = 0;
        newnode(0);
        newnode(-1);
        last = 0;
        n = 0;
        s[n] = -1; // 开头放一个字符集中没有的字符，减少特判
        fail[0] = 1;
    }
    int get_fail(int x){ // 和KMP一样，失配后找一个尽量最长的
        while(s[n-len[x]-1] != s[n]) x = fail[x];
        return x;
    }
    void add(int c){
        c -= 'a'; // 字符集去冗
        s[++ n] = c;
        int cur = get_fail(last);
        if(!nex[cur][c]){
            int now = newnode(len[cur]+2);
            fail[now] = nex[get_fail(fail[cur])][c];
            nex[cur][c] = now;
            num[now] = num[fail[now]] + 1;
        }
        last = nex[cur][c];
        cnt[last]++;
    }
    void count(){
        // 最后统计一遍每个节点出现个数
        // 父亲累加儿子的cnt,类似SAM中parent树
        // 满足parent拓扑关系
        for(int i= tot - 1; i >= 0; i --)
            cnt[fail[i]] += cnt[i];
    }
}pam;
```


## AC自动机

参数:
*tr &nbsp; : &nbsp; Trie树
*fail &nbsp; : &nbsp; 失配数组 --- fail[u] 所表示的字符串是 u 字符串的最长后缀
*t &nbsp; : &nbsp; 待查询的字符串

``` C++
void build() {
  for (int i = 0; i < 26; i++)
    if (tr[0][i]) 
      q.push(tr[0][i]);
  while (q.size()) {
    int u = q.front(); q.pop();
    for (int i = 0; i < 26; i++) {
      if (tr[u][i])
        fail[tr[u][i]] = tr[fail[u]][i], q.push(tr[u][i]);
      else
        tr[u][i] = tr[fail[u]][i];
    }
  }
}

int query(char *t) {
  int u = 0, res = 0;
  for (int i = 1; t[i]; i++) {
    u = tr[u][t[i] - 'a'];  // 转移
    for (int j = u; j && e[j] != -1; j = fail[j]) {
      res += e[j], e[j] = -1;
    }
  }
  return res;
}
```

## Manacher
参数:
*s &nbsp; : &nbsp; 输入字符串
*s_new &nbsp; : &nbsp; 对输入字符串插入空字符
*p &nbsp; : &nbsp; $p_i-1$ 表示在 $i$ 为中心的最长回文串长度

``` C++
struct Manacher{
    int len, tlen;
    int p[maxn*2]; // p[i] - 1 表示回文串长度
    int s_new[maxn*2];
    char s[maxn];
    const int ALP = 1024;
    void init()// 取得新字符串长度并完成向 s_new 的转换
    {
        len = strlen(s);
        s_new[0] = -ALP;
        s_new[1] = -1;
        tlen = 2;
        for (int i = 0; i < len; i++)
        {
            s_new[tlen ++] = s[i];
            s_new[tlen ++] = -1;
        }
        s_new[tlen] = -2;  // s_new[tlen] != s_new[0] != s_new[i] (0 < i < tlen)
        return ;  // 返回 s_new 的长度
    }
    void deal()
    {
        int max_len = -1;  // 最长回文长度
        int id, mx = 0;
        for (int i = 1; i < tlen; i++)
        {
            if (i < mx)
                p[i] = min(p[2 * id - i], mx - i);  // 需搞清楚上面那张图含义, mx 和 2*id-i 的含义
            else
                p[i] = 1;
            while (s_new[i - p[i]] == s_new[i + p[i]])  // 不需边界判断，因为左有'$',右有'\0'
                p[i]++;
            // 我们每走一步 i，都要和 mx 比较，我们希望 mx 尽可能的远，这样才能更有机会执行 if (i < mx)这句代码，从而提高效率
            if (mx < i + p[i])
            {
                id = i;
                mx = i + p[i];
            }
        }
        return ;
    }
    void prin(int posi){ // 对标新的字符串数组的下标,打印以该虚拟位置为中心的回文串
        if(!posi) return;
        int start_ = (posi - 1) / 2 - (p[posi] - 1) / 2;
        for(int i = 1; i < p[posi]; i ++)
            printf("%c", s[start_ ++]);
        return ;
    }
}Mana;
```

## 最小表示 (待更新)



# 数学部分

## BSGS 大步-小步
注意可以不平衡分块，考虑多组询问的情况下。

## MillerRabbin 素数测定

每次测定正确率为 $75\%$，在进行 $TestTime$ 次测定后，错误率将降到 $0.25 ^ {TestTime}$

参数:
n &nbsp; : &nbsp; 待测定的整数

``` C++
bool millerRabbin(int n) {
  if (n < 3) return n == 2;
  int a = n - 1, b = 0;
  while (a % 2 == 0) a /= 2, ++b;
  // test_time 为测试次数,建议设为不小于 8
  // 的整数以保证正确率,但也不宜过大,否则会影响效率
  for (int i = 1, j; i <= test_time; ++i) {
    int x = rand() % (n - 2) + 2, v = quickPow(x, a, n);
    if (v == 1 || v == n - 1) continue;
    for (j = 0; j < b; ++j) {
      v = (long long)v * v % n;
      if (v == n - 1) break;
    }
    if (j >= b) return 0;
  }
  return 1;
}
```

## Pollard-Rho算法 (大整数质因子分解)
参数: 
*f &nbsp; : &nbsp; 分解后的素因子
c &nbsp; : &nbsp; 随机数
``` C++
const int MAXN = 65;
long long x[MAXN];
vector<long long> f;

long long multi(long long a, long long b, long long p) {
    long long ans = 0;
    while(b) {
        if(b&1LL) ans = (ans+a)%p;
        a = (a+a)%p;
        b >>= 1;
    }
    return ans;
}

long long qpow(long long a, long long b, long long p) {
    long long ans = 1;
    while(b) {
        if(b&1LL) ans = multi(ans, a, p);
        a = multi(a, a, p);
        b >>= 1;
    }
    return ans;
}

bool Miller_Rabin(long long n) {
    if(n == 2) return true;
    int s = 20, i, t = 0;
    long long u = n-1;
    while(!(u & 1)) {
        t++;
        u >>= 1;
    }
    while(s--) {
        long long a = rand()%(n-2)+2;
        x[0] = qpow(a, u, n);
        for(i = 1; i <= t; i++) {
            x[i] = multi(x[i-1], x[i-1], n);
            if(x[i] == 1 && x[i-1] != 1 && x[i-1] != n-1) return false;
        }
        if(x[t] != 1) return false;
    }
    return true;
}

long long gcd(long long a, long long b) {
    return b ? gcd(b, a%b) : a;
}

long long Pollard_Rho(long long n, int c) {
    long long i = 1, k = 2, x = rand()%(n-1)+1, y = x;
    while(true) {
        i++;
        x = (multi(x, x, n) + c)%n;
        long long p = gcd((y-x+n)%n, n);
        if(p != 1 && p != n) return p;
        if(y == x) return n;
        if(i == k) {
            y = x;
            k <<= 1;
        }
    }
}

void find(long long n, int c) {
    if(n == 1) return;
    if(Miller_Rabin(n)) {
        f.push_back(n);
        return;
    }
    long long p = n, k = c;
    while(p >= n) p = Pollard_Rho(p, c--);
    find(p, k);
    find(n/p, k);
}
```

## 矩阵相关	
### 矩阵的逆	
> *f &nbsp; : &nbsp; 输入矩阵	
> *g &nbsp; : &nbsp; 输出矩阵，f 矩阵的逆矩阵	
``` C++	
void inverse(){	
    double temp;	
    memset(g, 0, sizeof(g));	
    for(int i = 0;i < n; i++) g[i][i] = 1.0;	
    for(int i = 0;i < n; i++){	
        for(int j = i;j < n; j++){	
            if(fabs(f[j][i]) > eps){	
                for(int k = 0;k < n; k++){	
                    swap(f[i][k],f[j][k]);	
                    swap(g[i][k],g[j][k]);	
                }	
                break;	
            }	
        }	
        temp = f[i][i];	
        for(int k = 0;k < n; k++)	
        {	
            f[i][k] /= temp;	
            g[i][k] /= temp;	
        }	
        for(int j = 0;j < n; j++)	
        {	
            if(j != i && fabs(f[j][i]) > eps)	
            {	
                temp = f[j][i];	
                for(int k = 0;k < n; k++){	
                    g[j][k] -= g[i][k] * temp;	
                    f[j][k] -= f[i][k] * temp;	
                }	
            }	
        }	
    }	
}	
```	

### Gauss 消元	
``` C++	
double a[maxn][maxn],ans[maxn];	
bool l[maxn];	
// 输入矩阵大小，返回解空间维数，维数为0表示解唯一	
// l[i]为true表示该数解唯一	
int Gauss(int n) {	
    int i,j,k,res = 0,r = 0;	
    for(i = 0;i < n; i++) l[i] = false;	
    for(i = 0;i < n; i++) {	
        for(j = r;j < n; j++) {	
            if(fabs(a[j][i]) > eps) {	
                for(k = i;k <= n; k++) swap(a[j][k],a[r][k]);	
                break;	
            }	
        }	
        if(fabs(a[r][i]) < eps) {	
            res++;	
            continue;	
        }	
        for(j = 0;j < n; j++) {	
            if(j != r && fabs(a[j][i] / a[r][i]) > eps) {	
                double tmp = a[j][i] / a[r][i];	
                for(k = i;k <= n; k++) a[j][k] -= tmp * a[r][k];	
            }	
        }	
        l[i] = true;	
        r++;	
    }	
    for(i = 0;i < n; i++) {	
        if(l[i]) {	
            for(j = 0;j < n; j++) {	
                if(fabs(a[j][i]) > 0) ans[i] = a[j][n] / a[j][i];	
            }	
        }	
    }	
    return res;	
}	
```	

## 循环矩阵	
定义:第i行的向量为第i−1行的向量的各元素依次右移一位得到的结果	
例如：	
$$	
\begin{aligned}	
a_0 & & a_1 & & a_2 \\	
a_2 & & a_0 & & a_1 \\	
a_1 & & a_2 & & a_0 \\	
\end{aligned} 	
$$	
性质:两个循环矩阵的乘积仍是循环矩阵

### 快速求解循环矩阵乘积	
设有 $n*n$ 的循环矩阵 $A,B$，求 $A*B=C$	
定义 $f(x)= \sum_{i=0}^{n−1} a_i * x^i, g(x)= \sum_{i=0}^{n−1} b_i * x^i$	
其中 $a_i, b_i$ 分别为矩阵 $A,B$ 第一行的元素	
设 $h(x)=f(x)*g(x)= \sum_{i=0}^{n-1}c_i * x_i, c_i = \sum_{(j+k)\%n=i}a_j*b_k$(即循环卷积)	
则 $h(x)$ 的系数即为矩阵 $C$ 的第一行的元素	
故求 $A^m$ 即为求 $f(x)^m$,多项式快速幂即可	
对于长度为 $2$ 的幂的多项式的 $m$ 次循环卷积,可以直接以当前长度作为 $fft$ 长度,不需要满足2倍关系	

## 扩展欧拉定理
计算 $a^b \;mod \; p$，当 $b$ 很大时，可以通过广义欧拉定理降幂:


$$
a^b \; mod \; p \equiv \left\{
\begin{array}{rcl}
a^{b \; mod \; \phi(p)}  \; mod \; p, &  & gcd(a, p) = 1 \\
a^b \; mod \; p ,                     &  & gcd(a, p) \not= {1}, b < \phi(p)\\
a^{b \; mod \; \phi(p) + \phi(p)}  \; mod \; p, &  & gcd(a, p) \not= {1}, b \geq \phi(p)\\ 
\end{array} \right.
$$

也可以

$$
a^b \; mod \; p \equiv \left\{
\begin{array}{rcl}
a^b \; mod \; p ,                     &  & b < \phi(p)\\
a^{b \; mod \; \phi(p) + \phi(p)}  \; mod \; p, &  & b \geq \phi(p)\\ 
\end{array} \right.
$$

## 类欧几里德算法
用于求解以下几个问题：
$$
f(n, a, b, c) = \sum_{i=0}^{n} \lfloor \frac{a*i+b}{c} \rfloor \\

g(n, a, b, c) = \sum_{i=0}^{n} i * \lfloor \frac{a*i+b}{c} \rfloor \\

h(n, a, b, c) = \sum_{i=0}^{n} {(\lfloor \frac{a*i+b}{c} \rfloor)} ^ 2
$$

``` C++
const int P = 998244353;
int i2 = 499122177, i6 = 166374059; 
// i2 表示 2 在模 P 意义下的逆元，i6 表示 6 在模 P 意义下的逆元
struct data {
  data() { f = g = h = 0; }
  int f, g, h;
};  // 三个函数打包
data calc(int n, int a, int b, int c) {
  int ac = a / c, bc = b / c, m = (a * n + b) / c, n1 = n + 1, n21 = n * 2 + 1;
  data d;
  if (a == 0)  // 迭代到最底层
  {
    d.f = bc * n1 % P;
    d.g = bc * n % P * n1 % P * i2 % P;
    d.h = bc * bc % P * n1 % P;
    return d;
  }
  if (a >= c || b >= c)  // 取模
  {
    d.f = n * n1 % P * i2 % P * ac % P + bc * n1 % P;
    d.g = ac * n % P * n1 % P * n21 % P * i6 % P + bc * n % P * n1 % P * i2 % P;
    d.h = ac * ac % P * n % P * n1 % P * n21 % P * i6 % P +
          bc * bc % P * n1 % P + ac * bc % P * n % P * n1 % P;
    d.f %= P, d.g %= P, d.h %= P;

    data e = calc(n, a % c, b % c, c);  // 迭代

    d.h += e.h + 2 * bc % P * e.f % P + 2 * ac % P * e.g % P;
    d.g += e.g, d.f += e.f;
    d.f %= P, d.g %= P, d.h %= P;
    return d;
  }
  data e = calc(m - 1, c, c - b - 1, a);
  d.f = n * m % P - e.f, d.f = (d.f % P + P) % P;
  d.g = m * n % P * n1 % P - e.h - e.f, d.g = (d.g * i2 % P + P) % P;
  d.h = n * m % P * (m + 1) % P - 2 * e.g - 2 * e.f - d.f;
  d.h = (d.h % P + P) % P;
  return d;
}
```

## 线性基
### 线性基求交
``` C++
struct LinearBasis {
  long long basis[65];
  void clear(){
    memset(basis, 0, sizeof(basis));
  }
  void insert(long long val){
    for(int i = 60; i >= 0; i --){
      if(((val >> i) & 1) == 0) continue;
      if(basis[i]) val = val ^ basis[i];
      else basis[i] = val;
    }
  }
};

LinearBasis Merge(LinearBasis A,LinearBasis B) {
	LinearBasis All , C , D;
	All.clear();
	C.clear();
	D.clear();
	for (int i = 60;i >= 0;i--) {
		All.basis[i] = A.basis[i];
		D.basis[i] = 1ll << i;
	}
	for (int i = 60; i >= 0; i--) {
		if (B.basis[i]) {
			long long v = B.basis[i] , k = 0;
			bool flag = true;
			for (int j = 60; j >= 0; j--) {
				if (v & (1ll << j)) {
					if (All.basis[j]) {
						v ^= All.basis[j];
						k ^= D.basis[j];
					} else {
						flag = false;
						All.basis[j] = v;
						D.basis[j] = k;
						break;
					}
				}
			}
			if (flag) {
				long long v = 0;
				for (int j = 60; j >= 0; j--) {
					if (k & (1ll << j)) {
						v ^= A.basis[j];
					}
				}
				C.insert(v);
			}
		}
	}
	return C;
}
```

### 线性基求并
容斥后转化成线性基求交即可

### 区间线性基
$LinearBasis$ 记录基向量的时间戳，并通过 $query$ 函数得到区间线性基的抑或最大值。

``` C++
struct LinearBasis{
    int tim[33], bas[33];
    void insert(int x, int t){
        for(int i = 30; i >= 0; i --){
            if(((x >> i) & 1) == 0) continue;
            if(t > tim[i]){
                bas[i] ^= x;
                swap(x, bas[i]);
                swap(t, tim[i]);
            } 
            else x ^= bas[i];
        }
    }
}arr[maxn], temv;

int query(int l, int r){
    temv = arr[r];
    int ans = 0;
    for(int i = 30; i >= 0; i --){
        if(temv.tim[i] < l || temv.bas[i] == 0) continue;
        if((ans >> i) & 1) continue;
        ans = ans ^ temv.bas[i];
    }
    return ans;
}
```

## 数论函数
### 数论分块

$\sqrt{n}$ 复杂度内计算 $\sum_{i=1}^{n} f(\lfloor \frac{n}{i} \rfloor)$

``` C++
int cal(int n){
  long long ans = 0;
  for(int i = 1; i <= n; i ++){
    int val = n / i;
    int l = i, r = n / val; // 表示权值为 val 的数字在
    ans = ans + f(val) * (r - l + 1);
    i = r;
  }
}
```

### 积性函数
若 $f(x)$ 与 $g(x)$ 都是积性函数，则以下函数也是积性函数
$$
\begin{aligned}
h(x) & = f(x^p) \\
h(x) & = f^p(x) \\ 
h(x) & = f(x) * g(x) \\
h(x) & = \sum_{d|x} f(d) * g(\frac{x}{d})
\end{aligned}
$$

#### 常见的积性函数
单位函数： $\epsilon(n)=[n=1]$
恒等函数： $\operatorname{id}_k(n)=n^k$ $\operatorname{id}_{1}(n)$ 通常简记作 $\operatorname{id}(n)$ 。
常数函数： $1(n)=1$
除数函数： $\sigma_{k}(n)=\sum_{d\mid n}d^{k}$ ，$\sigma_{0}(n)$ 通常简记作 $\operatorname{d}(n)$ 或 $\tau(n)$ ， $\sigma_{1}(n)$ 通常简记作 $\sigma(n)$ 。
欧拉函数： $\varphi(n)=\sum_{i=1}^n [\gcd(i,n)=1]$
莫比乌斯函数： $\mu(n) = \begin{cases}1 & n=1 \\ 0 & \exists d:d^{2} \mid n \\ (-1)^{\omega(n)} & otherwise\end{cases}$ ，其中 $\omega(n)$ 表示 $n$ 的本质不同质因子个数，是一个加性函数。

### 狄利克雷卷积 ($Dirichlet$ 卷积)
积性函数 $f(x)$ 和 $g(x)$ 的 $Dirichlet$ 卷积: 
$$
(f * g)(x) = \sum_{d|x} f(d) g(\frac{x}{d})
$$

#### 例子
$$ 
\begin{aligned} 
\varepsilon = \mu * 1 & \Leftrightarrow \varepsilon(n) = \sum_{d\mid n}\mu(d) \\ 
d = 1 * 1 & \Leftrightarrow d(n) = \sum_{d \mid n} 1 \\ 
\sigma = d * 1 & \Leftrightarrow \varepsilon(n) = \sum_{d \mid n} d \\
\varphi = \mu * \text{ID} & \Leftrightarrow \varphi(n) = \sum_{d\mid n}d\cdot\mu(\frac{n}{d}) \\
\end{aligned} 
$$

### $Fibonacci$ 函数相关结论
1. 对于$Fibonacci$ 函数 $f(x)$ 有 $gcd(f(x), f(y)) == f(gcd(x, y))$
2. 如果 $fib(k)$ 能被 $x$ 整除，则 $fib(k*i)$ 都可以被 $x$ 整除。
3. $f(0)+f(1)+f(2)+…+f(n)=f(n+2)-1$
4. $f(1)+f(3)+f(5)+…+f(2n-1)=f(2n)$
5. $f(2)+f(4)+f(6)+…+f(2n) =f(2n+1)-1$
6. $[f(0)]^2+[f(1)]^2+…+[f(n)]^2=f(n)·f(n+1)$
7. $f(0)-f(1)+f(2)-…+(-1)^n·f(n)=(-1)^n·[f(n+1)-f(n)]+1$
8. $f(n+m)=f(n+1)·f(m)+f(n)*f(m-1)$
9. $[f(n)]^2=(-1)^{(n-1)}+f(n-1)·f(n+1)$
10. $f(2n-1)=[f(n)]^2-[f(n-2)]^2$
11. $3 * f(n)=f(n+2)+f(n-2)$
12. $f(2n-2m-2)[f(2n)+f(2n+2)]=f(2m+2)+f(4n-2m) [ n > m \geq -1,且n \geq 1]$
13. $f(2n+1)=[f(n)]^2+[f(n+1)]^2$
14. $f(i)f(i-1)-f(i+1)f(i-2)=(-1)^i$

## 数论相关简单结论

### 筛法

``` C++

const int maxn = 1e7+5;
bool flag[maxn];
int phi[maxn],pri[maxn];
int cnt = 0;

//f[i]表示i的最大质因子
for (int i = 2; i < maxn; ++i){
    if(f[i]) continue;
    for (int j = i;j < maxn; j += i) f[j] = i;
}

//筛质数
void GetPrime(){
    for (int i = 2; i < maxn; ++i){
        if (!flag[i]) pri[cnt++] = i;
        for (int j = 0; j < cnt && 1LL * pri[j] * i < maxn; ++j){
            flag[pri[j] * i] = 1;
            if (i % pri[j] == 0) break;
        }
    }
}

//筛欧拉函数
void Get_phi(){
    phi[1] = 1;
    for(int i = 2; i < maxn; i++){
        if(!flag[i]){
            pri[cnt++] = i;
            phi[i] = i - 1;
        }
        for(int j = 0; j < cnt; j++){
            if(1LL * i * pri[j] > maxn) break;
            flag[i * pri[j]] = true;
            if(i % pri[j] == 0){
                phi[i * pri[j]] = pri[j] * phi[i];
                break;
            }
            else phi[i * pri[j]] = (pri[j] - 1) * phi[i];
        }
    }
}

//筛莫比乌斯函数
void Get_mu(){
    mu[1] = 1;
    for(int i = 2; i < maxn; i++){
        if(!flag[i]){
            pri[cnt++] = i;
            mu[i] = -1;
        }
        for(int j = 0; j < cnt; j++){
            if(1LL * i * pri[j] > maxn) break;
            flag[i * pri[j]] = true;
            if(i % pri[j] == 0){
                mu[i * pri[j]] = 0;
                break;
            }
            else mu[i * pri[j]] = -mu[i];
        }
    }
}

//筛约数个数
int pri[maxn],e[maxn],div[maxn];
int cnt = 0;
void init(){
    div[1] = 1;
    for(int i = 2; i < maxn; i++){
        if(!flag[i]){
            pri[cnt++] = i;
            e[i] = 1;
            div[i] = 2;
        }
        for(int j = 0; j < cnt; j++){
            if(1LL * i * pri[j] > maxn) break;
            flag[i * pri[j]] = true;
            if(i % pri[j] == 0){
                e[i * pri[j]] = e[i] + 1;
                div[i * pri[j]] = div[i] / (e[i] + 1) * (e[i] + 2);
                break;
            }
            e[i * pri[j]] = 1;
            div[i * pri[j]] = div[i] * 2;
        }
    }
}

```

### 容斥
$f(n) = \sum_{d|n}g(d)$ ,已知 $f$, 求 $g$, 复杂度 $O(n*logn)$
``` C++

for (int i = 1; i <= n; ++i)
  for (int j = i + i; j <= n; j += i)       
    f[j] -= f[i];

```

$f[n]=\sum_{d|n} g(d)$ ,已知 $g$ ,求 $f$, 复杂度 $O(n*logn)$
``` C++

for (int i = n; i >= 1; --i)
  for (int j = i + i; j <= n; j += i)       
    f[j] += f[i];
```

$f[n]=\sum_{n|d}g(d)$, 已知 $f$, 求 $g$, 复杂度 $O(n*logn)$
``` C++

for (int i = n; i >= 1; --i)
  for (int j = i + i; j <= n; j += i)       
    f[i] -= f[j];

```

$f[n]=\sum_{n|d}g(d)$,已知 $g$ ,求 $f$, 复杂度 $O(n*logn)$
``` C++

for (int i = 1; i <= n; ++i)
  for (int j = i + i; j <= n; j += i)       
    f[i] += f[j];
    
``` 

$f[s]$ 存原来的元素，之后 $f[s]$ 存子集所有元素和
``` C++
for (int i = 0; i < n; i++)
    for (int s = 0; s < (1 << n); s++)
        if (s >> i & 1)
            f[s] += f[s ^ 1 << i];
``` 


$f[s]$ 存子集所有元素和，之后 $f[s]$ 存原来的元素
``` C++

for (int i = 0; i < n; i++)
    for (int s = 0; s < (1 << n); s++)
        if (s >> i & 1)
            f[s] -= f[s ^ 1 << i];
            
```

$h[x]=\sum_{d|x}(f[d]*g[\frac{x}{d}])$, 已知 $f,g$ 的 $1 \sim n$, 求 $h(x)$

``` C++
int f[MAXN],g[MAXN],h[MAXN]={0};
void calc(int n)
{    
    for (int i=1;i*i<=n;i++)
        for (int j=i;i*j<=n;j++)
            if(j==i)h[i*j]+=f[i]*g[i];
            else h[i*j]+=f[i]*g[j]+f[j]*g[i];
} 
```

已知 $f[i]$,求 $g[i] = \sum_{[gcd(i,j)=1]}f[i]$
``` C++
for(i = 1;i <= n; i++){
    for(j= i + i;j <= n; j += i) f[i] += f[j];
}
for(i = 1;i <= n; i++) f[i] *= mu[i];
for(i = n;i >= 1; i--){
    for(j = i + i;j <= n; j += i) f[j] += f[i];
}
新的f[i]即为g[i]
```

## 多项式算法(待更新)
### FFT(待更新)

### 分治FFT(待更新)

### FWT(待更新)

### NTT(待更新)

### 多项式求逆(待更新)

## 线性规划(待更新)
### 单纯形(待更新)
### KKT(待更新)
### 拉格朗日乘子法(待更新)

## 常见积分表(待更新)

## 常见生成函数(待更新)

## BM 线性递推
``` C++

#include <bits/stdc++.h>
 
using namespace std;
#define rep(i,a,n) for (long long i=a;i<n;i++)
#define per(i,a,n) for (long long i=n-1;i>=a;i--)
#define pb push_back
#define mp make_pair
#define all(x) (x).begin(),(x).end()
#define fi first
#define se second
#define SZ(x) ((long long)(x).size())
typedef vector<long long> VI;
typedef long long ll;
typedef pair<long long,long long> PII;
const ll mod=1e9+7;
ll powmod(ll a,ll b) {ll res=1;a%=mod; assert(b>=0); for(;b;b>>=1){if(b&1)res=res*a%mod;a=a*a%mod;}return res;}
// head
 
long long _,n;
namespace linear_seq
{
    const long long N=10010;
    ll res[N],base[N],_c[N],_md[N];
 
    vector<long long> Md;
    void mul(ll *a,ll *b,long long k)
    {
        rep(i,0,k+k) _c[i]=0;
        rep(i,0,k) if (a[i]) rep(j,0,k)
            _c[i+j]=(_c[i+j]+a[i]*b[j])%mod;
        for (long long i=k+k-1;i>=k;i--) if (_c[i])
            rep(j,0,SZ(Md)) _c[i-k+Md[j]]=(_c[i-k+Md[j]]-_c[i]*_md[Md[j]])%mod;
        rep(i,0,k) a[i]=_c[i];
    }
    long long solve(ll n,VI a,VI b)
    { // a 系数 b 初值 b[n+1]=a[0]*b[n]+...
//        printf("%d\n",SZ(b));
        ll ans=0,pnt=0;
        long long k=SZ(a);
        assert(SZ(a)==SZ(b));
        rep(i,0,k) _md[k-1-i]=-a[i];_md[k]=1;
        Md.clear();
        rep(i,0,k) if (_md[i]!=0) Md.push_back(i);
        rep(i,0,k) res[i]=base[i]=0;
        res[0]=1;
        while ((1ll<<pnt)<=n) pnt++;
        for (long long p=pnt;p>=0;p--)
        {
            mul(res,res,k);
            if ((n>>p)&1)
            {
                for (long long i=k-1;i>=0;i--) res[i+1]=res[i];res[0]=0;
                rep(j,0,SZ(Md)) res[Md[j]]=(res[Md[j]]-res[k]*_md[Md[j]])%mod;
            }
        }
        rep(i,0,k) ans=(ans+res[i]*b[i])%mod;
        if (ans<0) ans+=mod;
        return ans;
    }
    VI BM(VI s)
    {
        VI C(1,1),B(1,1);
        long long L=0,m=1,b=1;
        rep(n,0,SZ(s))
        {
            ll d=0;
            rep(i,0,L+1) d=(d+(ll)C[i]*s[n-i])%mod;
            if (d==0) ++m;
            else if (2*L<=n)
            {
                VI T=C;
                ll c=mod-d*powmod(b,mod-2)%mod;
                while (SZ(C)<SZ(B)+m) C.pb(0);
                rep(i,0,SZ(B)) C[i+m]=(C[i+m]+c*B[i])%mod;
                L=n+1-L; B=T; b=d; m=1;
            }
            else
            {
                ll c=mod-d*powmod(b,mod-2)%mod;
                while (SZ(C)<SZ(B)+m) C.pb(0);
                rep(i,0,SZ(B)) C[i+m]=(C[i+m]+c*B[i])%mod;
                ++m;
            }
        }
        return C;
    }
    long long gao(VI a,ll n)
    {
        VI c=BM(a);
        c.erase(c.begin());
        rep(i,0,SZ(c)) c[i]=(mod-c[i])%mod;
        return solve(n,c,VI(a.begin(),a.begin()+SZ(c)));
    }
};
 
int main()
{
    while(~scanf("%I64d", &n))
    {   printf("%I64d\n",linear_seq::gao(VI{1,5,11,36,95,281,781,2245,6336,18061, 51205},n-1));
    }
}

```

## Lucas 定理
$p$ 是素数，且相对较小时:
$$
C_{n}^{m} \% p = C_{n/p}^{m/p} * C_{n\%p}^{m\%p} \, \% \, p
$$

### 扩展 Lucas 定理
$p$ 不是素数，且 $p = \prod p_{i}^{\alpha_i}, p_i \in prime$ 时， 求出 $f_i = C_{n}^{m} \% {p_i}^{\alpha_i}$ 的值，再对 $f_i$ 通过中国剩余定理合并。

关于 $C_{n}^{m} \; mod \; {p_i}^{\alpha_i}$, 我们可以考虑计算 $n! \; mod \; {p_i}^{\alpha_i}$, $m! \; mod \; {p_i}^{\alpha_i}$, $(n-m)! \; mod \; {p_i}^{\alpha_i}$。
比如计算 $10! \; mod \; 3$, 相当于计算 $1 * 2 * 1 * 4 * 5 * 2 * 7 * 8 * 1 * 10 * 3^{4} \; mod \; 3$。

``` C++
#include<bits/stdc++.h>

using namespace std;

typedef long long ll;

ll exgcd(ll a,ll b,ll &x,ll &y)
{
    if(!b){x=1;y=0;return a;}
    ll res=exgcd(b,a%b,x,y),t;
    t=x;x=y;y=t-a/b*y;
    return res;
}

ll p;

inline ll power(ll a,ll b,ll mod)
{
    ll sm;
    for(sm=1;b;b>>=1,a=a*a%mod)if(b&1)
        sm=sm*a%mod;
    return sm;
}

ll fac(ll n,ll pi,ll pk)
{
    if(!n)return 1;
    ll res=1;
    for(register ll i=2;i<=pk;++i)
        if(i%pi)(res*=i)%=pk;
    res=power(res,n/pk,pk);
    for(register ll i=2;i<=n%pk;++i)
        if(i%pi)(res*=i)%=pk;
    return res*fac(n/pi,pi,pk)%pk;
}

inline ll inv(ll n,ll mod)
{
    ll x,y;
    exgcd(n,mod,x,y);
    return (x+=mod)>mod?x-mod:x;
}

inline ll CRT(ll b,ll mod){return b*inv(p/mod,mod)%p*(p/mod)%p;}

const int MAXN=11;

static ll n,m;

static ll w[MAXN];

inline ll C(ll n,ll m,ll pi,ll pk)
{
    ll up=fac(n,pi,pk),d1=fac(m,pi,pk),d2=fac(n-m,pi,pk);
    ll k=0;
    for(register ll i=n;i;i/=pi)k+=i/pi;
    for(register ll i=m;i;i/=pi)k-=i/pi;
    for(register ll i=n-m;i;i/=pi)k-=i/pi;
    return up*inv(d1,pk)%pk*inv(d2,pk)%pk*power(pi,k,pk)%pk;
}

inline ll exlucus(ll n,ll m)
{
    ll res=0,tmp=p,pk;
    static int lim=sqrt(p)+5;
    for(register int i=2;i<=lim;++i)if(tmp%i==0)
    {
        pk=1;while(tmp%i==0)pk*=i,tmp/=i;
        (res+=CRT(C(n,m,i,pk),pk))%=p;
    }
    if(tmp>1)(res+=CRT(C(n,m,tmp,tmp),tmp))%=p;
    return res;
}

int main()
{
    scanf("%lld%lld%d",&n,&m,&p);
    printf("%d\n",exlucus(n,m));
    return 0;
}
```

## 中国剩余定理 (待更新)



## 置换群计数问题
### Burnside 引理
若 $D(a_i)$ 表示在置换 $a_i$ 下不变的元素个数, $G$ 表示置换群大小, $L$ 表示本质不同的方案数。则
$$
L = \frac{1}{|G|} \sum^{s} D(a_i)
$$

### Polya 定理
若 $G$ 表示置换群大小, $L$ 表示用 $m$ 种颜色对 $p$ 个元素着色在置换群中本质不同的方案数。则
$$
L = \frac{1}{|G|} \sum_{i}^{s} m ^ {c(g_i)}
$$

### min-max反演
$$
\max(S)=\sum_{T \subseteq S}(-1)^{|T|+1}\min(T)\\
\min(S)=\sum_{T \subseteq S}(-1)^{|T|+1}\max(T)
$$
例题 刚开始你有一个数字0，每一秒钟你会随机选择一个$[0,2^n)$的数字，与你手上的数字进行或操作。选择数字i的概率是$p_i$。问期望多少秒后，你手上的数字变成$2^n-1$。

题解 我们要求的，实际上是一个集合n个1中最晚出现的1的期望时间
$$E(max\{S\})=∑_{T⊆S}(−1)^{|T|+1}E(min\{T\})$$
那么问题就转化为了求每个集合中最早出现的1的期望时间。
假如在k时刻出现，那么前k−1时刻一定都是取的补集的子集，记T补集的所有子集概率和为$P$
$$
E(min\{T\})=∑_{k=1}^{∞}k(1-P)(P)^{k−1}\\
E(min\{T\})=\frac{1}{1-P}
$$
先用高维前缀和求出子集的概率之和，再枚举$\{T\}$求出答案。

# 动态规划
## 树上依赖背包(待更新)
## 可逆背包(待更新)
## SOSdp
> https://blog.csdn.net/weixin_38686780/article/details/100109753

## wqs二分
将区间分成m段，每段的代价是x^2，用wqs二分处理m，剩下的部分使用斜率优化来做。
``` C++
#include <bits/stdc++.h>
#define mid ((L + R) >> 1)
using namespace std;
const int N = 3005;
typedef long long LL;
int n, m;
LL s[N], f[N], g[N];//f表示dp值,g表示至少需要分成多少个区间
int q[N], l, r;//斜率优化的数组
inline LL sqr(LL x) { return 1LL * x * x; }
LL k(int a, int b) { return f[a] + sqr(s[a]) - f[b] - sqr(s[b]); }
int check(LL t) {
	q[0] = 0;
	l = 0;
	r = 1;
	for (int i = 1; i <= n; ++i) {
		while (r - l > 1 &&
		       (k(q[l + 1], q[l]) < 2 * s[i] * (s[q[l + 1]] - s[q[l]]) ||
		        (k(q[l + 1], q[l]) == 2 * s[i] * (s[q[l + 1]] - s[q[l]]) &&
		         g[q[l + 1]] <= g[q[l]]))) {
			l++;
		}
		f[i] = t + f[q[l]] + sqr(s[i] - s[q[l]]);
		g[i] = g[q[l]] + 1;
		while (r - l > 1 &&
		       (k(q[r - 1], q[r - 2]) * (s[i] - s[q[r - 1]]) >
		            k(i, q[r - 1]) * (s[q[r - 1]] - s[q[r - 2]]) ||
		        (k(q[r - 1], q[r - 2]) * (s[i] - s[q[r - 1]]) ==
		             k(i, q[r - 1]) * (s[q[r - 1]] - s[q[r - 2]]) &&
		         g[q[r - 1]] >= g[i]))) {
			r--;
		}
		q[r++] = i;
	}
	return g[n];
}
int main() {
	scanf("%d%d", &n, &m);
	for (int i = 1; i <= n; ++i) {
		scanf("%lld", &s[i]);
		s[i] += s[i - 1];
	}
	LL L = 0, R = sqr(s[n]);
	while (L < R) {
		if (check(mid) > m) {
			L = mid + 1;
		} else {
			R = mid;
		}
	}
	check(L);
	printf("%lld\n", m * (f[n] - m * L) - sqr(s[n]));
	return 0;
}
```
区间的代价是到中位数的距离之和的情况。
```c++
#include <bits/stdc++.h>
#define calc(x, y) f[x] + dis[x + 1][y]
using namespace std;
const int N = 3005;
typedef long long LL;
int n, m, a[N], pre[N], dis[N][N], f[N], g[N], q[N];//f表示dp值,g表示至少需要分成多少个区间,ai表示q[i]为最优决策点的区间的右端点
int check(int o) {
	int L = 0, R = 1;
	q[0] = 0;
	a[0] = n;
	for (int i = 1; i <= n; ++i) {
		f[i] = calc(q[L], i) + o;
		g[i] = g[q[L]] + 1;
		if (a[L] == i) L++;
		while (L < R) {
			int l = (L + 1 == R) ? i + 1 : a[R - 2] + 1;
			if (calc(q[R - 1], l) > calc(i, l)) {
				R--;
			} else
				break;
		}
		if (L == R) {
			q[R] = i;
			a[R++] = n;
		} else if (calc(q[R - 1], n) > calc(i, n)) {
			int l = (L + 1 == R) ? i + 1 : a[R - 2] + 1;
			int r = n;
			while (l < r) {
				int mid = (l + r + 1) >> 1;
				if (calc(q[R - 1], mid) > calc(i, mid)) {
					r = mid - 1;
				} else {
					l = mid;
				}
			}
			a[R - 1] = l;
			q[R] = i;
			a[R++] = n;
		}
	}
	return g[n];
}
int main() {
    scanf("%d%d", &n, &m);
	for (int i = 1; i <= n; ++i) {
		scanf("%d", &a[i]);
	}
	sort(a + 1, a + n + 1);
	for (int i = 1; i <= n; ++i) {
		pre[i] = pre[i - 1] + a[i];
	}
	for (int i = 1; i <= n; ++i) {
		for (int j = i; j <= n; ++j) {
			int mid = (i + j) >> 1;
			dis[i][j] = (mid - i) * a[mid] - pre[mid - 1] + pre[i - 1];
			dis[i][j] += pre[j] - pre[mid] - (j - mid) * a[mid];
		}
	}
	int L = 0, R = 1e7;
	while (L < R) {
		int mid = (L + R) >> 1;
		if (check(mid) > m) {
			L = mid + 1;
		} else {
			R = mid;
		}
	}
	check(L);
	printf("%d\n", f[n] - m * L);
	return 0;
}
```

# 图论
## 斯坦纳树
最小生成树是在给定的点集和边中寻求最短网络使所有点连通。而最小斯坦纳树允许在给定点外增加额外的点，使生成的最短网络开销最小。

令$f[i][sta]$表示 $i$ 号节点，与关键节点节点的联通性为 $sta$ 时的最小代价，这里的 $sta$ 是一个二进制数，在它二进制下的每一位中，$0$ 表示不连通，$1$ 表示联通。
那么转移的时候会有两种情况
> 由子集转移而来: $f[i][sta] = min_{s \in sta} \{ cal(i, s, C_{sta}s)\}$

> 由不含该节点的状态转移而来: $f[i][s] = min\{ f[k][s] + val(i, k)\}$

总复杂度为 $O(n*3^k)$

``` plain
伪代码
枚举状态集 sta
{  
    
    枚举 sta 的子集 s 
    { 
        更新 f[1~n][sta]
    } 
    将 f[S][x]<inf 的x入队 
    spfa(S)
}
```

## 虚树

> 1.如果栈为空,或者栈中只有一个元素,那么显然应该:
    $stk[++top]=u;$
> 2.取 $lca=LCA(u,stk[top])$,如果 $lca=stk[top]$,则说明 $u$ 点应该接着 $stk[top]$ 点延长当前的树链.做操作: $stk[++top]=u;$
> 3.如果 $lca≠stk[top]$,则说明 $u$ 与 $stk[top]$ 分属 $lca$ 的两颗不同的子树,且包含 $stk[top]$ 的这颗子树应该已经构建完成了,我们需要做的是: 将 $lca$ 的包含 $stk[top]$ 子树的那部分退栈,并将这部分建边形成虚树.如果 $lca$ 不在栈(树链)中,那么要把 $lca$ 也加入栈中,保证虚树的结构不出现问题,随后将 $u$ 加入栈中,以表延长树链.

``` C++
//实现按照 dfn 顺序逐个将关键点插入形成一颗虚树
void insert(int u){
    if(top <= 1) {stk[++top] = u;return ;}
    int lca = LCA(u,stk[top]);
    if(lca == stk[top]) {stk[++top] = u;return ;}
    while(top > 1 && dfn[lca] <= stk[top-1]) {
        addedge(stk[top-1],stk[top]);
        --top;
    }
    if(lca != stk[top]) stk[++top] = lca;
    stk[++top] = u;
}
```
也可以先将关键点按 $dfs$ 序排序，得到序列 $a$ , 然后对 $a_i$ 和 $a_{i+1}$ 分别求 $lca$，再将所得到的点进行去重。	
> 如果只是单次建虚树，则可以考虑 $dfs$ 如果一个节点存在两颗子树有关键点，那么这个节点也是关键点。	
## 树哈希

Method I

Formula:
$$
f_{now} = size_{now} * \sum_{i} f_{son_{now, i}} * seed^{i-1}
$$

Note:
其中 $f_x$ 为以节点 $x$ 为根的子树对应的哈希值。特殊地，我们令叶子节点的哈希值为 $1$ 。

$size_x$ 表示以节点 $x$ 为根的子树大小。

$son_{x,i}$ 表示 $x$ 所有子节点以 $f$ 作为关键字排序后排名第 $i$ 的儿子。

$seed$ 为选定的一个合适的种子（最好是质数，对字符串 $hash$ 有了解的人一定不陌生）

上述哈希过程中，可以适当取模避免溢出或加快运行速度。

Method II
Formula
$$
f_{now} = \bigoplus_{i} f_{son_{now, i}} * seed + size_{son_{now, i}}
$$
Note:

其中 $f_x$ 为以节点 $x$ 为根的子树对应的哈希值。特殊地，我们令叶子节点的哈希值为 $1$ 。

$size_x$ 表示以节点 $x$ 为根的子树大小。

$son_{x,i}$ 表示 $x$ 的子节点(不用排序)

Hack:
由于异或的性质，如果一个节点下有多棵本质相同的子树，这种哈希值将无法分辨该种子树出现 $1, 3, 5, ....$ 次的情况。


Method III
Formula

$$
f_{now} = 1 + \sum_{i} f_{son_{now, i}} * prime(size_{son_{now, i}})
$$
其中 $f_x$ 为以节点 $x$ 为根的子树对应的哈希值。特殊地，我们令叶子节点的哈希值为 $1$ 。
$size_x$ 表示以节点 $x$ 为根的子树大小。
$son_{x,i}$ 表示 $x$ 的子节点(不用排序)
$prime(i)$ 表示第 $i$ 个素数
	
## 支配树(待更新)	

## prufer 序列 (待更新)	

## LGV 引理 (待更新)	
Lindström–Gessel–Viennot lemma，即 LGV 引理，可以用来处理有向无环图上不相交路径计数等问题。

## 二分图匹配问题

### 最长反链(待更新)

### 霍尔定理

二分图一侧的子图$V$有完全匹配，当且仅当对$V$的任意子集$A$,和$A$直接相连的点的个数大于等于$A$的点的个数。
如果一个点集$S$满足上述条件,那么它一定是一个完美匹配的子集。
霍尔定理也可以求匹配数:$|V| - max(|A| - T(A))$,$T(A)$是指另一侧中和$A$直接相连的点的个数。

### 最小点覆盖方案构造
对二分图做完最大匹配后，从左侧所有未被匹配的点出发，每次从左往右走一条未被匹配的边，从右往左走一条被匹配的边，沿途打标记。最终选择左边所有未被标记的点，加上右边所有被标记的点，此点集可作为一组最小点覆盖方案。其补集可作为一组最大点独立集方案。

### HopcroftKarp算法(二分图匹配)
```C++
O(nsqrt(m)) be careful init
const int maxN = 55 * 55;
const int maxM = 55 * 55;
struct HopcroftKarp {
	int vis[maxN], level[maxN], ml[maxN], mr[maxM];
	vector<int> edge[maxN];  // constructing edges for left part only

	void init(int n) {
		for (int i = 1; i <= n; ++i) edge[i].clear();
	}

	void add(int u, int v) { edge[u].push_back(v); }

	bool dfs(int u) {
		vis[u] = true;
		for (vector<int>::iterator it = edge[u].begin(); it != edge[u].end();
		     ++it) {
			int v = mr[*it];
			if (v == -1 || (!vis[v] && level[u] < level[v] && dfs(v))) {
				ml[u] = *it;
				mr[*it] = u;
				return true;
			}
		}
		return false;
	}

	int matching(int n) {  // n for left
		memset(vis, 0, sizeof(vis));
		memset(level, 0, sizeof(level));
		memset(ml, -1, sizeof(ml));
		memset(mr, -1, sizeof(mr));
		for (int match = 0;;) {
			queue<int> que;
			for (int i = 1; i <= n; ++i) {
				if (ml[i] == -1) {
					level[i] = 0;
					que.push(i);
				} else
					level[i] = -1;
			}
			while (!que.empty()) {
				int u = que.front();
				que.pop();
				for (vector<int>::iterator it = edge[u].begin();
				     it != edge[u].end(); ++it) {
					int v = mr[*it];
					if (v != -1 && level[v] < 0) {
						level[v] = level[u] + 1;
						que.push(v);
					}
				}
			}
			for (int i = 1; i <= n; ++i) vis[i] = false;
			int d = 0;
			for (int i = 1; i <= n; ++i)
				if (ml[i] == -1 && dfs(i)) ++d;
			if (d == 0) return match;
			match += d;
		}
	}
} HK;
```

# 数据结构

## 双栈模拟 (待更新)
适用于询问区间双端点都单调的情况



## 长链剖分(待更新)
> https://blog.bill.moe/long-chain-subdivision-notes/
### 求距离为k的儿子个数(入点的时候减去，离开的时候加)

## 可持久化数据结构

## 区间LCM
带修改，区间范围在(1-100)之间的情况
将因为超过一个数字至多一个超过10的质因子，因此可以用bitset优化超过10的质因子是否存在，小于10的部分用两个int记录2,3,5,7的LCM和GCD。
```c++
const int N = 305000;
const int PRI_NUM = 21;
char s[105];
int pre4_pri[] = {2, 3, 5, 7},
    pri[PRI_NUM] = {11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47,
                    53, 59, 61, 67, 71, 73, 79, 83, 89, 97};
struct node {
	int val = 1;//只含2,3,5,7素因子的区间LCM值
	int gcd = 1;//只含2,3,5,7素因子的区间gcd值
	bitset<21> bits;//每个素数是否存在
	int get(int p) { // mod p
		int ret = val % p;
		for (int i = 0; i < PRI_NUM; ++i) {
			if (bits.test(i)) ret = 1LL * ret * pri[i] % p;
		}
		return ret;
	}
	void change(int u) {
		gcd = u;
		val = 1;
		for (int i = 0; i < 4; ++i) {
			while (u % pre4_pri[i] == 0) {
				val *= pre4_pri[i];
				u /= pre4_pri[i];
			}
		}
		for (int i = 0; i < PRI_NUM; ++i) {
			bits[i] = u % pri[i] == 0;
		}
	}
	void merge(node b, node c) {
		gcd = __gcd(b.gcd, c.gcd);
		val = b.val / __gcd(b.val, c.val) * c.val;
		bits = b.bits | c.bits;
	}
} tr[N << 2];
int lazy[N << 2];
void build(int o, int L, int R) {
	if (L + 1 == R) {
		int u;
		scanf("%d", &u);
		tr[o].change(u);
		return;
	}
	build(ls, L, mid);
	build(rs, mid, R);
	tr[o].merge(tr[ls], tr[rs]);
}
inline void pushdown(int o) {
	if (lazy[o]) {
		lazy[ls] = lazy[rs] = lazy[o];
		tr[ls] = tr[rs] = tr[o];
		lazy[o] = 0;
	}
}
node Q(int o, int L, int R, int l, int r) {
	if (l <= L && R <= r) return tr[o];
	pushdown(o);
	if (r <= mid) return Q(ls, L, mid, l, r);
	if (l >= mid) return Q(rs, mid, R, l, r);
	node ret;
	ret.merge(Q(ls, L, mid, l, r), Q(rs, mid, R, l, r));
	return ret;
}
void c(int o, int L, int R, int l, int r, int val) {
	if (l <= L && R <= r) {
		lazy[o] = val;
		tr[o].change(val);
		return;
	}
	pushdown(o);
	if (l < mid) c(ls, L, mid, l, r, val);
	if (r > mid) c(rs, mid, R, l, r, val);
	tr[o].merge(tr[ls], tr[rs]);
}
```

# 几何

# 杂项
### long long范围内任意模数乘法(利用自然溢出)
``` C++
LL mul(LL a,LL b) {
    LL r = (a * b - (LL)(((long double)a * b) / mod) * mod);
    return add(r - r / mod * mod,mod);
}
```

### 状态压缩下的子集枚举

```C++
for(int i = s; i; i = (i-1) & s); //枚举s的子集，复杂度O(2^n)
for(int s = 1; s < (1<<n); s ++){
  for(int i = s; i; i = (i-1) & s){
    // 枚举所有集合s，并枚举s的所有子集
  }
}
```

### 高维前缀和(子集求和)
```C++
int all = 1 << n;
for (int i = 0; i < n; ++i) {
	for (int j = all - 1; j; --j) {
		if (j >> i & 1) a[j] += a[j ^ (1 << i)];
	}
}
```

### 不平衡分块
分块的时候要考虑询问次数，不要死记sqrt(m)

### 股票问题
对于购买区间[L,R]的股票可以看成第L天买入，第L+1天卖出，第L+1天买入，第L+2天卖出，...，将区间转化成单点问题

### 思维是否各维度可以独立
特别是在棋盘问题和二维平面中，如果可以独立思考可以方便的化简问题。

### 位运算问题
位运算问题的常用工具：SOSdp、线性基、FWT、字典树、按位考虑后类欧几里得、异或还可以考虑前缀和。

### 极大区间统计(问区间内有多少个子段)
考虑第一个变化的位置对答案的贡献，如果是区间询问可以特判第一位，从第二位开始。

### 找规律
注意循环节，二进制，组合数，阶乘，记得打表看一眼。

### 求N(1<=1e18)项数列的值
求N项的值的常用工具：找规律，循环节，矩乘，生成函数，BM，二进制分解。

