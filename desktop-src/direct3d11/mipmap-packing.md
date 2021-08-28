---
title: Empaquetado de mapas MIP
description: En función del nivel de compatibilidad de los recursos en mosaico, los mapas mip con determinadas dimensiones no siguen las formas de mosaico estándar y se consideran empaquetados entre sí de una manera opaca para la aplicación.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd29098b2668b5b4aab51dd26924d8f166df6fab9a4c5f8c78d0c8f5166b28a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408045"
---
# <a name="mipmap-packing"></a>Empaquetado de mapas MIP

En función [](tiled-resources-features-tiers.md) del nivel de compatibilidad de los recursos en mosaico, los mapas mip con determinadas dimensiones no siguen las formas de mosaico estándar y se consideran empaquetados entre sí de una manera opaca para la aplicación. Los niveles más altos de compatibilidad tienen garantías más amplias sobre qué tipos de dimensiones de superficie caben en las formas de mosaico estándar (y, por tanto, las aplicaciones pueden asignar individualmente).

Lo que puede variar entre implementaciones es que, dadas las dimensiones, el formato, el número de mipmaps y los segmentos de matriz de un recurso en mosaico, se puede empaquetar algún número M de mips (por segmento de matriz) en algunos números N iconos. La API [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) existe para permitir que el controlador informe a la aplicación de qué son M y N (entre otros detalles sobre la superficie que esta API notifica que son estándar y no varían según el proveedor de hardware). El conjunto de iconos para los mips empaquetados sigue siendo de 64 KB y se puede asignar individualmente a ubicaciones dispares en un grupo de iconos. Pero la forma de píxel de los iconos y cómo encajan los mapas mip en el conjunto de iconos es específica de un proveedor de hardware y es demasiado compleja para exponer. Por lo tanto, las aplicaciones deben asignar todos los iconos que se designan como empaquetados, o ninguno de ellos, a la vez. De lo contrario, el comportamiento para acceder al recurso en mosaico no está definido.

En el caso de las superficies con matrices, el conjunto de mips empaquetados y el número de iconos empaquetados que almacenan esos mips (M y N descritos anteriormente) se aplican individualmente a cada segmento de matriz.

Las API dedicadas para copiar iconos [**(ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2::UpdateTiles)**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)no pueden tener acceso a mips empaquetados. Las aplicaciones que desean copiar datos hacia y desde mips empaquetados pueden hacerlo mediante todas las API específicas de recursos no en mosaico para copiar y representar en superficies.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




