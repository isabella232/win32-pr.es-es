---
description: En Direct3D 10, se tiene acceso a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Vistas de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000676"
---
# <a name="texture-views-direct3d-10"></a>Vistas de textura (Direct3D 10)

En Direct3D 10, se tiene acceso a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria. Una vista permite a una fase de canalización concreta tener acceso solo a los [Subrecursos](d3d10-graphics-programming-guide-resources-types.md) que necesita, en la representación deseada por la aplicación.

Una vista admite la noción de un recurso sin tipo. Un recurso de tipo less es un recurso creado con un tamaño específico, pero no un tipo de datos específico. Los datos se interpretan dinámicamente cuando se enlazan a la canalización.

En la ilustración siguiente se muestra un ejemplo de enlace de una matriz de textura 2D con 6 texturas como un recurso de sombreador mediante la creación de una vista de recursos del sombreador para ella. A continuación, el recurso se dirige como una matriz de texturas. (Nota: un subrecurso no se puede enlazar como entrada y salida a la canalización simultáneamente).

![Ilustración de una matriz de texturas con seis texturas](images/d3d10-cube-texture-faces.png)

Cuando se usa una matriz de textura 2D como destino de representación, el recurso se puede ver como una matriz de texturas 2D (6 en este ejemplo) con niveles de mipmap (3 en este ejemplo).

Cree un objeto de vista para un destino de representación mediante una llamada a CreateRenderTargetView. A continuación, llame a OMSetRenderTargets para establecer la vista de destino de representación en la canalización. Se representa en los destinos de representación mediante una llamada a Draw y el uso de RenderTargetArrayIndex para indizar la textura adecuada en la matriz. Puede usar un subrecurso (un nivel de mipmap, una combinación de índice de matriz) para enlazar a cualquier matriz de Subrecursos. Por lo tanto, puede enlazar con el segundo nivel de mipmap y solo actualizar este nivel de mipmap determinado si lo desea, como en la siguiente ilustración.

![Ilustración de enlace solo al segundo nivel de mipmap de una matriz de textura](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10: en Direct3D 10, ya no se enlaza un recurso directamente a la canalización, se crea una vista de un recurso y, a continuación, se establece la vista en la canalización. Esto permite que la validación y la asignación en el tiempo de ejecución y el controlador se produzcan al crear la vista, lo que minimiza la comprobación de tipos en tiempo de enlace.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




