---
title: Interfaz ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Una interfaz de recurso de sombreador tiene acceso a un recurso de sombreador.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998761"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="dae6a-105">Interfaz ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="dae6a-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="dae6a-106">Una interfaz de recurso de sombreador tiene acceso a un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dae6a-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="dae6a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dae6a-107">Members</span></span>

<span data-ttu-id="dae6a-108">La interfaz **ID3DX11EffectShaderResourceVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="dae6a-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="dae6a-109">**ID3DX11EffectShaderResourceVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dae6a-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="dae6a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae6a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dae6a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dae6a-111">Methods</span></span>

<span data-ttu-id="dae6a-112">La interfaz **ID3DX11EffectShaderResourceVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dae6a-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="dae6a-113">Método</span><span class="sxs-lookup"><span data-stu-id="dae6a-113">Method</span></span>                                                                           | <span data-ttu-id="dae6a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="dae6a-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="dae6a-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="dae6a-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="dae6a-116">Obtiene un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dae6a-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="dae6a-117">**GetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="dae6a-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="dae6a-118">Obtiene una matriz de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dae6a-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="dae6a-119">**SetResource**</span><span class="sxs-lookup"><span data-stu-id="dae6a-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="dae6a-120">Establezca un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dae6a-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="dae6a-121">**SetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="dae6a-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="dae6a-122">Establezca una matriz de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dae6a-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dae6a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae6a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dae6a-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="dae6a-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="dae6a-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="dae6a-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="dae6a-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="dae6a-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dae6a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae6a-127">Requirements</span></span>



| <span data-ttu-id="dae6a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae6a-128">Requirement</span></span> | <span data-ttu-id="dae6a-129">Value</span><span class="sxs-lookup"><span data-stu-id="dae6a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae6a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dae6a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dae6a-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae6a-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dae6a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dae6a-132">Library</span></span><br/> | <dl> <span data-ttu-id="dae6a-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="dae6a-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae6a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="dae6a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae6a-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="dae6a-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="dae6a-136">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="dae6a-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="dae6a-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="dae6a-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





