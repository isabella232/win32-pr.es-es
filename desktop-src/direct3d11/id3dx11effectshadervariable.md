---
title: Interfaz ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Una interfaz de variable de sombreador tiene acceso a una variable de sombreador.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interfaz ID3DX11EffectShaderVariable Direct3D 11
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998437"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="bff75-105">Interfaz ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="bff75-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="bff75-106">Una interfaz de variable de sombreador tiene acceso a una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bff75-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="bff75-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bff75-107">Members</span></span>

<span data-ttu-id="bff75-108">La interfaz **ID3DX11EffectShaderVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="bff75-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="bff75-109">**ID3DX11EffectShaderVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bff75-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="bff75-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bff75-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bff75-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bff75-111">Methods</span></span>

<span data-ttu-id="bff75-112">La interfaz **ID3DX11EffectShaderVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bff75-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="bff75-113">Método</span><span class="sxs-lookup"><span data-stu-id="bff75-113">Method</span></span>                                                                                                           | <span data-ttu-id="bff75-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="bff75-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="bff75-115">**GetComputeShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="bff75-116">Obtener un sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="bff75-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="bff75-117">**GetDomainShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="bff75-118">Obtiene un sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="bff75-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="bff75-119">**GetGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="bff75-120">Obtiene un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="bff75-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="bff75-121">**GetHullShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="bff75-122">Obtener un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="bff75-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="bff75-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="bff75-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="bff75-124">Obtiene una descripción de la firma de entrada.</span><span class="sxs-lookup"><span data-stu-id="bff75-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="bff75-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="bff75-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="bff75-126">Obtiene una descripción de la firma de salida.</span><span class="sxs-lookup"><span data-stu-id="bff75-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="bff75-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="bff75-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="bff75-128">Obtiene una descripción de la firma de la constante patch.</span><span class="sxs-lookup"><span data-stu-id="bff75-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="bff75-129">**GetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="bff75-130">Obtiene un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="bff75-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="bff75-131">**GetShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="bff75-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="bff75-132">Obtener una descripción del sombreador.</span><span class="sxs-lookup"><span data-stu-id="bff75-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="bff75-133">**GetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="bff75-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="bff75-134">Obtiene un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="bff75-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="bff75-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bff75-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bff75-136">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="bff75-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bff75-137">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bff75-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bff75-138">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bff75-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bff75-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bff75-139">Requirements</span></span>



| <span data-ttu-id="bff75-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff75-140">Requirement</span></span> | <span data-ttu-id="bff75-141">Value</span><span class="sxs-lookup"><span data-stu-id="bff75-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff75-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bff75-142">Header</span></span><br/>  | <dl> <span data-ttu-id="bff75-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff75-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bff75-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bff75-144">Library</span></span><br/> | <dl> <span data-ttu-id="bff75-145"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="bff75-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff75-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="bff75-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff75-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="bff75-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="bff75-148">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="bff75-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bff75-149">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="bff75-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





