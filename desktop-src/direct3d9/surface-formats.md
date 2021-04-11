---
description: En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo de memoria lineal denominado Surface.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formatos de superficie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152433"
---
# <a name="surface-formats-direct3d-9"></a>Formatos de superficie (Direct3D 9)

En Direct3D, todas las imágenes bidimensionales (2D) se representan mediante un intervalo de memoria lineal denominado Surface. Una superficie puede considerarse como una matriz 2D en la que cada elemento contiene un valor de color que representa una pequeña sección de la imagen, denominada píxel. El nivel de detalle de una imagen se define tanto en el número de píxeles necesarios para representar la imagen como en el número de bits necesarios para el espectro de colores de la imagen. Por ejemplo, una imagen de 800 píxeles de ancho por 600 píxeles de alto con 32 bits de color para cada píxel (escrito como 800x600x32) será más detallada que una imagen de 640 píxeles de ancho por 480 píxeles de alto con 16 bits de color para cada píxel (escrito como 640x480x16). Del mismo modo, la imagen más detallada requerirá una superficie más grande para almacenar los datos. En el caso de una imagen 800x600x32, las dimensiones de la matriz de la superficie serán de 800x600 y cada elemento contendrá un valor de 32 bits para representar su color.

Todas las superficies tienen un tamaño y almacenan un número específico de bits que representan el color. Los bits que representan el color se separan en elementos de color individuales: rojo, verde y azul. En Direct3D, todos los elementos de color se definen mediante el tipo enumerado [D3DFORMAT](d3dformat.md) . Un formato de color de Direct3D se divide en el número de bytes reservados para cada color. Por ejemplo, un formato de color de 16 bits en Direct3D se define como D3DFMT \_ R5G6B5, donde 5 bits están reservados para rojo (R), 6 bits para verde (G) y 5 bits para azul (B).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



