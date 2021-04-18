---
description: Las nubes, humo y rastros de vapor se pueden crear mediante una extensión de la técnica de la cartelera.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Nubes, humo y rastros de vapor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564331"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Nubes, humo y rastros de vapor (Direct3D 9)

Las nubes, humo y rastros de vapor se pueden crear mediante una extensión de la técnica de la cartelera. Vea la [cartelera (Direct3D 9)](billboarding.md). Al girar la cartelera en dos ejes en lugar de uno, la aplicación puede permitir al usuario ver una cartelera desde cualquier ángulo. Normalmente, una aplicación gira la cartelera en los ejes horizontal y vertical.

Para crear una nube sencilla, la aplicación puede girar un primitivo rectangular en uno o dos ejes para que el primitivo enfrente al usuario. Una textura similar a la nube se puede aplicar a la primitiva con transparencia. Para obtener más información sobre cómo aplicar texturas transparentes a primitivos, vea [Texture blending (Direct3D 9)](texture-blending.md). Puede animar la nube aplicando una serie de texturas a lo largo del tiempo.

Una aplicación puede crear nubes más complejas formando un grupo de primitivas. Cada parte de la nube es un primitivo rectangular. Los primitivos se pueden moverse de forma independiente a lo largo del tiempo para dar la apariencia de una niebla dinámica. En la ilustración siguiente se muestra este concepto.

![Ilustración de primitivas que forman nubes más complejas](images/cloud.png)

La apariencia del humo se muestra de manera similar a las nubes. Normalmente requiere varias cartelera, como nubes complejas. El humo normalmente Billows y aumenta con el tiempo, por lo que las cartelera que conforman el humo deben moverse en consecuencia. Es posible que tenga que agregar más cartelera a medida que la ciruela aumenta y se dispersa.

Un rastro de vapor es una ciruela de humo que no aumenta. Sin embargo, al igual que un humo, se dispersa con el tiempo. En la ilustración siguiente se muestra la técnica de uso de las cartelera para simular una pista de vapor.

![Ilustración de las cartelera que simulan un rastro de vapor](images/vapor.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de alfa](alpha-examples.md)
</dt> </dl>

 

 



