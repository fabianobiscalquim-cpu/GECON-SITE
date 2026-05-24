# Histórico e Contexto do Projeto: Gecon Condomínios

Este documento contém o resumo de todas as decisões, códigos e estilos definidos na nossa sessão. Você pode colar este arquivo inteiro em qualquer outra Inteligência Artificial (ChatGPT, Claude, Cursor, etc.) para que ela continue o trabalho exatamente do ponto em que paramos, sem perder nenhuma configuração de design.

---

## 1. O Objetivo do Projeto
- **Projeto:** Site Institucional da Gecon Condomínios (Unidade São Paulo).
- **Estilo Exigido:** "High-End", nível de startups de tecnologia premium (inspirado em referências como Stripe e OpenAI). 
- **O que evitar:** O site NÃO pode parecer um site padrão/comum de administradora de condomínios. As coisas não podem ter um aspecto turvo ou "sujo". Deve ser puramente limpo, minimalista e altamente tecnológico.

## 2. O Design System & Estética (Regras de Ouro)
A próxima IA deve obrigatoriamente seguir estas regras ao criar novos componentes:
1. **Liquid Glassmorphism:** O estilo visual base são painéis de "vidro escuro" com desfoque de fundo elevado (`backdrop-blur-xl`). O fundo dos cards geralmente é `bg-[#050a14]/60`.
2. **Luzes e Glows:** Componentes interativos recebem luzes radiantes (ex: `bg-[#007bff] blur-[60px] opacity-20`) para criar um efeito de reflexo de led por trás do vidro.
3. **Cores Principais:** 
   - Fundo da página: `bg-cream` (Creme/Branco suave).
   - Vidros escuros: `#050a14`.
   - Verde Institucional Gecon: `#09492C` (Usado para glows, textos de destaque e botões).
4. **Tipografia:** Uso do TailwindCSS. Fontes de título ganham `tracking-tight` e tags/pequenos textos ganham `tracking-widest` e `uppercase` para um tom luxuoso.
5. **Máscaras de Borda:** Usamos máscaras CSS complexas (`mask-composite`) para gerar bordas de 1px com gradientes super finos e luminosos ao invés de bordas sólidas.

## 3. O Que Já Foi Feito (Status Atual do index.html)
- **Navegação (Header):** Menu translúcido fixo no topo. O botão de "Solicite Orçamento" recebeu uma textura de ruído (noise texture em SVG) que dá um aspecto tátil ao verde da Gecon.
- **Hero Section (Dobra Inicial):**
  - Fundo com foto realista de prédio imersivo coberta com gradiente transparente.
  - Tipografia massiva ("GECON Condomínios") alinhada à esquerda, baseada na linha inferior.
  - Título secundário de impacto: *"Aqui você tem tudo que precisa, em um só lugar."*
- **Animação 3D de Cards (Stack de Serviços):** 
  - Do lado direito, ao invés de um loop lateral, construímos um baralho 3D animado usando CSS puro (`@keyframes stackCycle`).
  - 4 cards se alternam vindo para frente e indo para o final da fila (Administração, Mão de Obra, Portaria, Torre de Segurança).
  - Dentro desses cards, as fotos foram aplicadas com `mix-blend-overlay` e `opacity-30` garantindo que o vidro continue limpo, mas mostrando a silhueta da fotografia por baixo.

## 4. O Que Fazer Agora (Próximos Passos)
A partir de agora, o foco é construir o restante do site descendo a página:
1. **Seção "Diferenciais / Sobre":** Construir um layout "Bento Box" (grid de blocos de vidro de tamanhos variados que se encaixam perfeitamente).
2. **Seção "App Gecon":** Apresentar a tecnologia móvel da empresa com um visual estilo "Apresentação da Apple".
3. **Seção de Contato/Rodapé:** Formulário *clean* ou chamada direta para WhatsApp, fechando o site com alto nível de requinte.

---
**Instrução para a nova IA:** 
*Leia o arquivo `index.html` atual da pasta e continue a construção da seção "Diferenciais" (logo abaixo da `section` do Hero), aplicando fielmente o Design System listado acima.*
