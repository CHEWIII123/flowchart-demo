# flowchart-demo# 美国投资新规合规流程图

```mermaid
graph TD
    A[交易是否涉及"美国人"?<br/>（公民/居民/分支机构/子公司）] -->|是| B[交易类型是否受管制?<br/>（股权/债务/可转换股权/中国相关）]
    A -->|否| RESULT1["交易不受限制<br/>（新规不适用）"]
    B -->|是| C[是否符合例外情况?<br/>（公开证券/衍生品/股权激励等）]
    B -->|否| RESULT2["交易可继续进行"]
    C -->|是| RESULT2
    C -->|否| D[是否与中国有关联?<br/>（实体/持股50%+/政府关联）]
    D -->|是| E[涉及敏感技术?<br/>（半导体/量子计算/AI）]
    D -->|否| RESULT2
    E -->|是| RESULT3["需通报或被禁止"]
    E -->|否| RESULT2

    classDef decision fill:#f6f6f6,stroke:#333,stroke-width:2px;
    classDef result fill:#e8f4ff,stroke:#1e88e5,stroke-width:2px;
    class A,B,C,D,E decision
    class RESULT1,RESULT2,RESULT3 result
```
