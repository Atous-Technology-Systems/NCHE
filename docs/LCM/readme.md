1. Criado o LCM com o promtp + Anexo de todos os docs da V7 (05/07/2025)

```plain
Gere um arquivo CSV com **20 colunas e 150 linhas** extraindo dados do projeto NCHE conforme estrutura abaixo:

### COLUNAS (20):
1. **ID_Registro** (Identificador único sequencial)  
2. **Versao_Arquitetura** (NCHE v6 ou NCHE v7)  
3. **Dimensao_Principal** [Técnica|Comercial|Estratégica|Riscos|Temporal|Validação]  
4. **Subdimensao** (Ex: Gestão Térmica, Yield, TAM, etc.)  
5. **Metrica** (Nome específico da métrica)  
6. **Valor_v6** (Valor numérico ou descritivo na versão v6)  
7. **Valor_v7** (Valor numérico ou descritivo na versão v7)  
8. **Delta_Absoluto** (Diferença numérica: Valor_v7 - Valor_v6)  
9. **Delta_Relativo** (Variação percentual: ((Valor_v7/Valor_v6)-1)*100)  
10. **Unidade_Medida** (%, $, °C, anos, etc.)  
11. **Fonte_Documento** (Nome do documento origem)  
12. **Stakeholder_Relevante** [Executivo|Engenheiro|Investidor|Pesquisador]  
13. **Categoria_Risco** [M3D|Térmico|Variabilidade|Mercado]  
14. **Nivel_Risco_v6** (0-100%)  
15. **Nivel_Risco_v7** (0-100%)  
16. **Mitigacao_Implementada** (Descrição sucinta)  
17. **Status_Evolucao** [✅ Superado|⚠️ Mitigado|▶️ Em progresso]  
18. **Impacto_Projeto** [Baixo|Médio|Alto|Crítico]  
19. **Horizonte_Temporal** (2025, 2028, 2035, 2040+)  
20. **Link_Referencia** (Hyperlink para documento)  

### LINHAS (150):
- **50 linhas** para dimensão técnica (ex: Yield, Temperatura, CV Memristores)  
- **30 linhas** para dimensão comercial (TAM, Custo/Chip, ROI)  
- **20 linhas** para gestão de riscos (evolução e mitigação)  
- **25 linhas** para inovações (Metaplasticidade, Microfluídica, etc.)  
- **25 linhas** para validações (Benchmarks, MTTF, Precisão MNIST)  

### REGRAS DE EXTRAÇÃO:
1. Preencher **todas as 150 linhas** com dados reais do projeto  
2. Calcular automaticamente Deltas (colunas 8-9) quando aplicável  
3. Priorizar dados quantitativos sobre qualitativos  
4. Incluir hyperlinks reais (ex: `[Whitepaper v7](./whitepaper_original_v7.md)`)  
5. Variar stakeholders por linha conforme relevância  
6. Marcar `Status_Evolucao` como ✅ quando:  
   - Redução risco > 50%  
   - Melhoria métrica > 30%  
   - Meta comercial atingida  

### EXEMPLO DE LINHA:

ID_Registro,Versao_Arquitetura,Dimensao_Principal,Subdimensao,Metrica,Valor_v6,Valor_v7,Delta_Absoluto,Delta_Relativo,Unidade_Medida,Fonte_Documento,Stakeholder_Relevante,Categoria_Risco,Nivel_Risco_v6,Nivel_Risco_v7,Mitigacao_Implementada,Status_Evolucao,Impacto_Projeto,Horizonte_Temporal,Link_Referencia
1,NCHE v7,Técnica,Yield,Yield_Produção,45,82,37,82.22,%,"Réplica v7, Sumário v7",Engenheiro,Low Yield,65,20,Auto-reparação + Otimização processo,✅,Crítico,2025,./NCHE_v7_Replica.md


### REQUISITOS ADICIONAIS:
- Delimitador: `;` (ponto-e-vírgula)  
- Encoding: UTF-8  
- Formato datas: YYYY-MM-DD  
- Tratar "N/A" para dados não aplicáveis  
- Incluir cabeçalho na primeira linha

```

2. Solicitei ao LLM o seguinte prompt

```plain
Agora monte o prompt instruindo o LLM que ira ler esse arquivo, detalhando de forma redundante garantindo a compreensão e a leitura adequada, sobre como ele deve entender as colunas e cruzar as linhas como observador, dado que aqui é uma superposição com 150 estados simultaneos 
```

