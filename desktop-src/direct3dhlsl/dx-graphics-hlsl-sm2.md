---
title: Shader Model 2
description: El modelo de sombreador 2 agregó funcionalidades adicionales al modelo de sombreador 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed402b34bdb8ba8caed8dc7cd5b66126d242c9ad
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988028"
---
# <a name="shader-model-2"></a>Shader Model 2

El modelo de sombreador 2 agregó funcionalidades adicionales al [modelo de sombreador 1.](dx-graphics-hlsl-sm1.md)





|--------|-------| | Características | Funcionalidad | | Conjunto de instrucciones | <ul><li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones HLSL</strong></a></li><li>Instrucciones de ensamblado (vea <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instrucciones - vs_2_0</a>, Instrucciones - <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">vs_2_x</a> <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">,</a>instrucciones de ps_2_0 , <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x instrucciones</a>)</li></ul> | | Registrar conjunto | <ul><li>Registros de sombreador de píxeles <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">(vea ps_2_0 registros ,</a> <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x registros</a>)</li><li>Registros del sombreador de <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">vértices</a>(vea Registros - vs_2_0 , <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">Registros - vs_2_x</a>)</li></ul> | | Número máximo de sombreadores de píxeles | <ul><li>ps_2_0: 32 texturas + 64 aritméticas</li><li>ps_2_x: 96 como mínimo y hasta el número de ranuras en D3DCAPS9. D3DPSHADERCAPS2_0.NumInstructionSlots. Consulte D3DPSHADERCAPS2_0</li></ul> | | Número máximo de sombreadores de vértices | 256 instrucciones | | Perfiles de sombreador | ps_2_0, ps_2_x, vs_2_0, vs_2_x | 




 

Para más información sobre el modelo de sombreador 2, consulte:

-   [Sombreador de píxeles 2.0,](dx9-graphics-reference-asm-ps-2-0.md) [Sombreador de píxeles 2.x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Sombreador de vértices 2.0](dx9-graphics-reference-asm-vs-2-0.md), [Sombreador de vértices 2.x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




