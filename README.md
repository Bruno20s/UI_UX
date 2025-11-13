# UI_UX

NOTAÇÃO DE GRAFO DE FLUXO;
[1] Início do método
[2] Criação da conexão com o banco
[3] Montagem da consulta SQL
[4] Bloco try-catch de execução
[5] Execução da query
[6] Estrutura condicional if(resultado.next())
[7] Caminho com login válido
[8] Caminho com login inválido
[9] Retorno final
[10] Captura de exceção (erro durante execução)

COMPLEXIDADE CICLOMÁTICA;

Método conectarBD():
Pontos de Decisão(P):  
catch (Linha 15): 1 ponto de decisão (ramificação de exceção).
Cálculo: P + 1 = 2

Método verificarUsuario():
Pontos de Decisão(P):  
if(rs.next()) (Linha 29): 1 ponto de decisão (ramificação de sucesso/falha na busca).
  
catch (Linha 32): 1 ponto de decisão (ramificação de exceção).
Cálculo: P + 1 = 3

Complexidade Ciclomática Total da Classe User: 2+3=5


CAMINHOS BÁSICOS;

Caminhos Básicos para conectarBD(): 2
Sucesso: Conexão estabelecida sem exceções (try completo).

Falha: Ocorre exceção durante a conexão (try falha e desvia para catch).

Caminhos Básicos para verificarUsuario(): 3
Sucesso na Busca: Execução sem exceção, e o usuário é encontrado (rs.next() retorna true).

Falha na Busca: Execução sem exceção, mas o usuário não é encontrado (rs.next() retorna false).

Falha na Execução: Ocorre exceção durante a consulta ou conexão (try falha e desvia para catch).
