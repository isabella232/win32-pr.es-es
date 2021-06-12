---
title: ps_2_0
description: Obtenga información ps_2_0, un sombreador de píxeles programable, que se forma de un conjunto de instrucciones que funcionan con datos de píxeles.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010988"
---
# <a name="ps_2_0"></a><span data-ttu-id="ccbc4-103">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ccbc4-103">ps\_2\_0</span></span>

<span data-ttu-id="ccbc4-104">Un sombreador de píxeles programable se forma de un conjunto de instrucciones que funcionan con datos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="ccbc4-105">Registra la transferencia de datos dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="ccbc4-106">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="ccbc4-107">[ps \_ 2 \_ 0 Instructions contiene](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="ccbc4-108">[ps \_ 2 \_ 0 Registros enumera](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) los diferentes tipos de registros usados por el sombreador de vértices ALU.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="ccbc4-109">[Modificadores](dx9-graphics-reference-asm-ps-registers-modifiers.md) Se usan para modificar el funcionamiento de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="ccbc4-110">[La máscara de escritura del registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determina qué componentes del registro de destino se escriben.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="ccbc4-111">[Los modificadores de registro de origen del sombreador de](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) píxeles modifican los datos de registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="ccbc4-112">[Source Register Swling proporciona](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="ccbc4-113">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="ccbc4-113">Instruction Count</span></span>

<span data-ttu-id="ccbc4-114">Los sombreadores tienen restricciones para el número máximo de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="ccbc4-115">Total de ranuras de instrucción: 96 (64 aritméticas y 32 texturas).</span><span class="sxs-lookup"><span data-stu-id="ccbc4-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="ccbc4-116">Sampler Count</span><span class="sxs-lookup"><span data-stu-id="ccbc4-116">Sampler Count</span></span>

<span data-ttu-id="ccbc4-117">El número de muestreadores de textura disponibles es 16.</span><span class="sxs-lookup"><span data-stu-id="ccbc4-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccbc4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccbc4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccbc4-119">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="ccbc4-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




