<!--
1º Projeto de Linguagens de Programação I 2018/2019 (c) by Nuno Fachada

1º Projeto de Linguagens de Programação I 2018/2019 is licensed under a
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-nc-sa/4.0/>.
-->

# 1º Projeto de Linguagens de Programação I 2018/2019

## Descrição do problema

Os alunos devem implementar o jogo *18 Ghosts* \[[1][ref1]\] para dois
jogadores, as regras do qual estão disponíveis [aqui][regras].

O jogo deve ser desenvolvido com a linguagem C# \[[2][ref2],[3][ref3]\], mais
especificamente como uma aplicação de consola **.NET Core**, devendo também
funcionar e ser testado em Mac e/ou Linux (devem ser evitadas classes ou
métodos específicos para Windows).

Não serão avaliados projetos desenvolvidos noutras _frameworks_, como por
exemplo, .NET Framework, Unity, Windows Forms, etc.

Os grupos podem ter entre 2 a 3 elementos.

<a name="orgclasses"></a>

## Organização do projeto e estrutura de classes

O projeto deve estar devidamente organizado, fazendo uso de classes e
enumerações. Cada classe/enumeração deve ser colocada num ficheiro com o mesmo
nome. Por exemplo, uma classe chamada `Player` deve ser colocada no ficheiro
`Player.cs`. A estrutura de classes deve ser bem pensada e organizada de uma
forma lógica, e [cada classe deve ter uma responsabilidade específica e bem
definida][SRP].

