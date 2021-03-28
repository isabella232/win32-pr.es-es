---
title: Modificadores de instrucciones (HLSL VS Reference)
description: Modificadores de instrucciones
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104487199"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="a2d82-103">Modificadores de instrucciones (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="a2d82-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="a2d82-104">Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a2d82-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="a2d82-105">\_sábado</span><span class="sxs-lookup"><span data-stu-id="a2d82-105">\_sat</span></span>

<span data-ttu-id="a2d82-106">Satura (o fija) el resultado de la instrucción en \[ 0, 1 \] intervalo antes de escribir en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="a2d82-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="a2d82-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a2d82-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="a2d82-108">Donde:</span><span class="sxs-lookup"><span data-stu-id="a2d82-108">Where:</span></span>

<span data-ttu-id="a2d82-109">DST = abrazadera \_ entre \_ 0 \_ y \_ 1 (src0 + SRC1)</span><span class="sxs-lookup"><span data-stu-id="a2d82-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="a2d82-110">El \_ modificador de instrucciones SAT no cuesta ninguna ranura de instrucciones adicional.</span><span class="sxs-lookup"><span data-stu-id="a2d82-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="a2d82-111">Si se admite, el \_ modificador de instrucciones de SAT se puede usar con cualquier instrucción excepto: [FRC-vs](frc---vs.md), [sincos (-vs](sincos---vs.md)y [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="a2d82-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="a2d82-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a2d82-112">Vertex shader versions</span></span> | <span data-ttu-id="a2d82-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="a2d82-113">1\_1</span></span> | <span data-ttu-id="a2d82-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2d82-114">2\_0</span></span> | <span data-ttu-id="a2d82-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a2d82-115">2\_x</span></span> | <span data-ttu-id="a2d82-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2d82-116">2\_sw</span></span> | <span data-ttu-id="a2d82-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a2d82-117">3\_0</span></span> | <span data-ttu-id="a2d82-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a2d82-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a2d82-119">\_sábado</span><span class="sxs-lookup"><span data-stu-id="a2d82-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="a2d82-120">x</span><span class="sxs-lookup"><span data-stu-id="a2d82-120">x</span></span>    | <span data-ttu-id="a2d82-121">x</span><span class="sxs-lookup"><span data-stu-id="a2d82-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a2d82-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2d82-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d82-123">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a2d82-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




