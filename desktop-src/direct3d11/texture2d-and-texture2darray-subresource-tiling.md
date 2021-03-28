---
title: Mosaico de subrecurso Texture2D y Texture2DArray
description: En estas tablas se muestra cómo se muestran los Subrecursos Texture2D y Texture2DArray en mosaico.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421041"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Mosaico de subrecurso Texture2D y Texture2DArray

En estas tablas se muestra cómo se muestran los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) en mosaico. Los valores de estas tablas no cuentan el empaquetado de la cola MIP.

En esta tabla se muestra cómo se muestran en mosaico los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con recuentos Multimuestra de 1.



| Bits/píxel (1 ejemplo/píxel) | Dimensiones del mosaico (píxeles, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128x64                        |
| 128                         | 64x64                         |
| BC1, 4                       | 512x256                       |
| BC2, 3, 5, 6, 7                 | 256x256                       |



 

Los recuentos de bits de formato no admitidos con los recursos en mosaico son formatos de 96 BPP, formatos de vídeo, formato de DXGI \_ \_ R1 \_ UNORM, formato de dxgi \_ \_ R8G8 \_ B8G8 \_ UNORM y formato de dxgi \_ \_ R8R8 \_ \_ G8B8 UNORM.

En esta tabla se muestra cómo se muestran en mosaico los Subrecursos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con varios recuentos de muestras.



| Recuento de muestras Multimuestra           | Dividir las dimensiones del mosaico por encima de (WxH) |
|-----------------------------|-------------------------------|
| 1                           | asesoramiento                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4 TB                           |
| 16                          | 4 x 4                           |



 

Solo se requieren (y se permiten) los recuentos de muestras 1 y 4 para que se admitan con recursos en mosaico. Los recursos en mosaico no admiten actualmente 2, 8 y 16 aunque se muestren.

Las implementaciones pueden optar por admitir el modo 2, 8 o 16 de ejemplo de suavizado de contorno de muestreo múltiple (MSAA) para los recursos no en mosaico, aunque los recursos en mosaico no los admitan.

Los recursos en mosaico con recuentos de muestras mayores que 1 no pueden usar formatos de 128 BPP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se organiza en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 