---
title: Programar un guión gráfico
description: Una vez creado un guión gráfico, lo programa el administrador de animaciones.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- storyboards Windows Animation ,scheduling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008175"
---
# <a name="schedule-a-storyboard"></a>Programar un guión gráfico

Una vez creado un guión gráfico, lo programa el administrador de animaciones.

## <a name="overview"></a>Información general

De forma predeterminada, cada guión gráfico se inicia inmediatamente cuando se programa. Esto significa que cuando un guión gráfico empieza a animar una o varias variables, puede interrumpir cualquier otro guión gráfico que anima esas mismas variables. Sin embargo, una aplicación puede especificar otros comportamientos mediante la determinación de la prioridad relativa entre guiones gráficos.

Una vez programado un guión gráfico, ya no se puede modificar. Sin embargo, una vez que se ha quitado un guión gráfico de la programación, se puede volver a programar para su reproducción. Los desarrolladores deben tener cuidado al volver a usar guiones gráficos, ya que esto solo debe hacerse cuando no hay ninguna posibilidad de que el mismo guión gráfico tenga que ponerse en cola debido a una acción del usuario cuando ya se está reproduciendo o en cola en la programación.

## <a name="example-code"></a>Código de ejemplo

El código de ejemplo siguiente se toma de MainWindow.cpp en los ejemplos de animación Windows animación controlada por la aplicación y [animación controlada por temporizador](timer-driven-animation-sample.md). [](application-driven-animation-sample.md) Usa el método [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para programar el guión gráfico. Este método requiere la hora actual como parámetro.


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a>Paso anterior

Antes de iniciar este paso, debe haber completado este paso: Crear [un guión gráfico y Agregar transiciones](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Información general sobre guiones gráficos](storyboard-construction.md)
</dt> </dl>

 

 




