---
title: DDX
description: Devuelve el derivado parcial del valor especificado con respecto a la coordenada x del espacio de pantalla.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- HLSL de DDX
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420906"
---
# <a name="ddx"></a><span data-ttu-id="de9fd-104">DDX</span><span class="sxs-lookup"><span data-stu-id="de9fd-104">ddx</span></span>

<span data-ttu-id="de9fd-105">Devuelve el derivado parcial del valor especificado con respecto a la coordenada x del espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="de9fd-105">Returns the partial derivative of the specified value with respect to the screen-space x-coordinate.</span></span>



| <span data-ttu-id="de9fd-106">*RET* DDX (*x*)</span><span class="sxs-lookup"><span data-stu-id="de9fd-106">*ret* ddx(*x*)</span></span> |
|----------------|



 

<span data-ttu-id="de9fd-107">Esta función calcula el derivado parcial con respecto a la coordenada x del espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="de9fd-107">This function computes the partial derivative with respect to the screen-space x-coordinate.</span></span> <span data-ttu-id="de9fd-108">Para calcular el derivado parcial con respecto a la coordenada y del espacio de pantalla, utilice la función [**DDY**](dx-graphics-hlsl-ddy.md) .</span><span class="sxs-lookup"><span data-stu-id="de9fd-108">To compute the partial derivative with respect to the screen-space y-coordinate, use the [**ddy**](dx-graphics-hlsl-ddy.md) function.</span></span>

<span data-ttu-id="de9fd-109">Esta función solo se admite en sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="de9fd-109">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="de9fd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de9fd-110">Parameters</span></span>



| <span data-ttu-id="de9fd-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="de9fd-111">Item</span></span>                                                   | <span data-ttu-id="de9fd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="de9fd-112">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="de9fd-113"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="de9fd-113"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="de9fd-114">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="de9fd-114">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="de9fd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de9fd-115">Return Value</span></span>

<span data-ttu-id="de9fd-116">Derivado parcial del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="de9fd-116">The partial derivative of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="de9fd-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="de9fd-117">Type Description</span></span>



| <span data-ttu-id="de9fd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="de9fd-118">Name</span></span>  | [<span data-ttu-id="de9fd-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="de9fd-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="de9fd-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="de9fd-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="de9fd-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="de9fd-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="de9fd-122">*x*</span><span class="sxs-lookup"><span data-stu-id="de9fd-122">*x*</span></span>   | <span data-ttu-id="de9fd-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="de9fd-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="de9fd-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="de9fd-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="de9fd-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="de9fd-125">any</span></span>                            |
| <span data-ttu-id="de9fd-126">*direcc*</span><span class="sxs-lookup"><span data-stu-id="de9fd-126">*ret*</span></span> | <span data-ttu-id="de9fd-127">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="de9fd-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="de9fd-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="de9fd-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="de9fd-129">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="de9fd-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de9fd-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="de9fd-130">Minimum Shader Model</span></span>

<span data-ttu-id="de9fd-131">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="de9fd-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="de9fd-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="de9fd-132">Shader Model</span></span>                                                                | <span data-ttu-id="de9fd-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="de9fd-133">Supported</span></span>                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="de9fd-134">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="de9fd-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="de9fd-135">sí</span><span class="sxs-lookup"><span data-stu-id="de9fd-135">yes</span></span>                                       |
| [<span data-ttu-id="de9fd-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="de9fd-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                                  | <span data-ttu-id="de9fd-137">sí</span><span class="sxs-lookup"><span data-stu-id="de9fd-137">yes</span></span>                                       |
| [<span data-ttu-id="de9fd-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de9fd-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)                   | <span data-ttu-id="de9fd-139">sí</span><span class="sxs-lookup"><span data-stu-id="de9fd-139">yes</span></span>                                       |
| [<span data-ttu-id="de9fd-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de9fd-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                   | <span data-ttu-id="de9fd-141">sí en PS \_ 2 \_ x; no compatible con PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="de9fd-141">yes in ps\_2\_x; unsupported in ps\_2\_0.</span></span> |
| [<span data-ttu-id="de9fd-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de9fd-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                   | <span data-ttu-id="de9fd-143">no</span><span class="sxs-lookup"><span data-stu-id="de9fd-143">no</span></span>                                        |



 

<span data-ttu-id="de9fd-144">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="de9fd-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="de9fd-145">Vértice</span><span class="sxs-lookup"><span data-stu-id="de9fd-145">Vertex</span></span> | <span data-ttu-id="de9fd-146">Casco</span><span class="sxs-lookup"><span data-stu-id="de9fd-146">Hull</span></span> | <span data-ttu-id="de9fd-147">Dominio</span><span class="sxs-lookup"><span data-stu-id="de9fd-147">Domain</span></span> | <span data-ttu-id="de9fd-148">Geometría</span><span class="sxs-lookup"><span data-stu-id="de9fd-148">Geometry</span></span> | <span data-ttu-id="de9fd-149">Píxel</span><span class="sxs-lookup"><span data-stu-id="de9fd-149">Pixel</span></span> | <span data-ttu-id="de9fd-150">Compute</span><span class="sxs-lookup"><span data-stu-id="de9fd-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="de9fd-151">x</span><span class="sxs-lookup"><span data-stu-id="de9fd-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="de9fd-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="de9fd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9fd-153">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="de9fd-153">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

