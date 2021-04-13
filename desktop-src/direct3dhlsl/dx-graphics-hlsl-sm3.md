---
title: Modelo de sombreador 3
description: El modelo de sombreador 3 agregó capacidades adicionales al sombreador modelo 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104421506"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (referencia de HLSL)

El modelo de sombreador 3 agregó capacidades adicionales al [sombreador modelo 2](dx-graphics-hlsl-sm2.md).



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
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones de HLSL</strong></a></li>
<li>Instrucciones de ensamblado (vea <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">instrucciones de ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instrucciones-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registros</td>
<td><ul>
<li>Registros del sombreador de píxeles (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">registros de ps_3_0</a>)</li>
<li>Registros del sombreador de vértices (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registros-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sombreador de píxeles máximo</td>
<td>512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxPixelShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Sombreador de vértices máximo</td>
<td>512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxVertexShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Perfiles del sombreador</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre los sombreadores de modelo 3, vea:

-   [Sombreador de píxeles 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Sombreador de vértices 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 