---
title: vs_2_0
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983734"
---
# <a name="vs_2_0"></a><span data-ttu-id="3dc60-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dc60-105">vs\_2\_0</span></span>

<span data-ttu-id="3dc60-106">Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="3dc60-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="3dc60-107">Registra datos de transferencia dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="3dc60-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="3dc60-108">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="3dc60-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="3dc60-109">[Instrucciones: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="3dc60-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="3dc60-110">[Registros: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) muestra los distintos tipos de registros utilizados por el sombreador de vértices Alu.</span><span class="sxs-lookup"><span data-stu-id="3dc60-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="3dc60-111">Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.</span><span class="sxs-lookup"><span data-stu-id="3dc60-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="3dc60-112">Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="3dc60-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="3dc60-113">[El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.</span><span class="sxs-lookup"><span data-stu-id="3dc60-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="3dc60-114">[El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="3dc60-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="3dc60-115">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="3dc60-115">Instruction Count</span></span>

<span data-ttu-id="3dc60-116">Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas.</span><span class="sxs-lookup"><span data-stu-id="3dc60-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="3dc60-117">El número de instrucciones que se ejecutan puede ser mucho mayor (debido al soporte de bucle/REP) y está limitado por D3DCAPS9. MaxVShaderInstructionsExecuted, que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="3dc60-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dc60-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3dc60-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dc60-119">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="3dc60-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




