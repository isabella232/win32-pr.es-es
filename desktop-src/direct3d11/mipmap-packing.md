---
title: Empaquetado de mapas MIP
description: En función del nivel de compatibilidad de los recursos en mosaico, los mapas MIP con ciertas dimensiones no siguen las formas de mosaico estándar y se consideran que todos están empaquetados juntos entre sí de forma opaca para la aplicación.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075432"
---
# <a name="mipmap-packing"></a>Empaquetado de mapas MIP

En función del nivel de compatibilidad de los recursos [en](tiled-resources-features-tiers.md) mosaico, los mapas MIP con ciertas dimensiones no siguen las formas de mosaico estándar y se consideran que todos están empaquetados juntos entre sí de forma opaca para la aplicación. Los niveles más altos de soporte técnico tienen garantías más amplias sobre qué tipos de dimensiones de superficie caben en las formas de mosaico estándar (y, por tanto, las aplicaciones pueden asignarlos de forma individual).

Lo que puede variar entre las implementaciones es que, dadas las dimensiones de un recurso en mosaico, el formato, el número de mapas de información y los segmentos de matriz, se puede empaquetar un número M de MIPS (por segmento de matriz) en un número N de mosaicos. La API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) existe para permitir que el controlador informe a la aplicación Qué son M y N (entre otros detalles sobre la superficie que esta API notifica que son estándar y que no varían según el proveedor de hardware). El conjunto de mosaicos para el MIPS empaquetado sigue siendo de 64 KB y se puede asignar individualmente en ubicaciones dispares de un grupo de mosaicos. Pero la forma de píxeles de los mosaicos y el modo en que se ajustan los mipmaps en el conjunto de mosaicos es específica de un proveedor de hardware y es demasiado complejo de exponer. Por lo tanto, las aplicaciones deben asignar todos los iconos que se designan como empaquetados o ninguno de ellos a la vez. De lo contrario, el comportamiento para tener acceso al recurso en mosaico es indefinido.

En el caso de las superficies matrices, el conjunto de MIPs empaquetados y el número de mosaicos empaquetados que almacenan los MIPS (M y N descritos anteriormente) se aplican individualmente para cada segmento de la matriz.

Las API dedicadas para copiar mosaicos ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) y [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) no pueden tener acceso a MIPS empaquetado. Las aplicaciones que desean copiar datos a y desde MIPS empaquetados pueden hacerlo mediante todas las API específicas de recursos no en mosaico para copiar y representar superficies.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se organiza en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




