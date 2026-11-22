# API Testing Portfolio - Basics

## 项目简介
这是接口自动化入门实战仓库，主要记录从基础请求到 pytest 框架落地的过程。

## 技术栈
- Python 3.13
- Requests（HTTP 请求）
- Pytest（测试框架）
- Git（版本控制）

## 目录结构
- `week1_basics/day1_first_request.py`: 最基础的 GET/POST 请求与响应解析
- `week1_basics/test_day4_fixture.py`: 使用 Pytest Fixture 实现鉴权 token 的公共前置
- `week1_basics/test_day5_parametrize.py`: 使用 Pytest Parametrize 实现数据驱动测试

## 覆盖的测试场景
基于公开 API 项目 `Restful Booker`，目前覆盖了以下场景：
1. **鉴权测试**：正确/错误账号密码、空密码登录，验证 Token 返回与异常提示。
2. **业务链路**：登录获取 Token -> 携带 Token 查询订单 -> 修改订单信息。
3. **边界与异常值**：修改订单价格时传入正常值（999）、负数（-10）、零值（0），发现接口未做负数校验（潜在缺陷）。

## 如何运行
1. 克隆仓库：`git clone https://github.com/你的用户名/api-testing-portfolio.git`
2. 安装依赖：`pip install requests pytest`
3. 运行用例：`pytest week1_basics/ -v`

## 学习心得
理解 `print` 与 `assert` 的本质区别，掌握了用 Fixture 解决用例间的依赖共享，以及用数据驱动减少冗余代码。




