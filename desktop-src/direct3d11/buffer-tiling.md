---
title: Mosaico de búfer
description: Un recurso de búfer se divide en iconos de 64 KB, con algún espacio vacío en el último icono si el tamaño no es un múltiplo de 64 KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734247"
---
# <a name="buffer-tiling"></a>Mosaico de búfer

Un [recurso](overviews-direct3d-11-resources-buffers.md) de búfer se divide en iconos de 64 KB, con algún espacio vacío en el último icono si el tamaño no es un múltiplo de 64 KB.

Los búferes estructurados no deben tener ninguna restricción en el paso que se va a incluir en mosaico. Sin embargo, las posibles optimizaciones de rendimiento en hardware para usar [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) se pueden sacrificar haciendo que se coloquen en mosaico en primer lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 