---
title: ps_2_0
description: Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983614"
---
# <a name="ps_2_0"></a><span data-ttu-id="b82e2-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b82e2-105">ps\_2\_0</span></span>

<span data-ttu-id="b82e2-106">Un sombreador de píxeles programable se compone de un conjunto de instrucciones que operan en datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b82e2-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="b82e2-107">Registra datos de transferencia dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="b82e2-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="b82e2-108">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="b82e2-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="b82e2-109">[las \_ instrucciones de PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contienen una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="b82e2-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="b82e2-110">en los [registros de PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) se enumeran los distintos tipos de registros utilizados por el sombreador de vértices Alu.</span><span class="sxs-lookup"><span data-stu-id="b82e2-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="b82e2-111">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se utilizan para modificar la forma en que funciona una instrucción.</span><span class="sxs-lookup"><span data-stu-id="b82e2-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="b82e2-112">La [máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina los componentes del registro de destino que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="b82e2-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="b82e2-113">Los [modificadores de registro de origen del sombreador de píxeles](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="b82e2-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="b82e2-114">[El registro de origen permutación](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.</span><span class="sxs-lookup"><span data-stu-id="b82e2-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="b82e2-115">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="b82e2-115">Instruction Count</span></span>

<span data-ttu-id="b82e2-116">Los sombreadores tienen restricciones para el número máximo de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b82e2-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="b82e2-117">Total de ranuras de instrucciones: 96 (64 aritméticos y texturas de 32).</span><span class="sxs-lookup"><span data-stu-id="b82e2-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="b82e2-118">Recuento de muestras</span><span class="sxs-lookup"><span data-stu-id="b82e2-118">Sampler Count</span></span>

<span data-ttu-id="b82e2-119">El número de muestras de textura disponibles es 16.</span><span class="sxs-lookup"><span data-stu-id="b82e2-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b82e2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b82e2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b82e2-121">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="b82e2-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




