---
description: En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo lineal de memoria denominado superficie.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formatos de superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160427"
---
# <a name="surface-formats-direct3d-9"></a>Formatos de superficie (Direct3D 9)

En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo lineal de memoria denominado superficie. Una superficie se puede pensar en una matriz 2D donde cada elemento contiene un valor de color que representa una pequeña sección de la imagen, denominada píxel. El nivel de detalle de una imagen se define tanto por el número de píxeles necesarios para representar la imagen como por el número de bits necesarios para el espectro de colores de la imagen. Por ejemplo, una imagen de 800 píxeles de ancho por 600 píxeles de alto con 32 bits de color para cada píxel (escrita como 800 x 600 x 32) será más detallada que una imagen de 640 píxeles de ancho por 480 píxeles de alto con 16 bits de color para cada píxel (escrita como 640 x 480 x 16). Del mismo modo, la imagen más detallada requerirá una superficie mayor para almacenar los datos. Para una imagen de 800 x 600 x 32, las dimensiones de matriz de la superficie serán 800 x 600 y cada elemento contendrán un valor de 32 bits para representar su color.

Todas las superficies tienen un tamaño y almacenan un número específico de bits que representan el color. Los bits que representan el color se separan en elementos de color individuales: rojo, verde y azul. En Direct3D, todos los elementos de color se definen mediante el tipo enumerado [D3DFORMAT.](d3dformat.md) Un formato de color direct3D se divide en el número de byes reservados para cada color. Por ejemplo, un formato de color de 16 bits en Direct3D se define como D3DFMT R5G6B5, donde 5 bits están reservados para rojo (R), 6 bits para verde \_ (G) y 5 bits para azul (B).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



