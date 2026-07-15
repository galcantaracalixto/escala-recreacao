Escala de Horários — Equipe de Recreação

Página única em HTML/CSS/JS que exibe a escala de horários da equipe de recreação de forma visual, organizada por dia e por recreador.

Contexto

Antes desse projeto, a escala era controlada em várias planilhas Excel separadas, uma por mês/equipe, atualizadas manualmente. Isso trazia alguns problemas no dia a dia:


Informação espalhada em arquivos diferentes, sem um formato único;
Difícil de visualizar rapidamente "quem trabalha hoje e em que horário";
Sem distinção visual clara entre folga, carga cheia, 4h, compensação e férias;
Dependência do Excel instalado para simplesmente consultar a escala.


Para resolver isso, migrei os dados das planilhas para um único arquivo index.html, autocontido, e publiquei o projeto no Netlify, para que a equipe possa consultar a escala direto pelo navegador, sem precisar de Excel nem de arquivos locais.

O que essa solução faz


Mostra a escala do mês inteiro, com destaque para o dia atual;
Para cada dia, lista os 5 recreadores e seu status (horário de trabalho, folga, 4h, compensação ou férias);
Usa cores e ícones para diferenciar rapidamente cada tipo de status;
Interface pensada para leitura rápida, sem precisar abrir planilha nenhuma.


Como usar

Basta acessar o link publicado (hospedado no Netlify): [seu link aqui]

Não precisa instalar nada, baixar arquivo ou ter o Excel — funciona direto no navegador, inclusive pelo celular. Só a fonte do Google Fonts é carregada online; sem conexão, a página funciona normalmente com uma fonte padrão do sistema.


Opcional, caso alguém queira rodar localmente para desenvolvimento: basta abrir o arquivo index.html em qualquer navegador (Chrome, Edge, Firefox etc.).



Estrutura do arquivo

Tudo está em um único arquivo index.html, dividido em três partes:


CSS (dentro de <style>): visual da página; cores, layout, tipografia;
HTML: estrutura da página (cabeçalho, legenda, painel do dia);
JavaScript (dentro de <script>): dados da escala (NAMES, HOURS, entradas de cada dia) e a lógica que monta o painel do dia dinamicamente.


Atualizando a escala

Os dados de cada mês ficam direto no JavaScript, em constantes como NAMES (nomes dos recreadores) e nas entradas de cada dia (horário e tipo: off, full, comp, ferias, reduced).


Para quem consulta a escala: só acessar o link do Netlify, não precisa editar nada.
Para quem atualiza a escala: edita esses valores manualmente no index.html (não existe banco de dados ou planilha por trás) e faz o deploy novamente no Netlify (arrastando a pasta ou via Git, dependendo de como o projeto está configurado).


Possíveis próximos passos


Gerar a escala de meses futuros automaticamente a partir de uma planilha ou formulário;
Adicionar exportação em PDF;
Adicionar filtro por recreador.
