---
description: Dirección de la transición
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Dirección de la transición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550246"
---
# <a name="transition-direction"></a>Dirección de la transición

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una transición va desde la entrada a a la entrada B y desde el tiempo t ₀ hasta t ₁. Por lo tanto, la *Dirección* de una transición puede significar una de estas dos cosas:

-   Asignación de las capas de la escala de tiempo a las entradas.
-   La progresión a lo largo del tiempo.

El primero es la *dirección de entrada* y el segundo es la *dirección de progreso*. Puede controlar ambas direcciones.

-   Dirección de entrada: de forma predeterminada, una transición va del compuesto de los niveles de prioridad inferior a la capa que contiene la transición. Para invertir esta dirección, llame al método [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .
-   Dirección del progreso: la mayoría de las transiciones admiten una propiedad de **progreso** estándar, que especifica qué porcentaje de la transición se refleja en la salida en un momento dado. De forma predeterminada, el valor de la propiedad **Progress** va de 0,0 a 1,0 durante la transición. Para invertir el progreso, establezca la propiedad **Progress** en go de 1,0 a 0,0.

En el diagrama siguiente se ilustra la diferencia entre la dirección de entrada y la dirección de progreso. Muestra cuatro variaciones en una transición de [borrado de SMPTE](smpte-wipe-transition.md) estándar.

![instrucciones de borrado](images/wipedirections.png)

La transición reside en el seguimiento 1. De forma predeterminada, el borrado se realiza de izquierda a derecha y de seguimiento de 0 a 1. El intercambio de entradas hace que el barrido pase de la pista 1 a la pista 0, pero de izquierda a derecha. Invertir el progreso hace que la transición pase de derecha a izquierda. Puede combinar ambos, tal como se muestra en el extremo izquierdo.

Para obtener más información sobre el modo en que DES representa las transiciones, consulte [el modelo de escala de tiempo](the-timeline-model.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



