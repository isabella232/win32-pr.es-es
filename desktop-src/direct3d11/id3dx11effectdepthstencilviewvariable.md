---
title: Interfaz ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Una interfaz Depth-estarcido-View-variable obtiene acceso a una vista de galería de símbolos de profundidad.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interfaz ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interfaz ID3DX11EffectDepthStencilViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280409"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a><span data-ttu-id="6060d-105">Interfaz ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="6060d-105">ID3DX11EffectDepthStencilViewVariable interface</span></span>

<span data-ttu-id="6060d-106">Una interfaz Depth-estarcido-View-variable obtiene acceso a una vista de galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6060d-106">A depth-stencil-view-variable interface accesses a depth-stencil view.</span></span>

## <a name="members"></a><span data-ttu-id="6060d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6060d-107">Members</span></span>

<span data-ttu-id="6060d-108">La interfaz **ID3DX11EffectDepthStencilViewVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6060d-108">The **ID3DX11EffectDepthStencilViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6060d-109">**ID3DX11EffectDepthStencilViewVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6060d-109">**ID3DX11EffectDepthStencilViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6060d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6060d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6060d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6060d-111">Methods</span></span>

<span data-ttu-id="6060d-112">La interfaz **ID3DX11EffectDepthStencilViewVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6060d-112">The **ID3DX11EffectDepthStencilViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="6060d-113">Método</span><span class="sxs-lookup"><span data-stu-id="6060d-113">Method</span></span>                                                                                     | <span data-ttu-id="6060d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6060d-114">Description</span></span>                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="6060d-115">**GetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="6060d-115">**GetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | <span data-ttu-id="6060d-116">Obtener un recurso de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6060d-116">Get a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="6060d-117">**GetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="6060d-117">**GetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | <span data-ttu-id="6060d-118">Obtiene una matriz de recursos de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6060d-118">Get an array of depth-stencil-view resources.</span></span><br/> |
| [<span data-ttu-id="6060d-119">**SetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="6060d-119">**SetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | <span data-ttu-id="6060d-120">Establezca un recurso de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6060d-120">Set a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="6060d-121">**SetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="6060d-121">**SetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | <span data-ttu-id="6060d-122">Establezca una matriz de recursos de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6060d-122">Set an array of depth-stencil-view resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6060d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6060d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6060d-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6060d-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6060d-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6060d-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6060d-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6060d-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6060d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6060d-127">Requirements</span></span>



| <span data-ttu-id="6060d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6060d-128">Requirement</span></span> | <span data-ttu-id="6060d-129">Value</span><span class="sxs-lookup"><span data-stu-id="6060d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6060d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6060d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6060d-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6060d-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6060d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6060d-132">Library</span></span><br/> | <dl> <span data-ttu-id="6060d-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6060d-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6060d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6060d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6060d-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6060d-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6060d-136">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="6060d-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6060d-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="6060d-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





