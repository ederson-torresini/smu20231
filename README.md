# SMU 2023.1

Projeto aos moldes do [semestre 2011.1](https://github.com/boidacarapreta/smu20211/milestones?direction=asc&sort=due_date&state=closed).

## Máquinas de estado

Registro:

```mermaid
stateDiagram-v2
    state if_registro <<choice>>

    [*] --> WebSocket
    WebSocket --> Registro: registro
    
    Registro --> if_registro
    if_registro --> Registrado: ok
    if_registro --> Não_registrado: nok
    
    Registrado --> [*]
    Não_registrado --> [*]
```
