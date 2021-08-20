---
description: En el modo de sombreado plano, se muestra la siguiente piramidal con un borde nítido entre caras adyacentes. Sin embargo, en el modo de sombreado de Gouraud, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparar modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df53df2751dc184cbb8246f47a56fbb2b3320e96432b664524a2e30018adc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911668"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Comparar modos de sombreado (Direct3D 9)

En el modo de sombreado plano, se muestra la siguiente piramidal con un borde nítido entre caras adyacentes. Sin embargo, en el modo de sombreado de Gouraud, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.

![ilustración de una piramidal con bordes y flechas nítidos que apuntan a las normales faciales](images/shade2.png)

El sombreado de Gouraud enciende superficies planas de forma más realista que el sombreado plano. Una cara en el modo de sombreado plano es un color uniforme, pero el sombreado de Gouraud permite que la luz se desencare en una cara más correctamente. Este efecto es especialmente obvio si hay un origen de punto cercano.

El sombreado gouraud suaviza los bordes nítidos entre los polígonos que son visibles con sombreado plano. Sin embargo, puede dar lugar a bandas de color, que son bandas de color o luz que no se mezclan sin problemas entre polígonos adyacentes. La aplicación puede reducir la apariencia de las bandas de Mach al aumentar el número de polígonos de un objeto, aumentar la resolución de la pantalla o aumentar la profundidad de color de la aplicación.

El sombreado de Gouraud puede perder algunos detalles. Por ejemplo, en la ilustración siguiente, un contenido destacado está completamente contenido dentro de una cara de polígono.

![ilustración de un destacado dentro de una cara de polígono](images/gouraud.png)

En este caso, el sombreado de Gouraud, que se interpola entre vértices, perdería el foco por completo; la cara se representaría como si el foco no existiera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 



