---
title: Cómo se organiza en mosaico el área de un recurso en mosaico
description: Cuando se crea un recurso en mosaico, las dimensiones, el tamaño de los elementos de formato y el número de mapas MIP y/o segmentos de matriz (si procede) determinan el número de mosaicos necesarios para respaldar todo el área expuesta.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997124"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Cómo se organiza en mosaico el área de un recurso en mosaico

Cuando se crea un recurso en mosaico, las dimensiones, el tamaño de los elementos de formato y el número de mapas MIP y/o segmentos de matriz (si procede) determinan el número de mosaicos necesarios para respaldar todo el área expuesta. El diseño de píxeles/bytes dentro de los mosaicos viene determinado por la implementación de. El número de píxeles que caben en un mosaico, dependiendo del tamaño del elemento de formato, es fijo y idéntico si se usa un swizzle estándar o no.

El número de mosaicos que va a usar un tamaño de superficie y un ancho de elemento de formato determinados está bien definido y predecible en función de las tablas de las secciones siguientes. En el caso de los recursos que contienen mapas MIP o casos en los que las dimensiones de la superficie no rellenan un icono, existen algunas restricciones y se tratan en el [empaquetado de mipmap](mipmap-packing.md).

Los distintos recursos en mosaico pueden apuntar a la memoria idéntica con formatos diferentes, siempre y cuando las aplicaciones no se basen en los resultados de escribir en la memoria con un formato y leer con otro. Sin embargo, en circunstancias limitadas, las aplicaciones pueden confiar en los resultados de escribir en la memoria con un formato y leer con otro si los formatos están en la misma familia de formato (es decir, tienen el mismo formato primario sin tipo). Por ejemplo, el formato de DXGI \_ \_ R8G8B8A8 \_ UNORM y el formato de dxgi \_ \_ R8G8B8A8 \_ uint son compatibles entre sí, pero no con el formato de dxgi \_ \_ R16G16 \_ UNORM. Una aplicación debe coincidir con todas las propiedades de recurso para reinterpretar los datos entre dos texturas, ya que los patrones de mosaico son muy conservadormente indefinidos. Obviamente, sin embargo, el formato es más LAX. Los formatos solo deben ser compatibles como se muestra anteriormente. Una excepción es donde se definen bien los datos de sangrados de un formato de alias a otro: Si un mosaico contiene completamente 0 para todos sus bits, ese mosaico se puede usar con cualquier formato que interprete el contenido de la memoria como 0 (independientemente del diseño de memoria). Por lo tanto, un icono se puede borrar a 0x00 con el formato DXGI \_ \_ \_ UNORM y después usarse con un formato como dxgi \_ format \_ R32G32 \_ float y parecería que el contenido sigue siendo (0.0 f, 0.0 f).

El diseño de los datos dentro de un mosaico puede depender de las propiedades de los recursos, el subrecurso en el que reside y la ubicación del icono en el subrecurso. Las excepciones principales se ilustran anteriormente: los formatos compatibles con otras propiedades de recursos son iguales y cuando todos los textura son el mismo patrón.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mosaico de subrecurso Texture2D y Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | En estas tablas se muestra cómo se muestran los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) en mosaico. <br/>                                                                                                          |
| [Mosaico de subrecurso Texture3D](texture3d-subresource-tiling.md)<br/>                                       | En esta tabla se muestra cómo se muestran los Subrecursos de [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) en mosaico. <br/>                                                                                                                                                                            |
| [Mosaico de búfer](buffer-tiling.md)<br/>                                                                     | Un recurso de [búfer](overviews-direct3d-11-resources-buffers.md) se divide en mosaicos de 64 KB, con un espacio vacío en el último mosaico si el tamaño no es múltiplo de 64 KB.<br/>                                                                                                  |
| [Empaquetado de mapas MIP](mipmap-packing.md)<br/>                                                                   | En función del nivel de compatibilidad de los recursos [en](tiled-resources-features-tiers.md) mosaico, los mapas MIP con ciertas dimensiones no siguen las formas de mosaico estándar y se consideran que todos están empaquetados juntos entre sí de forma opaca para la aplicación. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

