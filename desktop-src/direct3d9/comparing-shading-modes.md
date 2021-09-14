---
description: En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes. Sin embargo, en el modo de sombreado de Gouraud, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparar modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888716"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Comparar modos de sombreado (Direct3D 9)

En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes. Sin embargo, en el modo de sombreado de Gouraud, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.

![ilustración de una pirámide con bordes y flechas nítidos que apuntan a los normales faciales](images/shade2.png)

El sombreado de Gouraud enciende superficies planas de forma más realista que el sombreado plano. Una cara en el modo de sombreado plano es un color uniforme, pero el sombreado de Gouraud permite que la luz se rebaja más correctamente en una cara. Este efecto es especialmente obvio si hay un origen de punto cercano.

El sombreado gouraud suaviza los bordes nítidos entre polígonos que son visibles con sombreado plano. Sin embargo, puede dar lugar a bandas de colores, que son bandas de color o luz que no se mezclan sin problemas entre polígonos adyacentes. La aplicación puede reducir la apariencia de bandas de Mach al aumentar el número de polígonos de un objeto, aumentar la resolución de la pantalla o aumentar la profundidad de color de la aplicación.

El sombreado de Gouraud puede perder algunos detalles. Por ejemplo, en la ilustración siguiente, un contenido destacado se encuentra completamente dentro de una cara de polígono.

![ilustración de un destacado dentro de una cara de polígono](images/gouraud.png)

En este caso, el sombreado de Gouraud, que se interpola entre los vértices, perdería el foco por completo; la cara se representaría como si el foco de atención no existiera.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 



