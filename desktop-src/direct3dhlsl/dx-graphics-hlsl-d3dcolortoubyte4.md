---
title: D3DCOLORtoUBYTE4
description: Convierte un vector de punto flotante, 4D establecido por un D3DCOLOR en UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- HLSL de D3DCOLORtoUBYTE4
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533459"
---
# <a name="d3dcolortoubyte4"></a><span data-ttu-id="efee1-104">D3DCOLORtoUBYTE4</span><span class="sxs-lookup"><span data-stu-id="efee1-104">D3DCOLORtoUBYTE4</span></span>

<span data-ttu-id="efee1-105">Convierte un vector de punto flotante, 4D establecido por un D3DCOLOR en UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="efee1-105">Converts a floating-point, 4D vector set by a D3DCOLOR to a UBYTE4.</span></span>



| <span data-ttu-id="efee1-106">*RET* D3DCOLORtoUBYTE4 (*x*)</span><span class="sxs-lookup"><span data-stu-id="efee1-106">*ret* D3DCOLORtoUBYTE4(*x*)</span></span> |
|-----------------------------|



 

<span data-ttu-id="efee1-107">Esta función swizzles y escala los componentes del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="efee1-107">This function swizzles and scales components of the *x* parameter.</span></span> <span data-ttu-id="efee1-108">Utilice esta función para compensar la falta de compatibilidad con UBYTE4 en algún hardware.</span><span class="sxs-lookup"><span data-stu-id="efee1-108">Use this function to compensate for the lack of UBYTE4 support in some hardware.</span></span>

## <a name="parameters"></a><span data-ttu-id="efee1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efee1-109">Parameters</span></span>



| <span data-ttu-id="efee1-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="efee1-110">Item</span></span>                                                   | <span data-ttu-id="efee1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="efee1-111">Description</span></span>                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="efee1-112"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="efee1-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="efee1-113">\[en \] el Vector4 de punto flotante que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="efee1-113">\[in\] The floating-point vector4 to convert.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="efee1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efee1-114">Return Value</span></span>

<span data-ttu-id="efee1-115">Representación UBYTE4 del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="efee1-115">The UBYTE4 representation of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="efee1-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="efee1-116">Type Description</span></span>



| <span data-ttu-id="efee1-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="efee1-117">Name</span></span>  | [<span data-ttu-id="efee1-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="efee1-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="efee1-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="efee1-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="efee1-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="efee1-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="efee1-121">*x*</span><span class="sxs-lookup"><span data-stu-id="efee1-121">*x*</span></span>   | [<span data-ttu-id="efee1-122">**medios**</span><span class="sxs-lookup"><span data-stu-id="efee1-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="efee1-123">**float**</span><span class="sxs-lookup"><span data-stu-id="efee1-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="efee1-124">4</span><span class="sxs-lookup"><span data-stu-id="efee1-124">4</span></span>    |
| <span data-ttu-id="efee1-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="efee1-125">*ret*</span></span> | [<span data-ttu-id="efee1-126">**medios**</span><span class="sxs-lookup"><span data-stu-id="efee1-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="efee1-127">**integer**</span><span class="sxs-lookup"><span data-stu-id="efee1-127">**integer**</span></span>](/windows/desktop/WinProg/windows-data-types)                      | <span data-ttu-id="efee1-128">4</span><span class="sxs-lookup"><span data-stu-id="efee1-128">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="efee1-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="efee1-129">Minimum Shader Model</span></span>

<span data-ttu-id="efee1-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="efee1-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="efee1-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="efee1-131">Shader Model</span></span>                                                                       | <span data-ttu-id="efee1-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="efee1-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="efee1-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="efee1-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="efee1-134">sí</span><span class="sxs-lookup"><span data-stu-id="efee1-134">yes</span></span>       |
| [<span data-ttu-id="efee1-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="efee1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="efee1-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="efee1-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="efee1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="efee1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efee1-138">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="efee1-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

