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
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="4840d-103">Shader Model 3 (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="4840d-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="4840d-104">El modelo de sombreador 3 agregó capacidades adicionales al [sombreador modelo 2](dx-graphics-hlsl-sm2.md).</span><span class="sxs-lookup"><span data-stu-id="4840d-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4840d-105">Característica</span><span class="sxs-lookup"><span data-stu-id="4840d-105">Feature</span></span></td>
<td><span data-ttu-id="4840d-106">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="4840d-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4840d-107">Conjunto de instrucciones</span><span class="sxs-lookup"><span data-stu-id="4840d-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="4840d-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones de HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="4840d-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="4840d-109">Instrucciones de ensamblado (vea <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">instrucciones de ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instrucciones-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="4840d-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4840d-110">Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4840d-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="4840d-111">Registros del sombreador de píxeles (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">registros de ps_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="4840d-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="4840d-112">Registros del sombreador de vértices (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registros-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="4840d-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4840d-113">Sombreador de píxeles máximo</span><span class="sxs-lookup"><span data-stu-id="4840d-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="4840d-114">512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxPixelShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="4840d-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4840d-115">Sombreador de vértices máximo</span><span class="sxs-lookup"><span data-stu-id="4840d-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="4840d-116">512 como mínimo y hasta el número de ranuras de D3DCAPS9. MaxVertexShader30InstructionSlots (vea <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="4840d-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4840d-117">Perfiles del sombreador</span><span class="sxs-lookup"><span data-stu-id="4840d-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="4840d-118">ps_3_0, vs_3_0</span><span class="sxs-lookup"><span data-stu-id="4840d-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4840d-119">Para obtener más información sobre los sombreadores de modelo 3, vea:</span><span class="sxs-lookup"><span data-stu-id="4840d-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="4840d-120">Sombreador de píxeles 3,0</span><span class="sxs-lookup"><span data-stu-id="4840d-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="4840d-121">Sombreador de vértices 3,0</span><span class="sxs-lookup"><span data-stu-id="4840d-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="4840d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4840d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4840d-123">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="4840d-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 