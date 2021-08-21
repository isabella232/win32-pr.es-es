---
title: Mosaico de subrecurso Texture2D y Texture2DArray
description: Estas tablas muestran cómo se en mosaicos los subrecursos Texture2D y Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7cc181845785ab978dc5d58b1e131a7f32c34a6d04006af1ac8034f089ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530440"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Mosaico de subrecurso Texture2D y Texture2DArray

Estas tablas muestran cómo se en mosaicos los subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray.**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) Los valores de estas tablas no cuentan el empaquetado de mip de cola.

En esta tabla se muestra cómo se en mosaicos los subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con recuentos de múltiples muestras de 1.



| Bits/píxeles (1 muestra/píxel) | Dimensiones de mosaico (píxeles, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256 x 128                       |
| 32                          | 128 x 128                       |
| 64                          | 128 x 64                        |
| 128                         | 64x64                         |
| BC1,4                       | 512 x 256                       |
| BC2,3,5,6,7                 | 256x256                       |



 

Los recuentos de bits de formato no admitidos con recursos en mosaico son formatos de 96 bpp, formatos de vídeo, DXGI \_ FORMAT \_ R1 \_ UNORM, DXGI \_ FORMAT \_ R8G8 \_ B8G8 UNORM y \_ DXGI FORMAT \_ \_ R8R8 \_ G8B8 \_ UNORM.

En esta tabla se muestra cómo se en mosaicos los subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con varios recuentos de muestreo múltiple.



| Recuento de varios muestreos           | Dividir las dimensiones de mosaico anteriores por (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4 x 4                           |



 

Solo los recuentos de ejemplo 1 y 4 son necesarios (y permitidos) para ser compatibles con los recursos en mosaico. Los recursos en mosaico no admiten actualmente 2, 8 y 16, aunque se muestran.

Las implementaciones pueden optar por admitir 2, 8 o 16 ejemplos de modo de suavizado de contorno multimuestreo (MSAA) para recursos sin mosaico, aunque los recursos en mosaico no los admitan.

Los recursos en mosaico con recuentos de ejemplo mayores que 1 no pueden usar formatos de 128 bpp.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 