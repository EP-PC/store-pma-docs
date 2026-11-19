# Apresentação

A [página de apresentação](https://insper.github.io/platform/2026.2/exercises/project/presentation/)
pede um vídeo de **1 a 2 minutos** com: introdução, arquitetura, demonstração, desafios
(bottlenecks) e conclusão.

## Vídeo (1 min 58 s)

<video controls preload="metadata" width="100%">
  <source src="../video/store-pma.mp4" type="video/mp4">
  Seu navegador não toca vídeo: <a href="../video/store-pma.mp4">baixe o arquivo</a>.
</video>

**Como foi feito.** As cenas de terminal e de navegador são **gravações reais** do projeto rodando:
a loja completa (imagens do grupo no Docker Hub), os mesmos `k8s.yaml` do EKS num cluster kind com
o HPA escalando, o Grafana do Order com tráfego, e o cache e a varredura do Exchange. Elas foram
gravadas no GitHub Actions (repositório privado `garciapp2/store-pma-video`), e cada clipe tem um
selo com a velocidade em que aparece. Os diagramas são animações feitas com o Manim. A narração é
de Pedro Garcia; as cenas foram sincronizadas com ela frase a frase, a partir da transcrição.

## Roteiro narrado

| Tempo | Parte | O que aparece |
|---|---|---|
| 0:00 | Introdução: o projeto e o grupo | título e integrantes |
| 0:13 | Arquitetura: gateway, serviços, AWS e Jenkins | diagrama animado |
| 0:35 | Demonstração: 401 sem login, 403 para USER, pedido convertido em reais, 422 | gravação da loja pelo gateway |
| 0:53 | Kubernetes e teste de carga: health-check e HPA de 1 para 4 réplicas | gravação no cluster kind |
| 1:05 | Bottlenecks: 2 por integrante | tabela animada |
| 1:21 | Observabilidade | gravação do Grafana |
| 1:26 | Exchange: cache (~800 → 4 ms) e Trivy barrando a imagem | gravações do benchmark e do Trivy |
| 1:39 | Custos e disponibilidade | animação |
| 1:49 | Documentação e conclusão | site e animação |

## Teste de carga

O vídeo do teste de carga com HPA (exigido pela página de Load Testing) está em
[Teste de carga e HPA](projeto/load-test.md#video-do-teste-com-hpa).
