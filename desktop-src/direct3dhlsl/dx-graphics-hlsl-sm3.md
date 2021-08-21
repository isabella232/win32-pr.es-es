---
title: Modelo de sombreador 3
description: Shader Model 3 agregó funcionalidades adicionales al modelo de sombreador 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed2d64ccfb06fc0fe50e5bd0075732c1fd9cbb70ca1e05bda5afd24cd5c5f98f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789545"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (referencia HLSL)

Shader Model 3 agregó funcionalidades adicionales al modelo [de sombreador 2.](dx-graphics-hlsl-sm2.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Característica</td>
<td>Funcionalidad</td>
</tr>
<tr class="even">
<td>Conjunto de instrucciones</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones HLSL</strong></a></li>
<li>Instrucciones de ensamblado <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">(consulte instrucciones ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instrucciones - vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registro</td>
<td><ul>
<li>Registros del sombreador de píxeles <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">(consulte ps_3_0 registros)</a></li>
<li>Registros del sombreador de vértices (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registros - vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Máximo de sombreador de píxeles</td>
<td>512 como mínimo y hasta el número de ranuras en D3DCAPS9. MaxPixelShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Máximo del sombreador de vértices</td>
<td>512 como mínimo y hasta el número de ranuras en D3DCAPS9. MaxVertexShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9).</strong></a></td>
</tr>
<tr class="even">
<td>Perfiles de sombreador</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Para más información sobre los sombreadores del modelo 3, consulte:

-   [Sombreador de píxeles 3.0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Sombreador de vértices 3.0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 