---
title: Formatos de estarcido no compatibles con recursos en mosaico
description: Los formatos que contienen la galería de símbolos no se admiten con recursos en mosaico.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075001"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>Formatos de estarcido no compatibles con recursos en mosaico

Los formatos que contienen la galería de símbolos no se admiten con recursos en mosaico.

Los formatos que contienen la Galería \_ de símbolos incluyen el formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint (y los formatos relacionados en la familia R24G8) y el \_ formato dxgi \_ D32 \_ float \_ S8X24 \_ uint (y los formatos relacionados en la familia R32G8X24).

Algunas implementaciones almacenan la profundidad y la galería de símbolos en asignaciones independientes mientras que otras las almacenan juntas. La administración de mosaicos para los dos esquemas tendría que ser diferente, y ninguna API única puede abstraer o racionalizar las diferencias. Se recomienda que el hardware futuro admita superficies de estarcido y profundidad independientes, cada una de las cuales se organiza por separado. la profundidad de bits de 32 tendría iconos de 128x128 y la galería de símbolos de 8 bits tendría iconos de 256x256. Por lo tanto, las aplicaciones tendrían que vivir con la alineación de la forma de mosaico entre la profundidad y la galería de símbolos. Pero ya existe el mismo problema con los distintos formatos de superficie de destino de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proceso cruzado y uso compartido de dispositivos entre recursos en mosaico](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




