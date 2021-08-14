---
description: En Direct3D 10, se accede a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Vistas de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc420e39c4d577947cae657f3296b15f0052db9e823e07d3a3ba1ccb641fb6b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101359"
---
# <a name="texture-views-direct3d-10"></a>Vistas de textura (Direct3D 10)

En Direct3D 10, se accede a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria. Una vista permite que una fase de canalización determinada acceda solo a los [subrecursos](d3d10-graphics-programming-guide-resources-types.md) que necesita, en la representación deseada por la aplicación.

Una vista admite la noción de un recurso sin tipo. Un recurso sin tipo es un recurso creado con un tamaño específico, pero no un tipo de datos específico. Los datos se interpretan dinámicamente cuando se enlazan a la canalización.

En la ilustración siguiente se muestra un ejemplo de enlace de una matriz de texturas 2D con 6 texturas como un recurso de sombreador mediante la creación de una vista de recursos de sombreador para él. A continuación, el recurso se trata como una matriz de texturas. (Nota: un subrecurso no se puede enlazar como entrada y salida a la canalización simultáneamente).

![ilustración de una matriz de texturas con seis texturas](images/d3d10-cube-texture-faces.png)

Cuando se usa una matriz de textura 2D como destino de representación, el recurso se puede ver como una matriz de texturas 2D (6 en este ejemplo) con niveles de mapa mip (3 en este ejemplo).

Cree un objeto de vista para un destino de representación mediante una llamada a CreateRenderTargetView. A continuación, llame a OMSetRenderTargets para establecer la vista de destino de representación en la canalización. Para representar en los destinos de representación, llame a Draw y use RenderTargetArrayIndex para indexar en la textura adecuada de la matriz. Puede usar un subrecurso (un nivel mipmap, combinación de índice de matriz) para enlazar a cualquier matriz de subrecursos. Por lo tanto, podría enlazar al segundo nivel de mapa mipmap y actualizar solo este nivel de mapa mip si lo desea, como en la ilustración siguiente.

![ilustración del enlace solo al segundo nivel mipmap de una matriz de textura](images/d3d10-cube-texture-faces-subresource.png)



Diferencias entre Direct3D 9 y Direct3D 10:

- En Direct3D 10, ya no se enlaza un recurso directamente a la canalización, se crea una vista de un recurso y, a continuación, se establece la vista en la canalización. Esto permite que la validación y asignación en el tiempo de ejecución y el controlador se produzcan en la creación de vistas, lo que minimiza la comprobación de tipos en tiempo de enlace.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




