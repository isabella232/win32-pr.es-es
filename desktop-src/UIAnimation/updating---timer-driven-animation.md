---
title: Crear un guion gráfico y agregar transiciones
description: Para crear una animación, una aplicación debe construir un guion gráfico.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- guiones gráficos animación de Windows, crear
- guiones gráficos animación de ventanas, agregar transiciones
- transiciones animación de Windows, crear
- transiciones animación de Windows, agregar a guion gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357515"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="6d8a2-107">Crear un guion gráfico y agregar transiciones</span><span class="sxs-lookup"><span data-stu-id="6d8a2-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="6d8a2-108">Para crear una animación, una aplicación debe construir un guion gráfico.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="6d8a2-109">Información general</span><span class="sxs-lookup"><span data-stu-id="6d8a2-109">Overview</span></span>

<span data-ttu-id="6d8a2-110">Los pasos generales para crear un guión gráfico son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6d8a2-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="6d8a2-111">Crear un guion gráfico</span><span class="sxs-lookup"><span data-stu-id="6d8a2-111">Create a storyboard</span></span>
2.  <span data-ttu-id="6d8a2-112">Crear una o más transiciones</span><span class="sxs-lookup"><span data-stu-id="6d8a2-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="6d8a2-113">Agregue las transiciones al guion gráfico, especificando las variables que animan</span><span class="sxs-lookup"><span data-stu-id="6d8a2-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="6d8a2-114">Se puede crear un guión gráfico vacío mediante el administrador de animaciones.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="6d8a2-115">La aplicación debe rellenar cada guion gráfico con transiciones.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="6d8a2-116">Cada transición especifica cómo cambia una variable de animación única en un intervalo de tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="6d8a2-117">Las transiciones se pueden crear mediante el componente de biblioteca de transición incluido en la animación de Windows.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="6d8a2-118">Como alternativa, una aplicación puede crear sus propias transiciones personalizadas o utilizar una biblioteca de transición de un tercero.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="6d8a2-119">Cuando la aplicación agrega una transición a un guion gráfico, especifica qué variable de animación se animará la transición.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="6d8a2-120">Un guión gráfico puede incluir transiciones en una o varias variables de animación.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="6d8a2-121">Los guiones gráficos más complejos pueden usar fotogramas clave para sincronizar los inicios o finales de las transiciones, o para especificar partes del guion gráfico que se deben repetir (un número fijo de veces o indefinidamente).</span><span class="sxs-lookup"><span data-stu-id="6d8a2-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="6d8a2-122">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d8a2-122">Example Code</span></span>

<span data-ttu-id="6d8a2-123">El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow:: ChangeColor.</span><span class="sxs-lookup"><span data-stu-id="6d8a2-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="6d8a2-124">En este ejemplo se crea el guión gráfico (paso 1) mediante el método [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , se crean las transiciones (paso 2) mediante el método [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) y se agregan las transiciones al guion gráfico (paso 3) mediante el método [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .</span><span class="sxs-lookup"><span data-stu-id="6d8a2-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="6d8a2-125">Paso anterior</span><span class="sxs-lookup"><span data-stu-id="6d8a2-125">Previous Step</span></span>

<span data-ttu-id="6d8a2-126">Antes de comenzar este paso, debe haber completado este paso: [leer los valores de la variable de animación](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="6d8a2-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="6d8a2-127">siguiente paso</span><span class="sxs-lookup"><span data-stu-id="6d8a2-127">Next Step</span></span>

<span data-ttu-id="6d8a2-128">Después de completar este paso, el paso siguiente es [programar un guion gráfico](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="6d8a2-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d8a2-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d8a2-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d8a2-130">**IUIAnimationManager::CreateStoryboard**</span><span class="sxs-lookup"><span data-stu-id="6d8a2-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="6d8a2-131">**IUIAnimationStoryboard::AddTransition**</span><span class="sxs-lookup"><span data-stu-id="6d8a2-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="6d8a2-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span><span class="sxs-lookup"><span data-stu-id="6d8a2-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="6d8a2-133">Información general sobre guiones gráficos</span><span class="sxs-lookup"><span data-stu-id="6d8a2-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




