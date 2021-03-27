---
title: Interfaz ID3DX11EffectPass (D3dx11effect. h)
description: Una interfaz ID3DX11EffectPass encapsula las asignaciones de estado dentro de una técnica. La duración de un objeto ID3DX11EffectPass es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interfaz ID3DX11EffectPass Direct3D 11
- Interfaz ID3DX11EffectPass Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280454"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="fe9fe-105">Interfaz ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="fe9fe-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="fe9fe-106">Una interfaz **ID3DX11EffectPass** encapsula las asignaciones de estado dentro de una técnica.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="fe9fe-107">La duración de un objeto **ID3DX11EffectPass** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="fe9fe-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe9fe-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe9fe-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe9fe-109">Methods</span></span>

<span data-ttu-id="fe9fe-110">La interfaz **ID3DX11EffectPass** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="fe9fe-111">Método</span><span class="sxs-lookup"><span data-stu-id="fe9fe-111">Method</span></span>                                                                   | <span data-ttu-id="fe9fe-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe9fe-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="fe9fe-113">**Aplicar**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="fe9fe-114">Establezca el estado contenido en un paso en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="fe9fe-115">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="fe9fe-116">Generar una máscara para permitir o evitar cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="fe9fe-117">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="fe9fe-118">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="fe9fe-119">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="fe9fe-120">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="fe9fe-121">**GetComputeShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="fe9fe-122">Obtener una descripción del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="fe9fe-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="fe9fe-124">Obtener una descripción del paso.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="fe9fe-125">**GetDomainShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="fe9fe-126">Obtiene una descripción del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="fe9fe-127">**GetGeometryShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="fe9fe-128">Obtiene una descripción del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="fe9fe-129">**GetHullShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="fe9fe-130">Obtiene la descripción del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="fe9fe-131">**GetPixelShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="fe9fe-132">Obtiene una descripción del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="fe9fe-133">**GetVertexShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="fe9fe-134">Obtiene una descripción del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="fe9fe-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="fe9fe-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="fe9fe-136">Pruebe un paso para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="fe9fe-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe9fe-137">Remarks</span></span>

<span data-ttu-id="fe9fe-138">Un paso es un bloque de código que establece los objetos y sombreadores de estado de representación.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="fe9fe-139">Un paso se declara dentro de una técnica.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="fe9fe-140">Para obtener una interfaz de paso de efecto, llame a un método como [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span><span class="sxs-lookup"><span data-stu-id="fe9fe-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="fe9fe-141">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fe9fe-142">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="fe9fe-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fe9fe-143">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fe9fe-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe9fe-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe9fe-144">Requirements</span></span>



| <span data-ttu-id="fe9fe-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe9fe-145">Requirement</span></span> | <span data-ttu-id="fe9fe-146">Value</span><span class="sxs-lookup"><span data-stu-id="fe9fe-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9fe-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe9fe-147">Header</span></span><br/>  | <dl> <span data-ttu-id="fe9fe-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fe-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe9fe-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe9fe-149">Library</span></span><br/> | <dl> <span data-ttu-id="fe9fe-150"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="fe9fe-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9fe-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe9fe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9fe-152">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="fe9fe-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fe9fe-153">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="fe9fe-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





