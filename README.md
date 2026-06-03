# IgrejaTV - Sistema de TV Corporativa para Igrejas

Plataforma completa de Digital Signage desenvolvida especialmente para igrejas.  
Exibição automática de anúncios, cultos, eventos, versículos e comunicados em tempo real.

**Tecnologias:** Next.js 15 + NestJS + PostgreSQL + Socket.IO + AWS S3

## Estrutura Completa do Repositório ## 
igreja-tv-system/
├── backend/                          # NestJS - API
├── frontend/                         # Next.js 15 - Interface
├── docker-compose.yml
├── .gitignore
├── README.md
└── LICENSE

## 1. Backend
backend/
├── src/
│   ├── auth/
│   │   ├── auth.controller.ts
│   │   ├── auth.service.ts
│   │   ├── auth.module.ts
│   │   ├── jwt.strategy.ts
│   │   └── dto/
│   │       ├── login.dto.ts
│   │       └── register.dto.ts
│   │
│   ├── content/
│   │   ├── content.controller.ts
│   │   ├── content.service.ts
│   │   ├── content.module.ts
│   │   ├── content.entity.ts
│   │   └── dto/
│   │       ├── create-content.dto.ts
│   │       └── update-content.dto.ts
│   │
│   ├── playlist/
│   │   ├── playlist.controller.ts
│   │   ├── playlist.service.ts
│   │   ├── playlist.module.ts
│   │   ├── playlist.entity.ts
│   │   └── dto/
│   │
│   ├── screen/
│   │   ├── screen.controller.ts
│   │   ├── screen.service.ts
│   │   ├── screen.module.ts
│   │   └── screen.entity.ts
│   │
│   ├── socket/
│   │   ├── socket.gateway.ts
│   │   └── socket.module.ts
│   │
│   ├── church/
│   │   ├── church.entity.ts
│   │   └── church.module.ts
│   │
│   ├── common/
│   │   ├── filters/
│   │   └── interceptors/
│   │
│   ├── app.module.ts
│   └── main.ts
│
├── .env.example
├── nest-cli.json
├── tsconfig.json
├── package.json
└── README.md

## 2. Frontend
frontend/
├── app/
│   ├── admin/
│   │   ├── layout.tsx
│   │   ├── dashboard/
│   │   │   └── page.tsx
│   │   ├── contents/
│   │   │   ├── page.tsx
│   │   │   └── new/
│   │   │       └── page.tsx
│   │   ├── playlists/
│   │   │   └── page.tsx
│   │   ├── screens/
│   │   │   └── page.tsx
│   │   └── schedule/
│   │       └── page.tsx
│   │
│   ├── tv/
│   │   └── [screenId]/
│   │       └── page.tsx                 # ← Tela principal da TV
│   │
│   ├── api/
│   │   └── contents/
│   │       └── route.ts                 # Route Handlers (opcional)
│   │
│   ├── globals.css
│   ├── layout.tsx
│   └── page.tsx                         # Página inicial (landing)
│
├── components/
│   ├── admin/
│   │   ├── Sidebar.tsx
│   │   ├── ContentCard.tsx
│   │   ├── ContentForm.tsx
│   │   ├── PlaylistBuilder.tsx          # Drag and Drop
│   │   └── ScreenCard.tsx
│   │
│   ├── tv/
│   │   ├── MainArea.tsx
│   │   ├── SideBar.tsx
│   │   ├── FooterBar.tsx
│   │   └── CultoMode.tsx
│   │
│   └── ui/                              # Componentes reutilizáveis
│       ├── Button.tsx
│       ├── Card.tsx
│       └── Modal.tsx
│
├── lib/
│   ├── api.ts
│   ├── socket.ts
│   └── utils.ts
│
├── public/
│   ├── images/
│   │   └── logo-igreja.png
│   └── icons/
│
├── .env.local
├── next.config.mjs
├── tailwind.config.ts
├── tsconfig.json
├── package.json
└── README.md

