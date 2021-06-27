# xdai-rpc
About xdai rpc
ABOUT
Drill is an HTTP Load testing framework

This repo contains files for loadtesting

xDai RPC
with most common RPC requests we've had on our public RPCS:

eth_blockNumber
eth_getBalance
eth_getBlockByNumber
net_version
eth_getLogs
PREREQUISITIES
Install Rust https://www.rust-lang.org/tools/install
Install Drill https://github.com/fcsonline/drill
Clone the repo git clone https://github.com/igorbarinov/drill-configs-rpc.git
RUN
drill --benchmark xdai-benchmark.yml --stats

EXAMPLE OUTPUT OF A RUN
eth_getLogs               https://dai.poa.network/ 200 OK 394ms
eth_getLogs               https://dai.poa.network/ 200 OK 344ms
eth_getLogs               https://dai.poa.network/ 200 OK 373ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 270ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 333ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 345ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 236ms
eth_getLogs               https://dai.poa.network/ 200 OK 427ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 326ms
eth_getLogs               https://dai.poa.network/ 200 OK 369ms
eth_getLogs               https://dai.poa.network/ 200 OK 327ms
eth_getBlockByNumber      https://dai.poa.network/ 200 OK 372ms
eth_getLogs               https://dai.poa.network/ 200 OK 382ms


eth_getLogs               Total requests            250
eth_getLogs               Successful requests       249
eth_getLogs               Failed requests           1
eth_getLogs               Median time per request   437ms
eth_getLogs               Average time per request  464ms
eth_getLogs               Sample standard deviation 155ms

eth_getBlockByNumber      Total requests            750
eth_getBlockByNumber      Successful requests       748
eth_getBlockByNumber      Failed requests           2
eth_getBlockByNumber      Median time per request   377ms
eth_getBlockByNumber      Average time per request  392ms
eth_getBlockByNumber      Sample standard deviation 124ms

net_version               Total requests            250
net_version               Successful requests       249
net_version               Failed requests           1
net_version               Median time per request   379ms
net_version               Average time per request  397ms
net_version               Sample standard deviation 146ms

eth_blockNumber           Total requests            250
eth_blockNumber           Successful requests       250
eth_blockNumber           Failed requests           0
eth_blockNumber           Median time per request   446ms
eth_blockNumber           Average time per request  477ms
eth_blockNumber           Sample standard deviation 122ms

eth_getBalance            Total requests            500
eth_getBalance            Successful requests       500
eth_getBalance            Failed requests           0
eth_getBalance            Median time per request   377ms
eth_getBalance            Average time per request  404ms
eth_getBalance            Sample standard deviation 176ms

Concurrency Level         50
Time taken for tests      19.0 seconds
Total requests            2000
Successful requests       1996
Failed requests           4
Requests per second       105.33 [#/sec]
Median time per request   394ms
Average time per request  415ms
Sample standard deviation 149ms
