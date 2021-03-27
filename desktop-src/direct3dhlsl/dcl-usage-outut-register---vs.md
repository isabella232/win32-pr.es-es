---
title: dcl_usage salida (SM1, SM2, SM3-vs ASM)
description: Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para el color, ocho para la textura, uno para la posición y otro para la niebla y el tamaño de los puntos).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997129"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="00ee9-103">\_salida de uso de DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="00ee9-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="00ee9-104">Los distintos tipos de registros de salida se han contraído en doce registros de salida (dos para el color, ocho para la textura, uno para la posición y otro para la niebla y el tamaño de los puntos).</span><span class="sxs-lookup"><span data-stu-id="00ee9-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="00ee9-105">Se pueden usar para cualquier elemento que el usuario quiera interpolar para el sombreador de píxeles: coordenadas de textura, colores, niebla, etc.</span><span class="sxs-lookup"><span data-stu-id="00ee9-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="00ee9-106">Los registros de salida requieren declaraciones que incluyen la semántica.</span><span class="sxs-lookup"><span data-stu-id="00ee9-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="00ee9-107">Por ejemplo, los registros de posición y de tamaño de punto antiguos se reemplazan declarando un registro de salida con una posición o semántica de tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="00ee9-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="00ee9-108">De los doce registros de salida, los diez (no necesariamente O0 a O9) tienen cuatro componentes (xyzw), otro se debe declarar como Position (y también debe incluir los cuatro componentes) y, opcionalmente, uno más puede ser un tamaño de punto escalar.</span><span class="sxs-lookup"><span data-stu-id="00ee9-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ee9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00ee9-109">Syntax</span></span>

<span data-ttu-id="00ee9-110">La sintaxis para declarar registros de salida es similar a las declaraciones del registro de entrada:</span><span class="sxs-lookup"><span data-stu-id="00ee9-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="00ee9-111">semántica de DCL \_ o \[ . máscara de escritura \_\]</span><span class="sxs-lookup"><span data-stu-id="00ee9-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="00ee9-112">Donde:</span><span class="sxs-lookup"><span data-stu-id="00ee9-112">Where:</span></span>

-   <span data-ttu-id="00ee9-113">la \_ semántica de DCL puede usar el mismo conjunto de semántica que para la declaración de entrada.</span><span class="sxs-lookup"><span data-stu-id="00ee9-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="00ee9-114">Los nombres semánticos proceden de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (y se emparejan con un índice, como position3).</span><span class="sxs-lookup"><span data-stu-id="00ee9-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="00ee9-115">Siempre debe haber un registro de salida con la semántica positiont0 cuando no se usa para el procesamiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="00ee9-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="00ee9-116">La semántica positiont0 y la semántica pointsize0 son las únicas que tienen un significado más allá, simplemente permiten la vinculación de los sombreadores de vértices a píxeles.</span><span class="sxs-lookup"><span data-stu-id="00ee9-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="00ee9-117">En el caso de los sombreadores con control de flujo, se supone que se declara el resultado peor de los casos.</span><span class="sxs-lookup"><span data-stu-id="00ee9-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="00ee9-118">No hay valores predeterminados si un sombreador no genera realmente lo que declara debe (debido al control de flujo).</span><span class="sxs-lookup"><span data-stu-id="00ee9-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="00ee9-119">o es un registro de salida.</span><span class="sxs-lookup"><span data-stu-id="00ee9-119">o is an output register.</span></span> <span data-ttu-id="00ee9-120">Consulte [ \_ registros de salida](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="00ee9-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="00ee9-121">escribir \_ máscara indica el mismo registro de salida que se puede declarar varias veces (de modo que se pueden aplicar diferentes semánticas a componentes individuales), cada vez con una máscara de escritura única.</span><span class="sxs-lookup"><span data-stu-id="00ee9-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="00ee9-122">Sin embargo, no se puede usar la misma semántica varias veces en una declaración.</span><span class="sxs-lookup"><span data-stu-id="00ee9-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="00ee9-123">Esto significa que los vectores deben tener cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros individuales).</span><span class="sxs-lookup"><span data-stu-id="00ee9-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="00ee9-124">Cuando se usa la semántica de tamaño de punto, debe tener una máscara de escritura completa porque se considera un escalar.</span><span class="sxs-lookup"><span data-stu-id="00ee9-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="00ee9-125">Cuando se usa la semántica de posición, debe tener una máscara de escritura completa porque se deben escribir los cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="00ee9-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ee9-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00ee9-126">Remarks</span></span>



| <span data-ttu-id="00ee9-127">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="00ee9-127">Vertex shader versions</span></span> | <span data-ttu-id="00ee9-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="00ee9-128">3\_0</span></span> | <span data-ttu-id="00ee9-129">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="00ee9-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="00ee9-130">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="00ee9-130">dcl\_usage</span></span>             | <span data-ttu-id="00ee9-131">x</span><span class="sxs-lookup"><span data-stu-id="00ee9-131">x</span></span>    | <span data-ttu-id="00ee9-132">x</span><span class="sxs-lookup"><span data-stu-id="00ee9-132">x</span></span>     |



 

<span data-ttu-id="00ee9-133">Todas las instrucciones de [ \_ uso de DCL](dcl-usage-input-register---vs.md) deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="00ee9-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="00ee9-134">Ejemplos de declaraciones</span><span class="sxs-lookup"><span data-stu-id="00ee9-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="00ee9-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00ee9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ee9-136">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="00ee9-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 