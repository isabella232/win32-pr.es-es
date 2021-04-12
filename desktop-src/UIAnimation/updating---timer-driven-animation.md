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
# <a name="create-a-storyboard-and-add-transitions"></a>Crear un guion gráfico y agregar transiciones

Para crear una animación, una aplicación debe construir un guion gráfico.

## <a name="overview"></a>Información general

Los pasos generales para crear un guión gráfico son los siguientes:

1.  Crear un guion gráfico
2.  Crear una o más transiciones
3.  Agregue las transiciones al guion gráfico, especificando las variables que animan

Se puede crear un guión gráfico vacío mediante el administrador de animaciones. La aplicación debe rellenar cada guion gráfico con transiciones. Cada transición especifica cómo cambia una variable de animación única en un intervalo de tiempo determinado. Las transiciones se pueden crear mediante el componente de biblioteca de transición incluido en la animación de Windows. Como alternativa, una aplicación puede crear sus propias transiciones personalizadas o utilizar una biblioteca de transición de un tercero. Cuando la aplicación agrega una transición a un guion gráfico, especifica qué variable de animación se animará la transición.

Un guión gráfico puede incluir transiciones en una o varias variables de animación. Los guiones gráficos más complejos pueden usar fotogramas clave para sincronizar los inicios o finales de las transiciones, o para especificar partes del guion gráfico que se deben repetir (un número fijo de veces o indefinidamente).

## <a name="example-code"></a>Código de ejemplo

El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplo de animación [controlada por temporizador](timer-driven-animation-sample.md); Vea el método CMainWindow:: ChangeColor. En este ejemplo se crea el guión gráfico (paso 1) mediante el método [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , se crean las transiciones (paso 2) mediante el método [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) y se agregan las transiciones al guion gráfico (paso 3) mediante el método [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .


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



## <a name="previous-step"></a>Paso anterior

Antes de comenzar este paso, debe haber completado este paso: [leer los valores de la variable de animación](updating---application-driven-animation.md).

## <a name="next-step"></a>siguiente paso

Después de completar este paso, el paso siguiente es [programar un guion gráfico](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Información general sobre guiones gráficos](storyboard-construction.md)
</dt> </dl>

 

 




