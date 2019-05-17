# http://diaktors.github.io
Diaktors Team - Mastermind Innovation :neckbeard:

Inspiration
> Diactoros (pronunciation: `/dɪʌktɒrɒs/`): an epithet for Hermes, meaning literally, "the messenger."

# I - Write inspiration

```
State Manager (SM) permite que os depuradores diagnostiquem travamentos e bloqueios de aplicativos. Uma cadeia de espera é uma sequência alternada de segmentos e objetos de sincronização; cada thread aguarda o objeto que o segue, que pertence ao segmento subseqüente na cadeia.

Um encadeamento aguarda um objeto de sincronização a partir do momento em que o solicita até que ele seja adquirido. Um bloqueio pertence a um encadeamento a partir do momento em que o encadeamento o adquire, até que ele seja liberado. A propriedade de bloqueio é equivalente ao bloqueio que está aguardando o segmento liberá-lo. Portanto, se o encadeamento 1 aguardar um bloqueio que pertence ao encadeamento 2, será o mesmo que dizer que o encadeamento 1 aguarda o encadeamento 2. O SM atualmente suporta as seguintes primitivas de sincronização:

ALPC
COM
Critical sections
Mutexes
SendMessage

O que é esperado nas operações em processos e encadeamentos?

Para recuperar a cadeia de espera de um ou mais segmentos, crie uma instância do SM usando as funções OpenThreadWaitChainSession e GetThreadWaitChain. As sessões do SM são representadas por um identificador do tipo HSM. As sessões podem ser de natureza síncrona ou assíncrona. As sessões síncronas bloquearão o encadeamento de chamada até que uma cadeia de espera seja recuperada. Sessões síncronas não podem ser canceladas. Sessões assíncronas não bloqueiam o segmento de chamada e podem ser canceladas pelo aplicativo usando a função CloseThreadWaitChainSession. Os resultados de operações assíncronas são disponibilizados por meio de uma função de retorno de chamada WaitChainCallback fornecida pelo aplicativo.

Para sessões assíncronas, o chamador pode especificar um ponteiro para uma estrutura de dados de contexto por meio de GetThreadWaitChain. O mesmo ponteiro é passado para a função de retorno de chamada. Essa estrutura de dados de contexto é definida pelo usuário e opaca para o SM. Ele pode ser usado pelo aplicativo para comunicar o contexto entre uma consulta SM e uma função de retorno de chamada. Uma abordagem comum é passar um identificador de evento por meio dessa estrutura; quando o retorno de chamada é executado, ele sinaliza esse evento e informa algum thread de monitoramento que a consulta foi concluída.

```
