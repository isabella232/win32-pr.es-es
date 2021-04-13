---
title: texldd-PS
description: Muestrea una textura con entradas de degradado adicionales.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420740"
---
# <a name="texldd---ps"></a><span data-ttu-id="9a4e5-103">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="9a4e5-103">texldd - ps</span></span>

<span data-ttu-id="9a4e5-104">Muestrea una textura con entradas de degradado adicionales.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-104">Samples a texture with additional gradient inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a4e5-105">Syntax</span></span>



| <span data-ttu-id="9a4e5-106">texldd, DST, src0, SRC1, src2, src3</span><span class="sxs-lookup"><span data-stu-id="9a4e5-106">texldd, dst, src0, src1, src2, src3</span></span> |
|-------------------------------------|



 

<span data-ttu-id="9a4e5-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="9a4e5-107">Where:</span></span>

-   <span data-ttu-id="9a4e5-108">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-108">dst is a destination register.</span></span>
-   <span data-ttu-id="9a4e5-109">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-109">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="9a4e5-110">Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="9a4e5-110">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="9a4e5-111">SRC1 identifica los registros de la muestra de origen \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-111">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="9a4e5-112">La muestra le ha asociado una textura y un estado de control definido por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="9a4e5-112">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (ex.</span></span> <span data-ttu-id="9a4e5-113">D3DSAMP \_ MINFILTER).</span><span class="sxs-lookup"><span data-stu-id="9a4e5-113">D3DSAMP\_MINFILTER).</span></span>
-   <span data-ttu-id="9a4e5-114">src2 es un registro de origen de entrada que especifica el degradado x.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-114">src2 is an input source register that specifies the x gradient.</span></span>
-   <span data-ttu-id="9a4e5-115">src3 es un registro de origen de entrada que especifica el degradado y.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-115">src3 is an input source register that specifies the y gradient.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a4e5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a4e5-116">Remarks</span></span>



| <span data-ttu-id="9a4e5-117">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9a4e5-117">Pixel shader versions</span></span> | <span data-ttu-id="9a4e5-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="9a4e5-118">1\_1</span></span> | <span data-ttu-id="9a4e5-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="9a4e5-119">1\_2</span></span> | <span data-ttu-id="9a4e5-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9a4e5-120">1\_3</span></span> | <span data-ttu-id="9a4e5-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="9a4e5-121">1\_4</span></span> | <span data-ttu-id="9a4e5-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a4e5-122">2\_0</span></span> | <span data-ttu-id="9a4e5-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a4e5-123">2\_x</span></span> | <span data-ttu-id="9a4e5-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a4e5-124">2\_sw</span></span> | <span data-ttu-id="9a4e5-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a4e5-125">3\_0</span></span> | <span data-ttu-id="9a4e5-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a4e5-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9a4e5-127">texldd</span><span class="sxs-lookup"><span data-stu-id="9a4e5-127">texldd</span></span>                |      |      |      |      |      | <span data-ttu-id="9a4e5-128">x1 \*</span><span class="sxs-lookup"><span data-stu-id="9a4e5-128">x \*</span></span> | <span data-ttu-id="9a4e5-129">x</span><span class="sxs-lookup"><span data-stu-id="9a4e5-129">x</span></span>     | <span data-ttu-id="9a4e5-130">x</span><span class="sxs-lookup"><span data-stu-id="9a4e5-130">x</span></span>    | <span data-ttu-id="9a4e5-131">x</span><span class="sxs-lookup"><span data-stu-id="9a4e5-131">x</span></span>     |



 

<span data-ttu-id="9a4e5-132">\* Esta instrucción solo es compatible con la PS \_ 2 \_ a.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-132">\* This instruction is only supported by ps\_2\_a.</span></span> <span data-ttu-id="9a4e5-133">No es compatible con PS \_ 2 \_ b.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-133">It is not supported by ps\_2\_b.</span></span> <span data-ttu-id="9a4e5-134">Para obtener más información acerca de los perfiles, consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="9a4e5-134">For more information about profiles, see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).</span></span>

<span data-ttu-id="9a4e5-135">Esta instrucción muestrea una textura mediante las coordenadas de textura en src0, la muestra especificada por SRC1 y los degradados DSX y DSY provienen de src2 y src3.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-135">This instruction samples a texture using the texture coordinates at src0, the sampler specified by src1, and the gradients DSX and DSY coming from src2 and src3.</span></span> <span data-ttu-id="9a4e5-136">Los valores de degradado x e y se usan para seleccionar el nivel de mipmap adecuado de la textura para el muestreo.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-136">The x and y gradient values are used to select the appropriate mipmap level of the texture for sampling.</span></span>

<span data-ttu-id="9a4e5-137">Todos los orígenes admiten swizzles arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-137">All sources support arbitrary swizzles.</span></span>

<span data-ttu-id="9a4e5-138">Todas las máscaras de escritura son válidas en el destino.</span><span class="sxs-lookup"><span data-stu-id="9a4e5-138">All write masks are valid on the destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a4e5-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a4e5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a4e5-140">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9a4e5-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 