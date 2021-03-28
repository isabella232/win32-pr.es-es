---
title: texm3x3-PS
description: Realiza una multiplicación de una matriz de 3x3 cuando se usa junto con dos instrucciones texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983838"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="e8991-103">texm3x3-PS</span><span class="sxs-lookup"><span data-stu-id="e8991-103">texm3x3 - ps</span></span>

<span data-ttu-id="e8991-104">Realiza una multiplicación de una matriz de 3x3 cuando se usa junto con dos instrucciones [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="e8991-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8991-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8991-105">Syntax</span></span>



| <span data-ttu-id="e8991-106">texm3x3 DST, src</span><span class="sxs-lookup"><span data-stu-id="e8991-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="e8991-107">, donde</span><span class="sxs-lookup"><span data-stu-id="e8991-107">where</span></span>

-   <span data-ttu-id="e8991-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e8991-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e8991-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="e8991-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8991-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8991-110">Remarks</span></span>



| <span data-ttu-id="e8991-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e8991-111">Pixel shader versions</span></span> | <span data-ttu-id="e8991-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e8991-112">1\_1</span></span> | <span data-ttu-id="e8991-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e8991-113">1\_2</span></span> | <span data-ttu-id="e8991-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e8991-114">1\_3</span></span> | <span data-ttu-id="e8991-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e8991-115">1\_4</span></span> | <span data-ttu-id="e8991-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8991-116">2\_0</span></span> | <span data-ttu-id="e8991-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e8991-117">2\_x</span></span> | <span data-ttu-id="e8991-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e8991-118">2\_sw</span></span> | <span data-ttu-id="e8991-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e8991-119">3\_0</span></span> | <span data-ttu-id="e8991-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e8991-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e8991-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="e8991-121">texm3x3</span></span>               |      | <span data-ttu-id="e8991-122">x</span><span class="sxs-lookup"><span data-stu-id="e8991-122">x</span></span>    | <span data-ttu-id="e8991-123">x</span><span class="sxs-lookup"><span data-stu-id="e8991-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e8991-124">Esta instrucción es la misma que la instrucción [texm3x3tex-PS](texm3x3tex---ps.md) , sin la búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="e8991-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="e8991-125">Esta instrucción se utiliza como final de tres instrucciones que representan una operación de multiplicación de una matriz de 3x3.</span><span class="sxs-lookup"><span data-stu-id="e8991-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="e8991-126">La matriz de 3x3 se compone de las coordenadas de textura de la tercera fase de textura y de las dos fases de textura anteriores.</span><span class="sxs-lookup"><span data-stu-id="e8991-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="e8991-127">Se omite cualquier textura asignada a cualquiera de las tres fases de textura.</span><span class="sxs-lookup"><span data-stu-id="e8991-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="e8991-128">Esta instrucción debe usarse con dos instrucciones texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="e8991-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="e8991-129">Los registros de textura deben seguir la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="e8991-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="e8991-130">Aquí encontrará más detalles sobre cómo se realiza la multiplicación de 3x3.</span><span class="sxs-lookup"><span data-stu-id="e8991-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="e8991-131">La primera instrucción texm3x3pad realiza la primera fila de Multiply para buscar u<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="e8991-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="e8991-132">u<sup>'</sup> = TextureCoordinates (Stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e8991-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e8991-133">La segunda instrucción texm3x3pad realiza la segunda fila de la multiplicación para encontrar v<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="e8991-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="e8991-134">v<sup>'</sup> = TextureCoordinates (Stage m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e8991-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e8991-135">La instrucción texm3x3tex realiza la tercera fila de Multiply para buscar w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="e8991-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="e8991-136">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e8991-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="e8991-137">Coloque el resultado de la multiplicación de la matriz en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e8991-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="e8991-138">t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span><span class="sxs-lookup"><span data-stu-id="e8991-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8991-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8991-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8991-140">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e8991-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




