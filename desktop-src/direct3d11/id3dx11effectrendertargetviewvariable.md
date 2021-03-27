---
title: Interfaz ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Una interfaz de presentación-destino-vista tiene acceso a un destino de representación.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986875"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="a1c8b-105">Interfaz ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="a1c8b-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="a1c8b-106">Una interfaz de presentación-destino-vista tiene acceso a un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="a1c8b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1c8b-107">Members</span></span>

<span data-ttu-id="a1c8b-108">La interfaz **ID3DX11EffectRenderTargetViewVariable** hereda de [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a1c8b-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a1c8b-109">**ID3DX11EffectRenderTargetViewVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a1c8b-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="a1c8b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1c8b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a1c8b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1c8b-111">Methods</span></span>

<span data-ttu-id="a1c8b-112">La interfaz **ID3DX11EffectRenderTargetViewVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="a1c8b-113">Método</span><span class="sxs-lookup"><span data-stu-id="a1c8b-113">Method</span></span>                                                                                     | <span data-ttu-id="a1c8b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1c8b-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="a1c8b-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="a1c8b-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="a1c8b-116">Obtiene un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="a1c8b-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="a1c8b-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="a1c8b-118">Obtiene una matriz de destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="a1c8b-119">**SetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="a1c8b-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="a1c8b-120">Establezca un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="a1c8b-121">**SetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="a1c8b-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="a1c8b-122">Establezca una matriz de destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1c8b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1c8b-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1c8b-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a1c8b-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a1c8b-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a1c8b-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a1c8b-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1c8b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1c8b-127">Requirements</span></span>



| <span data-ttu-id="a1c8b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1c8b-128">Requirement</span></span> | <span data-ttu-id="a1c8b-129">Value</span><span class="sxs-lookup"><span data-stu-id="a1c8b-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c8b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1c8b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a1c8b-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c8b-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a1c8b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1c8b-132">Library</span></span><br/> | <dl> <span data-ttu-id="a1c8b-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a1c8b-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c8b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1c8b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c8b-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="a1c8b-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="a1c8b-136">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="a1c8b-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a1c8b-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a1c8b-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





