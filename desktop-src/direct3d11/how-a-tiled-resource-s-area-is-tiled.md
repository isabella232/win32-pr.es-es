---
title: Cómo se en mosaico el área de un recurso en mosaico
description: Al crear un recurso en mosaico, las dimensiones, el tamaño del elemento de formato y el número de mapas mipmap o segmentos de matriz (si procede) determinan el número de iconos necesarios para realizar una copia de seguridad de todo el área de superficie.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963819"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Cómo se en mosaico el área de un recurso en mosaico

Al crear un recurso en mosaico, las dimensiones, el tamaño del elemento de formato y el número de mapas mipmap o segmentos de matriz (si procede) determinan el número de iconos necesarios para realizar una copia de seguridad de todo el área de superficie. La implementación determina el diseño de píxel/byte dentro de los iconos. El número de píxeles que caben en un icono, en función del tamaño del elemento de formato, es fijo e idéntico, independientemente de si se usa un swzzle estándar o no.

El número de iconos que usará un determinado tamaño de superficie y ancho de elemento de formato está bien definido y predecible en función de las tablas de las secciones siguientes. En el caso de los recursos que contienen mapas MIP o casos en los que las dimensiones de superficie no rellenan un icono, existen algunas restricciones y se de abordan en empaquetado [de Mipmap](mipmap-packing.md).

Los distintos recursos en mosaico pueden apuntar a memoria idéntica con formatos diferentes, siempre y cuando las aplicaciones no se basen en los resultados de escribir en la memoria con un formato y leer con otro. Sin embargo, en circunstancias restringidas, las aplicaciones pueden basarse en los resultados de escribir en la memoria con un formato y leer con otro si los formatos están en la misma familia de formatos (es decir, tienen el mismo formato primario sin tipo). Por ejemplo, DXGI \_ FORMAT \_ R8G8B8A8 UNORM y DXGI FORMAT R8G8B8A8 UINT son compatibles entre sí, pero no con \_ \_ \_ \_ DXGI \_ FORMAT \_ R16G16 \_ UNORM. Una aplicación debe coincidir de forma conservadora con todas las propiedades de recursos para reinterpretar los datos entre dos texturas, ya que los patrones de mosaico son muy conservadores indefinidos. Obviamente, sin embargo, el formato es más lax. Los formatos solo deben ser compatibles como se muestra anteriormente. Una excepción es que los datos desaprobados de un alias de formato a otro están bien definidos: si un icono contiene completamente 0 para todos sus bits, ese icono se puede usar con cualquier formato que interprete ese contenido de memoria como 0 (independientemente del diseño de memoria). Por lo tanto, se podría borrar un icono para 0x00 con el formato DXGI FORMAT R8 UNORM y, a continuación, usar con un formato como DXGI FORMAT R32G32 FLOAT y parece que el contenido sigue siendo \_ \_ \_ \_ \_ \_ (0.0f,0.0f).

El diseño de los datos dentro de un icono puede depender de las propiedades del recurso, el subrecurso en el que reside y la ubicación del icono dentro del subrecurso. Las principales excepciones se ilustran anteriormente: formatos compatibles con otras propiedades de recursos que son iguales y cuando todos los elementos de textura tienen el mismo patrón.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mosaico de subrecurso Texture2D y Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Estas tablas muestran cómo se en mosaicos los subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray.**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) <br/>                                                                                                          |
| [Mosaico de subrecurso Texture3D](texture3d-subresource-tiling.md)<br/>                                       | En esta tabla se muestra cómo se en mosaicos los subrecursos de [**Texture3D.**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) <br/>                                                                                                                                                                            |
| [Mosaico de búfer](buffer-tiling.md)<br/>                                                                     | Un [recurso](overviews-direct3d-11-resources-buffers.md) de búfer se divide en iconos de 64 KB, con algún espacio vacío en el último icono si el tamaño no es un múltiplo de 64 KB.<br/>                                                                                                  |
| [Empaquetado de mapas MIP](mipmap-packing.md)<br/>                                                                   | En función [](tiled-resources-features-tiers.md) del nivel de compatibilidad de los recursos en mosaico, los mapas MIP con determinadas dimensiones no siguen las formas de mosaico estándar y se consideran que se empaquetan entre sí de una manera opaca para la aplicación. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

