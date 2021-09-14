---
title: No se admiten formatos de galería de símbolos con recursos en mosaico
description: Los formatos que contienen galería de símbolos no se admiten con recursos en mosaico.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966903"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>No se admiten formatos de galería de símbolos con recursos en mosaico

Los formatos que contienen galería de símbolos no se admiten con recursos en mosaico.

Los formatos que contienen galería de símbolos incluyen DXGI FORMAT D24 UNORM S8 UINT (y formatos relacionados de la familia \_ \_ \_ \_ \_ R24G8) y DXGI \_ FORMAT \_ D32 FLOAT S8X24 UINT (y formatos relacionados en la familia \_ \_ \_ R32G8X24).

Algunas implementaciones almacenan la profundidad y la galería de símbolos en asignaciones independientes, mientras que otras las almacenan juntas. La administración de mosaicos para los dos esquemas tendría que ser diferente y ninguna API puede abstraer o racionalizar las diferencias. Se recomienda que el hardware futuro admita superficies de galería de símbolos y profundidad independientes, cada una de ellas en mosaico de forma independiente. La profundidad de 32 bits tendría iconos de 128 x 128 y la galería de símbolos de 8 bits tendría iconos de 256 x 256. Por lo tanto, las aplicaciones tendrían que convivir con una desalineación de la forma del icono entre la profundidad y la galería de símbolos. Pero ya existe el mismo problema con diferentes formatos de superficie de destino de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso compartido de dispositivos y procesos en mosaico](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




