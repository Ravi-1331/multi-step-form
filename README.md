# [Shadcn/ui x NextJS 15 multistep form](https://multistepform.younesfakallah.fr) &middot; [![Author Ravi](https://img.shields.io/badge/Author-Younès-%3C%3E)](https://younesfakallah.fr/blog)

A multi-step form for Next.js built on top of [shadcn/ui](https://ui.shadcn.com)
complete with desktop and mobile responsiveness.

## Features

- ⚙️ URL state based
- 🎨 @shadcn based
- ♾️ 1 to many step
- 🍳 Easy to use

## Tech/framework used

- Next.js 15
- React Context
- Shadcn/ui
- Tailwind CSS
- TypeScript

## Step 1
npm install

## How to use it ?

Wrap your steps inside `StepProvider`. The order of the steps is determined by
their placement within the StepProvider. Example:

```tsx
"use client";

export default function Page() {
  return (
    <StepProvider>
      <Login />
      <Synchronize />
      <CreateTeam />
    </StepProvider>
  )
}

```

You can control the step flow directly from your step components using
`useStep`.

```tsx
export function Login() {
  const {
    goToNextStep,
    goToPrevStep,
    canGoToNextStep,
    canGoToPrevStep,
    setStep,
    reset,
    currentStep,
  } = useStep();
  return <Button onClick={goToNextStep}>Next step</Button>;
}
```
## project image
![Screenshot 2024-12-24 000514](https://github.com/user-attachments/assets/dac98bfa-474b-4ee8-90a2-f15695463205)

![Screenshot 2024-12-24 000524](https://github.com/user-attachments/assets/16bbd717-42b9-4a35-9c78-a7e62305d34f)

You also have to add some description about your steps inside `headerData` object
you will find it inside `@/components/step-header.tsx`.
