---
title: Programar un guion gráfico
description: Una vez creado un guion gráfico, lo programa el administrador de animaciones.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- guiones gráficos animación y programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075163"
---
# <a name="schedule-a-storyboard"></a>Programar un guion gráfico

Una vez creado un guion gráfico, lo programa el administrador de animaciones.

## <a name="overview"></a>Información general

De forma predeterminada, cada guion gráfico se inicia inmediatamente cuando está programado. Esto significa que cuando un guion gráfico comienza a animar una o más variables, puede interrumpir cualquier otro guion gráfico que anime esas mismas variables. Sin embargo, una aplicación puede especificar otros comportamientos determinando la prioridad relativa entre los guiones gráficos.

Una vez que se ha programado un guion gráfico, ya no se puede modificar. Sin embargo, una vez que se ha quitado un guion gráfico de la programación, se puede programar para que se reproduzca. Los desarrolladores deben tener cuidado al volver a usar guiones gráficos, ya que esto solo debe hacerse cuando no es posible que sea necesario poner en cola el mismo guion gráfico debido a una acción del usuario cuando ya se está reproduciendo o en cola en la programación.

## <a name="example-code"></a>Código de ejemplo

El siguiente código de ejemplo se toma de MainWindow. cpp en la animación de Windows ejemplos de animaciones [controladas](application-driven-animation-sample.md) por la aplicación y la [animación controlada por temporizador](timer-driven-animation-sample.md). Usa el método [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) para programar el guión gráfico. Este método requiere la hora actual como parámetro.


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

Antes de comenzar este paso, debe haber completado este paso: [crear un guion gráfico y agregar transiciones](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer:: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Información general sobre guiones gráficos](storyboard-construction.md)
</dt> </dl>

 

 




