# JobMatch-ATS

🎯 ATS Job Matcher & Resume BuilderUma aplicação web ATS-Friendly desenvolvida para comparar currículos com descrições de vagas de emprego, destacando lacunas de palavras-chave e gerando uma versão otimizada do currículo sem inventar experiências falsas.📌 

1. Sobre o Projeto e Problema Resolvido muitos profissionais qualificados são descartados em processos seletivos antes mesmo de passarem por uma avaliação humana. O motivo principal é o ATS (Applicant Tracking System), sistema de rastreamento de candidatos que filtra currículos com base na presença e na relevância de palavras-chave extraídas da descrição da vaga. O ATS Job Matcher resolve esse problema ao: Analisar a relevância do currículo em relação à descrição da vaga em tempo real.Mapear palavras-chave encontradas e identificar lacunas vitais para o ranqueamento.Reescrever o currículo em uma versão otimizada para o ATS, aprimorando o tom e o alinhamento das competências reais do candidato.
2. ⚠️ Regra Fundamental de Integridade: A aplicação nunca inventa competências ou experiências fictícias. Ela atua estritamente na melhoria da comunicação e no destaque ético do histórico do candidato.🚀
3. Aplicação em Produção Link da Aplicação:
# https://vagas-projetos.lovable.app/
4. Tecnologias Utilizadas: React, TypeScript, Tailwind CSS, shadcn/ui, Lucide Icons e Lovable Engine.🤖
5. Mega Prompt UtilizadoPara criar a primeira versão completa da aplicação no modo Build/Plan do Lovable 
   
# Theme & Palette
- Target Audience: Job seekers looking to optimize their resumes.
- Color Palette: Clean professional tech theme.
  - Primary: Deep Indigo / Slate Blue
  - Accent: Emerald Green (for matches and scores)
  - Background: Neutral Light Grey / Soft Off-White
  - Warnings/Gaps: Amber / Coral Red

# Layout & Screen Structure
1. **Hero Header**: Title, short explanation of what ATS is, and an ethical promise: "We improve how you present your story. We never invent experiences you don't have."
2. **Main Workspace (2 Column Split)**:
   - *Left Panel*: Textarea to paste Job Description (Vaga de Emprego) and Textarea to paste User's Resume (Currículo Atual).
   - *Right Panel / Result Section*:
     - **Match Percentage Indicator** (Score Progress Bar/Circle).
     - **Keywords Badge Grid**: Keywords Found (Green) vs. Missing Keywords (Red/Amber).
     - **ATS-Optimized Resume Editor/Preview**: A clear, beautifully formatted preview of the rewritten resume.
3. **Export Actions**: Action buttons to copy formatted text or export/download as PDF.

# Core Logic Flow
1. User pastes both texts and clicks "Analisar e Otimizar".
2. System extracts top relevant skill keywords from the job description.
3. System checks for presence of those keywords in the candidate's resume.
4. System calculates a Match Score (0-100%).
5. System generates an updated version of the resume that integrates missing keywords ethically where appropriate based on existing text context.

# UI Components (shadcn/ui)
- Use `Button`, `Textarea`, `Card`, `Badge`, `Progress`, `Tabs`, and `Toast` notifications for copy actions.
🔄 Evolução e Mudanças no Prompt InitialVersão Inicial: Focava apenas na comparação das palavras e cálculo do score.Refinamento: Foi adicionada a instrução explícita de regra de negócio no topo ("Não inventar experiências"), além da necessidade de incluir opções de exportação do resultado.🔄
4. Fluxo de Análise da Aplicação[ Cole a Vaga ] ───┐
                   ├──► [ Análise de Palavras-Chave ] ──► [ Cálculo de Match % ]
[ Cole o Currículo ] ──┘          │
                                  ├──► [ Destaque de Lacunas (Faltantes vs Encontradas) ]
                                  │
                                  └──► [ Geração de Currículo Reescrito & Exportação ]
Entrada de Dados: O usuário cola a vaga pretendida e seu currículo atual nos campos de texto.Extração e Processamento: A aplicação mapeia as competências técnicas, soft skills e requisitos descritos na vaga. Cruzamento de Informações: Identifica quais requisitos já constam no currículo do candidato e quais estão ausentes. Métricas e Diagnóstico: Exibe uma pontuação de aderência (Match Score %) e categoriza as palavras-chave com badges visuais.Ajuste Ético: A IA reescreve as seções do currículo ajustando o vocabulário para sincronizar com os termos exatos do ATS.🛠️
5. Refinamentos e Ajustes Pós-GeraçãoApós a geração inicial pelo Lovable, foram solicitadas as seguintes alterações via chat iterativo: Implementação do Exportador de PDF / Texto:Solicitação: "Adicione um botão para exportar a versão otimizada em arquivo PDF e a opção de copiar o texto direto para a área de transferência. "Motivo: Garantir que a ferramenta entregue utilidade imediata ao candidato. Inclusão da Trava Ética Visível na Interface: Solicitação: "Adicione um card de alerta no topo reforçando que o sistema melhora o posicionamento mas não inventa dados. "Motivo: Garantir clareza e transparência no uso de inteligência artificial na carreira. Melhoria na Responsividade Mobile: Solicitação: "Ajuste a visualização das duas colunas para empilhar em telas de celular. "Motivo: Melhorar a experiência em dispositivos móveis.📸

Este projeto foi desenvolvido pela Aline para fins educacionais e de portfólio no desafio da DIO com Lovable
