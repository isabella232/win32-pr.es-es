---
description: En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes. En el modo de sombreado Gouraud, sin embargo, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparar modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153576"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Comparar modos de sombreado (Direct3D 9)

En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes. En el modo de sombreado Gouraud, sin embargo, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.

![Ilustración de una pirámide con bordes nítidos y flechas que apuntan a las normales de cara](images/shade2.png)

El sombreado Gouraud muestra superficies planas más realista que el sombreado plano. Una superficie en el modo de sombreado plano es un color uniforme, pero el sombreado Gouraud permite que la luz se sitúe en una esfera más correctamente. Este efecto es especialmente obvio si hay un origen de punto cercano.

El sombreado Gouraud suaviza los bordes nítidos entre polígonos que están visibles con sombreado plano. Sin embargo, puede dar lugar a bandas de Mach, que son bandas de color o luz que no se combinan suavemente en polígonos adyacentes. La aplicación puede reducir la apariencia de las bandas de Mach aumentando el número de polígonos en un objeto, aumentando la resolución de la pantalla o aumentando la profundidad de color de la aplicación.

El sombreado Gouraud puede omitir algunos detalles. Por ejemplo, en la siguiente ilustración, una parte destacada se encuentra completamente dentro de una esfera de polígono.

![Ilustración de un foco dentro de una esfera de polígono](images/gouraud.png)

En este caso, el sombreado Gouraud, que se interpola entre vértices, omitiría el foco por completo; la superficie se representaría como si no existiera el foco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 



