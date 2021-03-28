---
title: DP3-PS
description: Calcula el producto de tres componentes de los registros de origen. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986363"
---
# <a name="dp3---ps"></a><span data-ttu-id="8af93-104">DP3-PS</span><span class="sxs-lookup"><span data-stu-id="8af93-104">dp3 - ps</span></span>

<span data-ttu-id="8af93-105">Calcula el producto de tres componentes de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="8af93-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af93-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8af93-106">Syntax</span></span>



| <span data-ttu-id="8af93-107">DP3 DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="8af93-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8af93-108">, donde</span><span class="sxs-lookup"><span data-stu-id="8af93-108">where</span></span>

-   <span data-ttu-id="8af93-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8af93-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8af93-110">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8af93-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8af93-111">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8af93-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af93-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8af93-112">Remarks</span></span>



| <span data-ttu-id="8af93-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8af93-113">Pixel shader versions</span></span> | <span data-ttu-id="8af93-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8af93-114">1\_1</span></span> | <span data-ttu-id="8af93-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="8af93-115">1\_2</span></span> | <span data-ttu-id="8af93-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8af93-116">1\_3</span></span> | <span data-ttu-id="8af93-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="8af93-117">1\_4</span></span> | <span data-ttu-id="8af93-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8af93-118">2\_0</span></span> | <span data-ttu-id="8af93-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8af93-119">2\_x</span></span> | <span data-ttu-id="8af93-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8af93-120">2\_sw</span></span> | <span data-ttu-id="8af93-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8af93-121">3\_0</span></span> | <span data-ttu-id="8af93-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8af93-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8af93-123">dp3</span><span class="sxs-lookup"><span data-stu-id="8af93-123">dp3</span></span>                   | <span data-ttu-id="8af93-124">x</span><span class="sxs-lookup"><span data-stu-id="8af93-124">x</span></span>    | <span data-ttu-id="8af93-125">x</span><span class="sxs-lookup"><span data-stu-id="8af93-125">x</span></span>    | <span data-ttu-id="8af93-126">x</span><span class="sxs-lookup"><span data-stu-id="8af93-126">x</span></span>    | <span data-ttu-id="8af93-127">x</span><span class="sxs-lookup"><span data-stu-id="8af93-127">x</span></span>    | <span data-ttu-id="8af93-128">x</span><span class="sxs-lookup"><span data-stu-id="8af93-128">x</span></span>    | <span data-ttu-id="8af93-129">x</span><span class="sxs-lookup"><span data-stu-id="8af93-129">x</span></span>    | <span data-ttu-id="8af93-130">x</span><span class="sxs-lookup"><span data-stu-id="8af93-130">x</span></span>     | <span data-ttu-id="8af93-131">x</span><span class="sxs-lookup"><span data-stu-id="8af93-131">x</span></span>    | <span data-ttu-id="8af93-132">x</span><span class="sxs-lookup"><span data-stu-id="8af93-132">x</span></span>     |



 

<span data-ttu-id="8af93-133">En el fragmento de código siguiente se muestran las operaciones realizadas:</span><span class="sxs-lookup"><span data-stu-id="8af93-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="8af93-134">Esta instrucción se ejecuta en la canalización de vectores, escribiendo siempre en los canales de color.</span><span class="sxs-lookup"><span data-stu-id="8af93-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="8af93-135">En el caso de \_ la versión 4, esta instrucción todavía utiliza la canalización de vectores, pero puede escribir en cualquier canal.</span><span class="sxs-lookup"><span data-stu-id="8af93-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="8af93-136">Una instrucción con una máscara de escritura de Register. RGB (. XYZ) de destino puede coexistir con DP3, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="8af93-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="8af93-137">La instrucción DP3 se puede modificar mediante el uso del modificador de argumento de entrada de [ajuste de escala firmado del registro de origen](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) aplicado a sus argumentos de entrada si aún no se han expandido al intervalo dinámico con firma.</span><span class="sxs-lookup"><span data-stu-id="8af93-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="8af93-138">En el caso de un sombreador de iluminación, el modificador de instrucciones saturadas ( \_ SAT) suele usarse para fijar los valores negativos a negro, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8af93-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="8af93-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8af93-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af93-140">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8af93-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




