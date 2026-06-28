# AzerothCore — PlayerBot + AI 聊天中文分支

基于 [liyunfan1223/azerothcore-wotlk](https://github.com/liyunfan1223/azerothcore-wotlk) 的 PlayerBot 分支，集成以下模块：

- [mod-playerbots](https://github.com/liyunfan1223/mod-playerbots) — 智能机器人系统
- [mod-ollama-chat](https://github.com/ashesaa11/mod-ollama-chat) — LLM AI 聊天（中文优化）

## 与上游的区别

- 分支 `liyunfan-playerbot`（基于 liyunfan1223 的 Playerbot 分支）
- 集成 mod-ollama-chat 子模块（GBK→UTF-8 编码修复，中文 prompt 模板）
- 中文机器人名和公会名数据库

## 编译

```bash
cmake -S . -B build -G "Visual Studio 17 2022" -A x64 \
  -DTOOLS_BUILD=all -DSCRIPTS=static \
  -DBOOST_ROOT="D:/local/boost_1_85_0" \
  -DOPENSSL_ROOT_DIR="D:/WOW/OpenSSL"

cmake --build build --config RelWithDebInfo --parallel 16
```

## 项目主页

[wow-ai-bots-cn](https://github.com/ashesaa11/wow-ai-bots-cn)
