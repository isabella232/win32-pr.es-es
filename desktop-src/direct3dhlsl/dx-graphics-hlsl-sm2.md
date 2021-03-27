---
title: Modelo de sombreador 2
description: El modelo de sombreador 2 agregó capacidades adicionales al modelo de sombreador 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104997036"
---
# <a name="shader-model-2"></a>Modelo de sombreador 2

El modelo de sombreador 2 agregó capacidades adicionales al [modelo de sombreador 1](dx-graphics-hlsl-sm1.md).



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
<li>Instrucciones de ensamblado (consulte las instrucciones <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instructions-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">instrucciones de ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x instrucciones</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registros</td>
<td><ul>
<li>Registros del sombreador de píxeles (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">registros de ps_2_0</a>, registros de <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x</a>)</li>
<li>Registros del sombreador de vértices (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registros-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registros-vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sombreador de píxeles máximo</td>
<td><ul>
<li>ps_2_0-32 textura + 64 aritmética</li>
<li>ps_2_x-96 como mínimo y hasta el número de ranuras de D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots. Consulte D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sombreador de vértices máximo</td>
<td>256 instrucciones</td>
</tr>
<tr class="even">
<td>Perfiles del sombreador</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Para obtener más información sobre el modelo de sombreador 2, consulte:

-   [Sombreador de píxeles 2,0](dx9-graphics-reference-asm-ps-2-0.md), [sombreador de píxeles 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Sombreador de vértices 2,0](dx9-graphics-reference-asm-vs-2-0.md), [sombreador de vértices 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




