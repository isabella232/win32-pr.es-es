---
title: Interfaz ID3DX11EffectVariable (D3dx11effect. h)
description: La interfaz ID3DX11EffectVariable es la clase base para todas las variables de efecto. La duración de un objeto ID3DX11EffectVariable es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interfaz ID3DX11EffectVariable Direct3D 11
- Interfaz ID3DX11EffectVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821287"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="88880-105">Interfaz ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="88880-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="88880-106">La interfaz **ID3DX11EffectVariable** es la clase base para todas las variables de efecto.</span><span class="sxs-lookup"><span data-stu-id="88880-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="88880-107">La duración de un objeto **ID3DX11EffectVariable** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.</span><span class="sxs-lookup"><span data-stu-id="88880-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="88880-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="88880-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88880-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="88880-109">Methods</span></span>

<span data-ttu-id="88880-110">La interfaz **ID3DX11EffectVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="88880-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="88880-111">Método</span><span class="sxs-lookup"><span data-stu-id="88880-111">Method</span></span>                                                                           | <span data-ttu-id="88880-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="88880-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="88880-113">**Asblend**</span><span class="sxs-lookup"><span data-stu-id="88880-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="88880-114">Obtiene una variable Effect-Blend.</span><span class="sxs-lookup"><span data-stu-id="88880-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="88880-115">**AsClassInstance**</span><span class="sxs-lookup"><span data-stu-id="88880-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="88880-116">Obtiene una variable de instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="88880-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="88880-117">**AsConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="88880-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="88880-118">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="88880-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="88880-119">**AsDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="88880-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="88880-120">Obtiene una variable de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="88880-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="88880-121">**AsDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="88880-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="88880-122">Obtiene una variable de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="88880-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="88880-123">**Asinterface**</span><span class="sxs-lookup"><span data-stu-id="88880-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="88880-124">Obtiene una variable de interfaz.</span><span class="sxs-lookup"><span data-stu-id="88880-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="88880-125">**Asmatrix**</span><span class="sxs-lookup"><span data-stu-id="88880-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="88880-126">Obtiene una variable de matriz.</span><span class="sxs-lookup"><span data-stu-id="88880-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="88880-127">**Asrasterizador**</span><span class="sxs-lookup"><span data-stu-id="88880-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="88880-128">Obtiene una variable de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="88880-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="88880-129">**AsRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="88880-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="88880-130">Obtiene una variable de vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="88880-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="88880-131">**Asmuestreador**</span><span class="sxs-lookup"><span data-stu-id="88880-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="88880-132">Obtiene una variable de muestra.</span><span class="sxs-lookup"><span data-stu-id="88880-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="88880-133">**Asescalar**</span><span class="sxs-lookup"><span data-stu-id="88880-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="88880-134">Obtiene una variable escalar.</span><span class="sxs-lookup"><span data-stu-id="88880-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="88880-135">**Assombreador**</span><span class="sxs-lookup"><span data-stu-id="88880-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="88880-136">Obtiene una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="88880-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="88880-137">**AsShaderResource**</span><span class="sxs-lookup"><span data-stu-id="88880-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="88880-138">Obtiene una variable de recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="88880-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="88880-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="88880-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="88880-140">Obtiene una variable de cadena.</span><span class="sxs-lookup"><span data-stu-id="88880-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="88880-141">**AsUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="88880-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="88880-142">Obtiene una variable de vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="88880-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="88880-143">**Asvector**</span><span class="sxs-lookup"><span data-stu-id="88880-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="88880-144">Obtiene una variable de vector.</span><span class="sxs-lookup"><span data-stu-id="88880-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="88880-145">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="88880-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="88880-146">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="88880-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="88880-147">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="88880-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="88880-148">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="88880-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="88880-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="88880-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="88880-150">Obtener una descripción.</span><span class="sxs-lookup"><span data-stu-id="88880-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="88880-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="88880-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="88880-152">Obtiene un elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="88880-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="88880-153">**GetMemberByIndex**</span><span class="sxs-lookup"><span data-stu-id="88880-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="88880-154">Obtiene un miembro de estructura por índice.</span><span class="sxs-lookup"><span data-stu-id="88880-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="88880-155">**GetMemberByName**</span><span class="sxs-lookup"><span data-stu-id="88880-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="88880-156">Obtiene un miembro de estructura por nombre.</span><span class="sxs-lookup"><span data-stu-id="88880-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="88880-157">**GetMemberBySemantic**</span><span class="sxs-lookup"><span data-stu-id="88880-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="88880-158">Obtiene un miembro de estructura por semántica.</span><span class="sxs-lookup"><span data-stu-id="88880-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="88880-159">**GetParentConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="88880-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="88880-160">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="88880-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="88880-161">**GetRawValue**</span><span class="sxs-lookup"><span data-stu-id="88880-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="88880-162">Obtener datos.</span><span class="sxs-lookup"><span data-stu-id="88880-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="88880-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="88880-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="88880-164">Obtener información de tipo.</span><span class="sxs-lookup"><span data-stu-id="88880-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="88880-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="88880-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="88880-166">Comparar el tipo de datos con los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="88880-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="88880-167">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="88880-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="88880-168">Establecer datos.</span><span class="sxs-lookup"><span data-stu-id="88880-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="88880-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88880-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88880-170">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="88880-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="88880-171">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="88880-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="88880-172">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="88880-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88880-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88880-173">Requirements</span></span>



| <span data-ttu-id="88880-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="88880-174">Requirement</span></span> | <span data-ttu-id="88880-175">Value</span><span class="sxs-lookup"><span data-stu-id="88880-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88880-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88880-176">Header</span></span><br/>  | <dl> <span data-ttu-id="88880-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="88880-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="88880-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88880-178">Library</span></span><br/> | <dl> <span data-ttu-id="88880-179"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="88880-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88880-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="88880-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88880-181">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="88880-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="88880-182">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="88880-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





