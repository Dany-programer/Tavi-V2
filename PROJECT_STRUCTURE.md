
# Estructura del Proyecto TAVI

A continuación se detalla la estructura de carpetas y archivos del proyecto Laboratorio EduPlay (TAVI).

```
.
├── .env
├── .vscode/
│   └── settings.json
├── README.md
├── components.json
├── next.config.ts
├── package.json
├── public/
│   └── imagene/
│       ├── Logo AVI.svg
│       ├── Logo Edutlan 2024.svg
│       ├── Logo LIEMAV.svg
│       ├── Logo-universidad.png
│       └── logo-cool.png
├── src/
│   ├── ai/
│   │   ├── dev.ts
│   │   ├── flows/
│   │   │   ├── generate-adaptive-challenges.ts
│   │   │   ├── generate-catcher-game-flow.ts
│   │   │   ├── generate-construction-game-flow.ts
│   │   │   ├── generate-creative-scripts-flow.ts
│   │   │   ├── generate-definition-challenge-flow.ts
│   │   │   ├── generate-explanatory-script-flow.ts
│   │   │   ├── generate-html-simulator.ts
│   │   │   ├── generate-memory-game-flow.ts
│   │   │   ├── generate-podcast-script-flow.ts
│   │   │   ├── generate-quiz-questions.ts
│   │   │   ├── generate-scenario-games.ts
│   │   │   ├── generate-text-resource.ts
│   │   │   ├── generate-tts-audio-flow.ts
│   │   │   ├── generate-visual-content-flow.ts
│   │   │   ├── generate-word-puzzle-flow.ts
│   │   │   └── provide-ai-powered-feedback.ts
│   │   └── genkit.ts
│   ├── app/
│   │   ├── (app)/
│   │   │   ├── challenge/
│   │   │   │   └── page.tsx
│   │   │   ├── create/
│   │   │   │   └── simulator/
│   │   │   │       ├── actions.ts
│   │   │   │       ├── components/
│   │   │   │       │   ├── CatcherGamePlayer.tsx
│   │   │   │       │   ├── ConstructionGamePlayer.tsx
│   │   │   │       │   ├── DefinitionChallengePlayer.tsx
│   │   │   │       │   ├── MemoryGamePlayer.tsx
│   │   │   │       │   └── WordPuzzlePlayer.tsx
│   │   │   │       └── page.tsx
│   │   │   ├── explorer/
│   │   │   │   └── page.tsx
│   │   │   ├── home/
│   │   │   │   └── page.tsx
│   │   │   ├── layout.tsx
│   │   │   ├── play/
│   │   │   │   ├── auditory/
│   │   │   │   │   ├── actions.ts
│   │   │   │   │   └── page.tsx
│   │   │   │   ├── page.tsx
│   │   │   │   ├── quiz/
│   │   │   │   │   ├── actions.ts
│   │   │   │   │   ├── page.tsx
│   │   │   │   │   └── quiz-client-page.tsx
│   │   │   │   ├── text/
│   │   │   │   │   ├── actions.ts
│   │   │   │   │   └── page.tsx
│   │   │   │   └── visual/
│   │   │   │       ├── actions.ts
│   │   │   │       ├── components/
│   │   │   │       │   ├── OutputDisplay.tsx
│   │   │   │       │   └── forms/
│   │   │   │       │       ├── ConceptIllustrationForm.tsx
│   │   │   │       │       ├── DataVisualizationForm.tsx
│   │   │   │       │       ├── ImageGenerationForm.tsx
│   │   │   │       │       └── InfoOrganizationForm.tsx
│   │   │   │       └── page.tsx
│   │   │   ├── profile/
│   │   │   │   └── page.tsx
│   │   │   ├── results/
│   │   │   │   ├── actions.ts
│   │   │   │   └── page.tsx
│   │   │   └── settings/
│   │   │       └── page.tsx
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   ├── login/
│   │   │   └── page.tsx
│   │   ├── page.tsx
│   │   ├── signup/
│   │   │   └── page.tsx
│   │   └── vark-test/
│   │       └── page.tsx
│   ├── components/
│   │   ├── content-card.tsx
│   │   ├── navigation/
│   │   │   ├── ProtectedRoute.tsx
│   │   │   ├── main-nav.tsx
│   │   │   └── sidebar-header-toggle.tsx
│   │   └── ui/
│   │       ├── accordion.tsx
│   │       ├── alert-dialog.tsx
│   │       ├── alert.tsx
│   │       ├── avatar.tsx
│   │       ├── badge.tsx
│   │       ├── button.tsx
│   │       ├── calendar.tsx
│   │       ├── card.tsx
│   │       ├── chart.tsx
│   │       ├── checkbox.tsx
│   │       ├── dialog.tsx
│   │       ├── dropdown-menu.tsx
│   │       ├── form.tsx
│   │       ├── input.tsx
│   │       ├── label.tsx
│   │       ├── menubar.tsx
│   │       ├── popover.tsx
│   │       ├── progress.tsx
│   │       ├── radio-group.tsx
│   │       ├── scroll-area.tsx
│   │       ├── select.tsx
│   │       ├── separator.tsx
│   │       ├── sheet.tsx
│   │       ├── sidebar.tsx
│   │       ├── skeleton.tsx
│   │       ├── slider.tsx
│   │       ├── switch.tsx
│   │       ├── table.tsx
│   │       ├── tabs.tsx
│   │       ├── textarea.tsx
│   │       ├── toast.tsx
│   │       └── toaster.tsx
│   ├── context/
│   │   └── AuthContext.tsx
│   ├── hooks/
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   └── lib/
│       ├── auditory-constants.ts
│       ├── auditory-types.ts
│       ├── firebase.ts
│       ├── kinesthetic-types.ts
│       ├── text-resource-enums.ts
│       ├── text-resource-labels.ts
│       ├── utils.ts
│       ├── visual-constants.ts
│       └── visual-types.ts
├── tailwind.config.ts
└── tsconfig.json
```
