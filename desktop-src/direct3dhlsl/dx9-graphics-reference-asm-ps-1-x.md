---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: El ensamblador de sombreador de píxeles se compone de un conjunto de instrucciones que operan en los datos de píxeles contenidos en los registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268242"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="a5e09-103">PS \_ 1 \_ , PS \_ 1 \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a5e09-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="a5e09-104">El ensamblador de sombreador de píxeles se compone de un conjunto de instrucciones que operan en los datos de píxeles contenidos en los registros.</span><span class="sxs-lookup"><span data-stu-id="a5e09-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="a5e09-105">Las operaciones se expresan como instrucciones que se componen de un operador y de uno o varios operandos.</span><span class="sxs-lookup"><span data-stu-id="a5e09-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="a5e09-106">Las instrucciones usan registros para transferir datos dentro y fuera del sombreador de píxeles ALU.</span><span class="sxs-lookup"><span data-stu-id="a5e09-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="a5e09-107">Los registros también se pueden usar en algunas instrucciones para almacenar resultados temporales.</span><span class="sxs-lookup"><span data-stu-id="a5e09-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="a5e09-108">La compatibilidad de HLSL con el sombreador de píxeles 1. x está en desuso.</span><span class="sxs-lookup"><span data-stu-id="a5e09-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="a5e09-109">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a5e09-109">Instructions</span></span>

<span data-ttu-id="a5e09-110">Hay dos categorías principales de instrucciones del sombreador de píxeles: Instrucciones aritméticas e instrucciones de direccionamiento de texturas.</span><span class="sxs-lookup"><span data-stu-id="a5e09-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="a5e09-111">Las instrucciones aritméticas modifican los datos de color.</span><span class="sxs-lookup"><span data-stu-id="a5e09-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="a5e09-112">Las operaciones de direccionamiento de texturas procesan datos de coordenadas de textura y, en la mayoría de los casos, muestra una textura.</span><span class="sxs-lookup"><span data-stu-id="a5e09-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="a5e09-113">Las instrucciones del sombreador de píxeles se ejecutan por píxel; es decir, no tienen ningún conocimiento de otros píxeles en la canalización.</span><span class="sxs-lookup"><span data-stu-id="a5e09-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="a5e09-114">Las instrucciones de direccionamiento de texturas consumen una ranura, pero las instrucciones aritméticas se pueden emparejar para habilitar los componentes de color (RGB) y una instrucción de componente alfa en una sola ranura.</span><span class="sxs-lookup"><span data-stu-id="a5e09-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="a5e09-115">[las \_ instrucciones PS 1 \_ , PS 1 \_ \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene una lista de las instrucciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5e09-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="a5e09-116">Cuando se habilita el muestreo múltiple, los sombreadores de píxeles solo se ejecutan una vez por píxel, no una vez para cada subpíxel.</span><span class="sxs-lookup"><span data-stu-id="a5e09-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="a5e09-117">El muestreo múltiple solo aumenta la resolución de los bordes de polígono, así como las pruebas de profundidad y de estarcido.</span><span class="sxs-lookup"><span data-stu-id="a5e09-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="a5e09-118">Por ejemplo, si está habilitado el muestreo múltiple de 3x3 y se detecta que un triángulo que se está rasterizando abarca cinco de los nueve subpíxeles de un píxel determinado, el sombreador de píxeles se ejecuta una vez y se aplica el mismo resultado de color a los cinco subpíxeles.</span><span class="sxs-lookup"><span data-stu-id="a5e09-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="a5e09-119">Registros</span><span class="sxs-lookup"><span data-stu-id="a5e09-119">Registers</span></span>

<span data-ttu-id="a5e09-120">[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) muestra los distintos registros utilizados por el sombreador Alu.</span><span class="sxs-lookup"><span data-stu-id="a5e09-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="a5e09-121">Modificadores</span><span class="sxs-lookup"><span data-stu-id="a5e09-121">Modifiers</span></span>

<span data-ttu-id="a5e09-122">Los [modificadores para PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) se pueden usar para cambiar la funcionalidad de una instrucción o los datos se leen o se escriben en un registro.</span><span class="sxs-lookup"><span data-stu-id="a5e09-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="a5e09-123">Direct3D 9 requiere cálculos intermedios para mantener una precisión de 8 bits como mínimo para todos los formatos de superficie.</span><span class="sxs-lookup"><span data-stu-id="a5e09-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="a5e09-124">Se recomienda la precisión superior (12 bits) para las matemáticas en la fase y la saturación a 8 bits entre las fases de textura.</span><span class="sxs-lookup"><span data-stu-id="a5e09-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="a5e09-125">No se admiten los modos de redondeo ni las excepciones modificables.</span><span class="sxs-lookup"><span data-stu-id="a5e09-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="a5e09-126">La multiplicación debe admitirse con una precisión de un paso a más cercano para mantener una pérdida de precisión mínima.</span><span class="sxs-lookup"><span data-stu-id="a5e09-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="a5e09-127">Recuento de muestras</span><span class="sxs-lookup"><span data-stu-id="a5e09-127">Sampler Count</span></span>

<span data-ttu-id="a5e09-128">El número de muestras de textura disponibles es:</span><span class="sxs-lookup"><span data-stu-id="a5e09-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="a5e09-129">Para PS \_ 1 \_ 0-PS \_ 1 \_ 3, el máximo es 4.</span><span class="sxs-lookup"><span data-stu-id="a5e09-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="a5e09-130">Para PS \_ 1 \_ 4, el máximo es 6.</span><span class="sxs-lookup"><span data-stu-id="a5e09-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5e09-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5e09-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e09-132">Sombreadores de píxeles</span><span class="sxs-lookup"><span data-stu-id="a5e09-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




