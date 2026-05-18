# shadcn/ui como Design System no Claude Projects

Guia para criar e subir o shadcn/ui do zero como design system no Claude Projects.

---

## Pré-requisitos

- [Node.js](https://nodejs.org/) instalado na sua máquina

---

## Passo 1 — Criar o projeto base

```bash
npx create-next-app@latest meu-design-system
cd meu-design-system
```

---

## Passo 2 — Instalar o shadcn

```bash
npx shadcn@latest init
```

---

## Passo 3 — Adicionar os componentes

Adicione os componentes que você quer usar:

```bash
npx shadcn@latest add button card input badge dialog table form select
```

Ou adicione todos de uma vez:

```bash
npx shadcn@latest add --all
```

---

## Passo 4 — Subir no Claude Projects

No campo **"Link code from your computer"**, arraste as seguintes pastas e arquivos:

```
├── components/ui/     ← todos os componentes gerados pelo shadcn
├── lib/utils.ts       ← helper cn()
├── tailwind.config.ts ← configuração do tema
└── app/globals.css    ← CSS variables do shadcn (cores, bordas, etc.)
```

---

## Passo 5 — Configurar as notas do projeto

No campo **"Any other notes"**, adicione:

> "Design system baseado em shadcn/ui com Tailwind CSS. Use sempre os componentes de `components/ui`. Siga as CSS variables definidas em `globals.css` para cores e tipografia."

---

## Estrutura de arquivos após o setup

```
meu-design-system/
├── app/
│   └── globals.css          ← CSS variables do tema
├── components/
│   └── ui/
│       ├── button.tsx
│       ├── card.tsx
│       ├── input.tsx
│       └── ...              ← demais componentes instalados
├── lib/
│   └── utils.ts             ← função cn() para classes condicionais
└── tailwind.config.ts       ← configuração do Tailwind com tema shadcn
```

---

## Tempo estimado

⏱ Todo o processo leva aproximadamente **5 minutos**.