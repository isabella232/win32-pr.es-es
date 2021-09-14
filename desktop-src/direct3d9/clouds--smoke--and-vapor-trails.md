---
description: Las nubes, el humo y los pistas de humo se pueden crear mediante una extensión de la técnica de alabar.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Nubes, humo y pistas de Quesada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063756"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Nubes, humo y pistas de Quesada (Direct3D 9)

Las nubes, el humo y los pistas de humo se pueden crear mediante una extensión de la técnica de alabar. Vea [Sobresaliendo (Direct3D 9).](billboarding.md) Al girar la rueda en dos ejes en lugar de uno, la aplicación puede permitir que el usuario vea un móvil desde cualquier ángulo. Normalmente, una aplicación gira el ángulo en los ejes horizontal y vertical.

Para crear una nube simple, la aplicación puede girar una primitiva rectangular en uno o dos ejes para que la primitiva se enfrenta al usuario. Después, se puede aplicar una textura de tipo nube a la primitiva con transparencia. Para obtener más información sobre cómo aplicar texturas transparentes a primitivas, vea [Mezcla de texturas (Direct3D 9).](texture-blending.md) Puede animar la nube aplicando una serie de texturas a lo largo del tiempo.

Una aplicación puede crear nubes más complejas formándolos a partir de un grupo de primitivas. Cada parte de la nube es una primitiva rectangular. Las primitivas se pueden mover de forma independiente con el tiempo para dar la apariencia de una bruma dinámica. En la ilustración siguiente se muestra este concepto.

![ilustración de primitivas que forman nubes más complejas](images/cloud.png)

La apariencia del humo se muestra de forma similar a las nubes. Normalmente, requiere varios paneles, como nubes complejas. Por lo general, el humo se factura y aumenta con el tiempo, por lo que las estaciones que lo hacen deben moverse en consecuencia. Es posible que tenga que agregar más paneles a medida que aumenta y se dispersa.

Una pista de humo es una ciruela de humo que no aumenta. Sin embargo, al igual que una columna de humo, se dispersa con el tiempo. En la ilustración siguiente se muestra la técnica de uso de ydas para simular un registro de la función.

![ilustración de los contrabandos que simulan una pista de música](images/vapor.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



