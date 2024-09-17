
```
___  ___ ______________  ___  ___   _   _
|  \/  ||  ___| ___ \  \/  | / _ \ | \ | |
| .  . || |__ | |_/ / .  . |/ /_\ \|  \| |
| |\/| ||  __||    /| |\/| ||  _  || . ` |
| |  | || |___| |\ \| |  | || | | || |\  |
\_|  |_/\____/\_| \_\_|  |_/\_| |_/\_| \_/

```
# :mermaid: CHARTS :mermaid:

---
Had fun doing some light process mapping for a project at work.

Still so much to explore:
- different icons
- colours
- shapes
- change title font colour

:point_down:

```mermaid

---

title: Audit Flow

---
%%{
    init:
        {
            'theme':'dark'
            ,'fontFamily':'monospace'
            ,'darkMode':'true'
        }

}%%

flowchart LR


    A[download Manual Upload list]      --> B(fa:fa-database Postgres)
    B(fa:fa-database Postgres)          --> |fa:fa-file csv| C[duckdb]
    D[fa:fa-file lists from shops]      --> |fa:fa-file csv| C[duckdb]
    C[duckdb]                           --> E[load data]
    F[check data types]                 --> G[check Dupes]
    G[check Dupes]                      --> H[find columns]
    H[find columns]                     --> E[EDA]
    E[EDA]                              --> I[filter out Opt-outs]
    I[filter out Opt-outs]              --> J[aggregate verication sources]
    J[aggregate verication sources]     --> L[detailed verifation sources]
    J[aggregate verication sources]     --> |fa:fa-file csv| M[send output to G Drive]
    L[detailed verifation sources]      --> |fa:fa-file csv| M[send output to G Drive]
    M[send output to G Drive]           --> P[inform compliance team]

```

:books: bibliography:
- [ascii art generato](https://patorjk.com/software/taag/#p=display&f=Graffiti&t=Type%20Something%20)r
- [tutorials](https://mermaid.js.org/ecosystem/tutorials.html)
