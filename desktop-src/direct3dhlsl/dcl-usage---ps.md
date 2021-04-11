---
title: dcl_semantics (SM3-PS ASM)
description: Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149432"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="ba21e-103">\_semántica de DCL (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="ba21e-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="ba21e-104">Declare la asociación entre la salida del sombreador de vértices y la entrada del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ba21e-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba21e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba21e-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="ba21e-106">\_semántica de DCL \[ \_ centroide \] DST \[ . Write \_ Mask\]</span><span class="sxs-lookup"><span data-stu-id="ba21e-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="ba21e-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="ba21e-107">Where:</span></span>

-   <span data-ttu-id="ba21e-108">\_semántica: identifica el uso de datos previsto y puede ser cualquiera de los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (sin el \_ prefijo D3DDECLUSAGE).</span><span class="sxs-lookup"><span data-stu-id="ba21e-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="ba21e-109">Además, se puede anexar un índice de entero a la semántica para distinguir los parámetros que utilizan una semántica similar.</span><span class="sxs-lookup"><span data-stu-id="ba21e-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="ba21e-110">\[\_[Centroide](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] es un modificador de instrucción opcional.</span><span class="sxs-lookup"><span data-stu-id="ba21e-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="ba21e-111">Es compatible con \_ las instrucciones de uso de DCL que declaran los registros de entrada y las instrucciones de búsqueda de texturas.</span><span class="sxs-lookup"><span data-stu-id="ba21e-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="ba21e-112">El centroide se anexa sin espacio.</span><span class="sxs-lookup"><span data-stu-id="ba21e-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="ba21e-113">DST: registro de destino.</span><span class="sxs-lookup"><span data-stu-id="ba21e-113">dst: destination register.</span></span> <span data-ttu-id="ba21e-114">Vea [registros de PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="ba21e-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="ba21e-115">escribir \_ máscara: el mismo registro de salida se puede declarar varias veces, cada vez con una máscara de escritura única (por lo que se pueden aplicar diferentes semánticas a componentes individuales).</span><span class="sxs-lookup"><span data-stu-id="ba21e-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="ba21e-116">Sin embargo, no se puede usar la misma semántica varias veces en una declaración.</span><span class="sxs-lookup"><span data-stu-id="ba21e-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="ba21e-117">Esto significa que los vectores deben tener cuatro componentes o menos y no pueden pasar por los límites de registro de cuatro componentes (registros de salida individuales).</span><span class="sxs-lookup"><span data-stu-id="ba21e-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="ba21e-118">Cuando \_ se usa la semántica psize, debe tener una máscara de escritura completa porque se considera un escalar.</span><span class="sxs-lookup"><span data-stu-id="ba21e-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="ba21e-119">Cuando \_ se usa la semántica de posición, debe tener una máscara de escritura completa porque se deben escribir los cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="ba21e-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba21e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba21e-120">Remarks</span></span>



| <span data-ttu-id="ba21e-121">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ba21e-121">Pixel shader versions</span></span> | <span data-ttu-id="ba21e-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="ba21e-122">1\_1</span></span> | <span data-ttu-id="ba21e-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="ba21e-123">1\_2</span></span> | <span data-ttu-id="ba21e-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ba21e-124">1\_3</span></span> | <span data-ttu-id="ba21e-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="ba21e-125">1\_4</span></span> | <span data-ttu-id="ba21e-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ba21e-126">2\_0</span></span> | <span data-ttu-id="ba21e-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ba21e-127">2\_x</span></span> | <span data-ttu-id="ba21e-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ba21e-128">2\_sw</span></span> | <span data-ttu-id="ba21e-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ba21e-129">3\_0</span></span> | <span data-ttu-id="ba21e-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ba21e-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ba21e-131">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="ba21e-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="ba21e-132">x</span><span class="sxs-lookup"><span data-stu-id="ba21e-132">x</span></span>    | <span data-ttu-id="ba21e-133">x</span><span class="sxs-lookup"><span data-stu-id="ba21e-133">x</span></span>     |



 

<span data-ttu-id="ba21e-134">Todas \_ las instrucciones de uso de DCL deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="ba21e-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="ba21e-135">Ejemplos de declaraciones</span><span class="sxs-lookup"><span data-stu-id="ba21e-135">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ba21e-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba21e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba21e-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ba21e-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="ba21e-138">[Ejemplo antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ba21e-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 