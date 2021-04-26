---
title: dcl_semantics (sm3 - ps asm)
description: Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 178b31a386a7ae4aa266ac33ddbb1ee5c842f2d1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997172"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="fb142-103">semántica de dcl \_ (sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="fb142-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="fb142-104">Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="fb142-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb142-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb142-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="fb142-106">dcl \_ semantics \[ \_ centroid \] dst \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="fb142-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="fb142-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="fb142-107">Where:</span></span>

-   <span data-ttu-id="fb142-108">\_semántica: identifica el uso de datos previsto y puede ser cualquiera de los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sin el prefijo D3DDECLUSAGE). \_</span><span class="sxs-lookup"><span data-stu-id="fb142-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="fb142-109">Además, se puede anexar un índice entero a la semántica para distinguir los parámetros que usan una semántica similar.</span><span class="sxs-lookup"><span data-stu-id="fb142-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="fb142-110">\[\_[Centroide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] es un modificador de instrucción opcional.</span><span class="sxs-lookup"><span data-stu-id="fb142-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="fb142-111">Se admite en las instrucciones de uso de dcl que declaran los registros de entrada \_ y en las instrucciones de búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="fb142-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="fb142-112">El centroide se anexa sin espacio.</span><span class="sxs-lookup"><span data-stu-id="fb142-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="fb142-113">dst: registro de destino.</span><span class="sxs-lookup"><span data-stu-id="fb142-113">dst: destination register.</span></span> <span data-ttu-id="fb142-114">Vea [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="fb142-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="fb142-115">máscara de escritura: el mismo registro de salida se puede declarar varias veces, cada vez con una máscara de escritura única (por lo que se puede aplicar una semántica diferente \_ a componentes individuales).</span><span class="sxs-lookup"><span data-stu-id="fb142-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="fb142-116">Sin embargo, la misma semántica no se puede usar varias veces en una declaración.</span><span class="sxs-lookup"><span data-stu-id="fb142-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="fb142-117">Esto significa que los vectores deben ser cuatro componentes o menos y no pueden pasar por los límites del registro de cuatro componentes (registros de salida individuales).</span><span class="sxs-lookup"><span data-stu-id="fb142-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="fb142-118">Cuando se \_ usa la semántica psize, debe tener una máscara de escritura completa porque se considera escalar.</span><span class="sxs-lookup"><span data-stu-id="fb142-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="fb142-119">Cuando se usa la semántica de posición, debe tener máscara de escritura completa porque se deben escribir \_ los cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="fb142-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb142-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb142-120">Remarks</span></span>



| <span data-ttu-id="fb142-121">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fb142-121">Pixel shader versions</span></span> | <span data-ttu-id="fb142-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="fb142-122">1\_1</span></span> | <span data-ttu-id="fb142-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="fb142-123">1\_2</span></span> | <span data-ttu-id="fb142-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fb142-124">1\_3</span></span> | <span data-ttu-id="fb142-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="fb142-125">1\_4</span></span> | <span data-ttu-id="fb142-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fb142-126">2\_0</span></span> | <span data-ttu-id="fb142-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fb142-127">2\_x</span></span> | <span data-ttu-id="fb142-128">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fb142-128">2\_sw</span></span> | <span data-ttu-id="fb142-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fb142-129">3\_0</span></span> | <span data-ttu-id="fb142-130">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fb142-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fb142-131">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="fb142-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="fb142-132">x</span><span class="sxs-lookup"><span data-stu-id="fb142-132">x</span></span>    | <span data-ttu-id="fb142-133">x</span><span class="sxs-lookup"><span data-stu-id="fb142-133">x</span></span>     |



 

<span data-ttu-id="fb142-134">Todas las instrucciones de uso de dcl \_ deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="fb142-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="fb142-135">Ejemplos de declaración</span><span class="sxs-lookup"><span data-stu-id="fb142-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="fb142-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb142-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb142-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fb142-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="fb142-138">[Ejemplo de suavizado de contorno](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="fb142-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
