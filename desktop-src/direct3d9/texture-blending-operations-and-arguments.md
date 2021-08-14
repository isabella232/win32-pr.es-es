---
description: Las aplicaciones asocian una fase de mezcla con cada textura del conjunto de texturas actuales. Direct3D evalúa cada fase de mezcla en orden, empezando por la primera textura del conjunto y finalizando con la ocho.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operaciones y argumentos de mezcla de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d242092de5919267d30a9b8ff4e7bd2324f0bc3120649d3bb1a423b3462be77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797777"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Operaciones y argumentos de mezcla de textura (Direct3D 9)

Las aplicaciones asocian una fase de mezcla con cada textura del conjunto de texturas actuales. Direct3D evalúa cada fase de mezcla en orden, empezando por la primera textura del conjunto y finalizando con la ocho.

Direct3D aplica la información de cada textura del conjunto de texturas actuales a la fase de mezcla asociada a ella. Las aplicaciones controlan qué información de una fase de textura se usa mediante una llamada a [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api). Puede establecer operaciones independientes para los canales de color y alfa, y cada operación usa dos argumentos. Especifique las operaciones de canal de color mediante el estado de fase COLOROP de D3DTSS; especifique las operaciones \_ alfa mediante D3DTSS \_ ALPHAOP. Ambos estados de fase usan valores del [**tipo enumerado D3DTEXTUREOP.**](./d3dtextureop.md)

Los argumentos de combinación de textura usan los miembros D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 y D3DTSS ALPHARG2 del tipo enumerado \_ [**D3DTEXTURESTAGESTATETYPE.**](./d3dtexturestagestatetype.md) Los valores de argumento correspondientes se identifican mediante [D3DTA.](d3dta.md)

> [!Note]  
> Puede deshabilitar una fase de textura y las fases de mezcla de textura posteriores en cascada estableciendo la operación de color de esa fase en D3DTOP \_ DISABLE. Al deshabilitar la operación de color, también se deshabilita de forma eficaz la operación alfa. Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color. Establecer la operación alfa en D3DTOP \_ DISABLE cuando la combinación de colores está habilitada provoca un comportamiento indefinido.

 

Para determinar las operaciones de combinación de textura admitidas de un dispositivo, consulte el miembro TextureCaps de la [**estructura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de texturas](texture-blending.md)
</dt> </dl>

 

 
