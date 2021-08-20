---
description: Dirección de transición
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Dirección de transición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2097f13225c7691780646d77a18d048a48e31eda498955bdc53a0c954728c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951503"
---
# <a name="transition-direction"></a>Dirección de transición

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una transición va de la entrada A a la entrada B y de la hora t₀ a t₁. Por lo tanto, *la dirección* de una transición puede significar una de estas dos cosas:

-   Asignación de capas de escala de tiempo a entradas.
-   Progresión a lo largo del tiempo.

La primera es la *dirección de entrada* y la segunda es la dirección de *progreso*. Puede controlar ambas direcciones.

-   Dirección de entrada: de forma predeterminada, una transición pasa de la composición de las capas de prioridad inferior a la capa que contiene la transición. Para invertir esta dirección, llame al [**método IAMTimelineTrans::SetSwapInputs.**](iamtimelinetrans-setswapinputs.md)
-   Dirección del progreso: la mayoría de las transiciones admiten una propiedad **Progress** estándar, que especifica qué porcentaje de la transición se refleja en la salida en un momento dado. De forma predeterminada, el valor de la propiedad **Progress** va de 0,0 a 1,0 durante la transición. Para invertir el progreso, establezca la **propiedad Progress** para que vaya de 1.0 a 0.0.

En el diagrama siguiente se muestra la diferencia entre la dirección de entrada y la dirección del progreso. Muestra cuatro variaciones en una transición estándar de [borrado de SMPTE.](smpte-wipe-transition.md)

![direcciones de borrado](images/wipedirections.png)

La transición reside en la pista 1. De forma predeterminada, el borrado va de izquierda a derecha y de la pista 0 a la pista 1. El intercambio de entradas hace que el borrado vaya de la pista 1 a la pista 0, pero de izquierda a derecha. Al invertir el progreso, la transición pasa de derecha a izquierda. Puede combinar ambos, como se muestra en el extremo izquierdo.

Para obtener más información sobre cómo REPRESENTA DES las transiciones, vea [El modelo de escala de tiempo](the-timeline-model.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



