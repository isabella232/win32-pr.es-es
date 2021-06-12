---
title: vs_2_0
description: Obtenga información vs_2_0, un sombreador de vértices programable, que se forma de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010858"
---
# <a name="vs_2_0"></a><span data-ttu-id="64539-103">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64539-103">vs\_2\_0</span></span>

<span data-ttu-id="64539-104">Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="64539-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="64539-105">Registra la transferencia de datos dentro y fuera de la ALU.</span><span class="sxs-lookup"><span data-stu-id="64539-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="64539-106">Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.</span><span class="sxs-lookup"><span data-stu-id="64539-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="64539-107">[Instrucciones: frente \_ a \_ 2 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="64539-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="64539-108">[Registros: frente \_ a 2 \_ 0,](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) se enumeran los distintos tipos de registros usados por el sombreador de vértices ALU.</span><span class="sxs-lookup"><span data-stu-id="64539-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="64539-109">[Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.</span><span class="sxs-lookup"><span data-stu-id="64539-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="64539-110">[Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.</span><span class="sxs-lookup"><span data-stu-id="64539-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="64539-111">[Source Register Swling proporciona](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.</span><span class="sxs-lookup"><span data-stu-id="64539-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="64539-112">[El enmascaramiento de registros de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina qué componentes del registro de destino se escriben.</span><span class="sxs-lookup"><span data-stu-id="64539-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="64539-113">Recuento de instrucciones</span><span class="sxs-lookup"><span data-stu-id="64539-113">Instruction Count</span></span>

<span data-ttu-id="64539-114">Cada sombreador de vértices puede tener hasta 256 instrucciones almacenadas.</span><span class="sxs-lookup"><span data-stu-id="64539-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="64539-115">El número de instrucciones que se ejecutan puede ser mucho mayor (debido a la compatibilidad con bucles y réplicas) y D3DCAPS9. MaxVShaderInstructionsExecuted, que debe ser al menos 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="64539-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64539-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64539-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64539-117">Sombreadores de vértices</span><span class="sxs-lookup"><span data-stu-id="64539-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




