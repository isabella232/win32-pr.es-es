---
title: Registro de contadores de bucle (referencia de HLSL VS)
description: El único registro de este banco es el registro del contador de bucle actual (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420014"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="a0264-103">Registro de contadores de bucle (referencia de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="a0264-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="a0264-104">El único registro de este banco es el registro del contador de bucle actual (aL).</span><span class="sxs-lookup"><span data-stu-id="a0264-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="a0264-105">Se incrementa automáticamente en cada ejecución del [bucle, en lugar](loop---vs.md)de. [ENDLOOP: bloque vs](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="a0264-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="a0264-106">Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido para usarlo fuera del bucle.</span><span class="sxs-lookup"><span data-stu-id="a0264-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0264-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0264-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0264-108">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a0264-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




