---
title: Mosaico de subrecurso Texture3D
description: En esta tabla se muestra cómo se muestran los Subrecursos de Texture3D en mosaico.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997169"
---
# <a name="texture3d-subresource-tiling"></a>Mosaico de subrecurso Texture3D

En esta tabla se muestra cómo se muestran los Subrecursos de [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) en mosaico. Los valores de esta tabla no cuentan el empaquetado de la cola MIP.

En esta tabla se toma el mosaico [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y se dividen las dimensiones x/y en 4 cada una de ellas y se agregan 16 niveles de profundidad. Todos los mosaicos para el primer plano (plano 2D de mosaicos que definen las 16 primeras capas de profundidad) aparecen antes que los planos posteriores.

> [!Note]  
> La compatibilidad con [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) en recursos en mosaico no se expone en la implementación inicial de los recursos en mosaico, pero las formas de iconos deseadas se enumeran aquí porque es posible que se tenga en cuenta la compatibilidad en una versión futura.

 



| Bits/píxel (1 ejemplo/píxel) | Dimensiones del mosaico (píxeles, a la x) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1, 4                       | 128x64x16                       |
| BC2, 3, 5, 6, 7                 | 64x64x16                        |



 

Los recuentos de bits de formato no admitidos con los recursos en mosaico son formatos de 96 BPP, formatos de vídeo, formato de DXGI \_ \_ R1 \_ UNORM, formato de dxgi \_ \_ R8G8 \_ B8G8 \_ UNORM y formato de dxgi \_ \_ R8R8 \_ \_ G8B8 UNORM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se organiza en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 