O exercício proposto no capítulo 20 do livro da disciplina [\[2\]](#ref2)
constitui um bom ponto de partida para desenhar uma estrutura de classes
adequada para este projeto.

Adicionalmente, a documentação da classe [`Console`] explica como usar cores na consola, bem como posicionar carateres em locais específicos. O uso de
carateres [Unicode] poderá também facilitar a visualização do jogo.

<a name="objetivos"></a>

## Objetivos e critério de avaliação

Este projeto tem os seguintes objetivos:

* **O1** - Jogo deve funcionar de acordo com as [regras]. Podem assumir que o
  jogador sabe as regras, mas deve existir uma legenda explicando o que
  significa cada caráter (fantasmas, portais, etc).
* **O2** - Projeto e código bem organizados, nomeadamente:
  * Estrutura de classes bem pensada (ver secção [Organização do projeto e
    estrutura de classes](#orgclasses)).
  * Código devidamente comentado e indentado.
  * Inexistência de código "morto", que não faz nada, como por exemplo
    variáveis, propriedades ou métodos nunca usados.
  * Projeto compila e executa sem erros e/ou *warnings*.
* **O3** - Projeto adequadamente documentado com
  [comentários de documentação XML][XML]. A documentação gerada em formato HTML
  ou CHM com [Doxygen], [Sandcastle] ou ferramenta similar \[[4][ref4]\], deve
  estar incluída no ZIP do projeto, mas **não** integrada no repositório Git.
* **O4** - Repositório Git deve refletir boa utilização do mesmo, com *commits*
  de todos os elementos do grupo e mensagens de *commit* que sigam as melhores
  práticas para o efeito (como indicado
  [aqui](https://chris.beams.io/posts/git-commit/),
  [aqui](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53),
  [aqui](https://github.com/erlang/otp/wiki/writing-good-commit-messages) e
  [aqui](https://stackoverflow.com/questions/2290016/git-commit-messages-50-72-formatting)).
  Quaisquer *assets* binários, tais como imagens para uso no relatório,
  por exemplo, devem ser integrados no repositório em modo Git LFS.
* **O5** - Relatório em formato [Markdown] (ficheiro `README.md`), organizado
  da seguinte forma:
  * Título do projeto.
  * Nome dos autores (primeiro e último) e respetivos números de aluno.
  * Indicação do repositório público Git utilizado. Esta indicação é opcional,
    pois podem preferir desenvolver o projeto num repositório privado.
  * Informação de quem fez o quê no projeto. Esta informação é **obrigatória**
    e deve refletir os *commits* feitos no Git.
  * Descrição da solução:
    * Arquitetura da solução, com breve explicação de como o programa foi
      organizado e algoritmos implementados.
    * Um diagrama UML de classes simples (i.e., sem indicação dos membros da
      classe) descrevendo a estrutura de classes.
    * Um fluxograma mostrando o funcionamento do programa.
    * Conclusões e matéria aprendida.
    * Referências, incluindo trocas de ideias com colegas, código aberto
      reutilizado ou no qual se basearam (e.g., do StackOverflow ou do GitHub)
      e bibliotecas de terceiros utilizadas. Devem ser o mais detalhados
      possível.
  * Nota adicionais sobre o relatório:
    * O relatório deve ser simples e breve, com informação mínima e suficiente
      para que seja possível ter uma boa ideia do que foi feito.
    * Atenção aos erros ortográficos, pois serão tidos em conta na nota final.
    * Atenção à formatação [Markdown], pois será tida em conta na nota final.
    * Se usarem o [Visual Studio Code] para fazer o relatório, façam uso da
      [extensão de correção ortográfica][VSCodeSpellCheck]
      (e o seu dicionário de [Português][VSCodeSpellCheckPT]) e [extensões para
      edição de Markdown][VSCodeMarkdown].

O projeto tem um peso de 3 valores na nota final da disciplina e será avaliado
de forma qualitativa. Isto significa que todos os objetivos têm de ser
parcialmente ou totalmente cumpridos. A cada objetivo, **O1** a **O5**, será
atribuída uma nota entre 0 e 1. A nota do projeto será dada pela seguinte
fórmula:

`N = 3 x O1 x O2 x O3 x O4 x O5 x D`

Em que *D* corresponde à nota da discussão e percentagem equitativa de
realização do projeto, também entre 0 e 1. Isto significa que se os alunos
ignorarem completamente um dos objetivos, não tenham feito nada no projeto ou
não comparecerem na discussão, a nota final será zero.

## Entrega

O projeto deve ser entregue por **grupos de 2 ou 3 alunos** via Moodle até às
**23h de 9 de maio de 2019**. Deve ser submetido um ficheiro `zip` com os
seguintes conteúdos:

* Solução ou projeto Visual Studio com implementação do jogo.
* Pasta escondida `.git` com o repositório Git local do projeto.
* Documentação HTML ou CHM gerada com [Doxygen], [Sandcastle] ou ferramenta
  similar \[[4][ref4]\].
* Ficheiro `README.md` contendo o relatório do projeto em formato [Markdown].
* Ficheiros de imagem contendo o fluxograma e o diagrama UML de classes.
  Estes ficheiros podem ser incluídos no repositório em modo Git LFS.

## Honestidade académica

Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de
honestidade académica. Isto significa que cada ideia que não seja do
aluno deve ser claramente indicada, com devida referência ao respetivo
autor. O não cumprimento desta regra constitui plágio.

O plágio inclui a utilização de ideias, código ou conjuntos de soluções
de outros alunos ou indivíduos, ou quaisquer outras fontes para além
dos textos de apoio à disciplina, sem dar o respetivo crédito a essas
fontes. Os alunos são encorajados a discutir os problemas com outros
alunos e devem mencionar essa discussão quando submetem os projetos.
Essa menção **não** influenciará a nota. Os alunos não deverão, no
entanto, copiar códigos, documentação e relatórios de outros alunos, ou dar os
seus próprios códigos, documentação e relatórios a outros em qualquer
circunstância. De facto, não devem sequer deixar códigos, documentação e
relatórios em computadores de uso partilhado.

Nesta disciplina, a desonestidade académica é considerada fraude, com
todas as consequências legais que daí advêm. Qualquer fraude terá como
consequência imediata a anulação dos projetos de todos os alunos envolvidos
(incluindo os que possibilitaram a ocorrência). Qualquer suspeita de
desonestidade académica será relatada aos órgãos superiores da escola
para possível instauração de um processo disciplinar. Este poderá
resultar em reprovação à disciplina, reprovação de ano ou mesmo suspensão
temporária ou definitiva da ULHT.

*Texto adaptado da disciplina de [Algoritmos e
Estruturas de Dados][aed] do [Instituto Superior Técnico][ist]*

## Referências

* <a name="ref1">\[1\]</a> **18 Ghosts** (2010). Retrieved from
  <https://boardgamegeek.com/boardgame/70116/18-ghosts>.
* <a name="ref2">\[2\]</a> Whitaker, R. B. (2016). **The C# Player's Guide**
  (3rd Edition). Starbound Software.
* <a name="ref3">\[3\]</a> Albahari, J. (2017). **C# 7.0 in a Nutshell**.
  O’Reilly Media.
* <a name="ref4">\[4\]</a> Dorsey, T. (2017). **Doing Visual Studio and .NET
  Code Documentation Right**. Visual Studio Magazine. Retrieved from
  <https://visualstudiomagazine.com/articles/2017/02/21/vs-dotnet-code-documentation-tools-roundup.aspx>.

## Licenças

Este enunciado é disponibilizados através da licença [CC BY-NC-SA 4.0][].

## Metadados

* Autor: [Nuno Fachada][]
* Curso:  [Licenciatura em Videojogos][lamv]
* Instituição: [Universidade Lusófona de Humanidades e Tecnologias][ULHT]

[ref1]:#ref1
[ref2]:#ref2
[ref3]:#ref3
[ref4]:#ref4
[ref5]:#ref5
[regras]:https://secure.grupolusofona.pt/ulht/moodle/pluginfile.php/555001/mod_assign/introattachment/0/18GHOSTS_EN_r1.pdf?forcedownload=1
[CC BY-NC-SA 4.0]:https://creativecommons.org/licenses/by-nc-sa/4.0/
[lamv]:https://www.ulusofona.pt/licenciatura/videojogos
[Nuno Fachada]:https://github.com/fakenmc
[ULHT]:https://www.ulusofona.pt/
[aed]:https://fenix.tecnico.ulisboa.pt/disciplinas/AED-2/2009-2010/2-semestre/honestidade-academica
[ist]:https://tecnico.ulisboa.pt/pt/
[Markdown]:https://guides.github.com/features/mastering-markdown/
[Doxygen]:https://www.stack.nl/~dimitri/doxygen/
[Sandcastle]:https://github.com/EWSoftware/SHFB
[KISS]:https://en.wikipedia.org/wiki/KISS_principle
[XML]:https://docs.microsoft.com/dotnet/csharp/codedoc
[SRP]:https://en.wikipedia.org/wiki/Single_responsibility_principle
[`Console`]:https://docs.microsoft.com/dotnet/api/system.console
[Unicode]:https://unicode-table.com/
[Visual Studio Code]:https://code.visualstudio.com/
[VSCodeMarkdown]:https://code.visualstudio.com/docs/languages/markdown
[VSCodeSpellCheck]:https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker
[VSCodeSpellCheckPT]:https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-portuguese
