---
description: Las aplicaciones asocian una fase de combinación con cada textura del conjunto de texturas actuales. Direct3D evalúa cada fase de combinación en orden, comenzando por la primera textura del conjunto y terminando por el octavo.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Operaciones y argumentos de combinación de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714741"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a>Operaciones y argumentos de combinación de texturas (Direct3D 9)

Las aplicaciones asocian una fase de combinación con cada textura del conjunto de texturas actuales. Direct3D evalúa cada fase de combinación en orden, comenzando por la primera textura del conjunto y terminando por el octavo.

Direct3D aplica la información de cada textura en el conjunto de texturas actuales a la fase de fusión que está asociada con ella. Las aplicaciones controlan qué información de una fase de textura se usa llamando a [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api). Puede establecer operaciones independientes para los canales alfa y de color, y cada operación utiliza dos argumentos. Especifique las operaciones del canal de color mediante el estado de fase de D3DTSS \_ COLOROP; especifique las operaciones alfa mediante D3DTSS \_ ALPHAOP. Ambos Estados de fase usan valores del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .

Los argumentos de combinación de texturas usan los \_ miembros D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 y D3DTSS \_ ALPHARG2 del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Los valores de argumento correspondientes se identifican mediante [D3DTA](d3dta.md).

> [!Note]  
> Puede deshabilitar una fase de textura (y todas las fases de fusión de texturas posteriores en cascada) estableciendo la operación de color para esa fase en D3DTOP \_ deshabilitar. Deshabilitar la operación de color realmente deshabilita también la operación alfa. Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color. La configuración de la operación Alpha en D3DTOP \_ se deshabilita cuando la combinación de colores está habilitada provoca un comportamiento indefinido.

 

Para determinar las operaciones admitidas de mezcla de texturas de un dispositivo, consulte el miembro TextureCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> </dl>

 

 
