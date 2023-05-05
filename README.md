# SMU 2023.1

Projeto aos moldes do [semestre 2011.1](https://github.com/boidacarapreta/smu20211/milestones?direction=asc&sort=due_date&state=closed).

## Máquinas de estado

Registro e entrada na sala de partida:

```mermaid
stateDiagram-v2
    state if_registro <<choice>>

    [*] --> WebSocket
    
    WebSocket --> Registro: "registro"
    
    Registro --> if_registro
    if_registro --> Registrado: "registro-ok"
    if_registro --> Não_registrado: "registro-nok"
    
    Não_registrado --> [*]

    Registrado --> Entrar_na_sala: "entrar-na-sala"
    Entrar_na_sala --> Na_sala_de_partida: "jogadores"
    Na_sala_de_partida --> [*]
```

## Repositórios dos alunos

- [Alana](https://github.com/alanamandim/smu20231)
- [Filipi](https://github.com/VirgilioFilipi/SMU2023.1) ([projeto](https://github.com/users/VirgilioFilipi/projects/2))
