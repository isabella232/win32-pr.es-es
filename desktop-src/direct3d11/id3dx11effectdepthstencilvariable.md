---
title: Interfaz ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Una interfaz de nivel de estarcido de profundidad tiene acceso a un estado de estarcido de profundidad.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003931"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="9f189-105">Interfaz ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="9f189-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="9f189-106">Una interfaz de nivel de estarcido de profundidad tiene acceso a un estado de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9f189-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="9f189-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f189-107">Members</span></span>

<span data-ttu-id="9f189-108">La interfaz **ID3DX11EffectDepthStencilVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="9f189-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="9f189-109">**ID3DX11EffectDepthStencilVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9f189-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="9f189-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f189-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9f189-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f189-111">Methods</span></span>

<span data-ttu-id="9f189-112">La interfaz **ID3DX11EffectDepthStencilVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9f189-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="9f189-113">Método</span><span class="sxs-lookup"><span data-stu-id="9f189-113">Method</span></span>                                                                                         | <span data-ttu-id="9f189-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f189-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="9f189-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="9f189-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="9f189-116">Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9f189-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="9f189-117">**GetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="9f189-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="9f189-118">Obtiene un puntero a una interfaz de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9f189-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="9f189-119">**SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="9f189-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="9f189-120">Establece el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9f189-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="9f189-121">**UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="9f189-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="9f189-122">Revierte un estado de estarcido de profundidad establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="9f189-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="9f189-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f189-123">Remarks</span></span>

<span data-ttu-id="9f189-124">Una interfaz [**ID3DX11EffectVariable**](id3dx11effectvariable.md) se crea cuando se lee un efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="9f189-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="9f189-125">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f189-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="9f189-126">Puede utilizar cualquiera de estos métodos para devolver el estado.</span><span class="sxs-lookup"><span data-stu-id="9f189-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="9f189-127">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="9f189-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9f189-128">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9f189-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9f189-129">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9f189-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f189-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f189-130">Requirements</span></span>



| <span data-ttu-id="9f189-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f189-131">Requirement</span></span> | <span data-ttu-id="9f189-132">Value</span><span class="sxs-lookup"><span data-stu-id="9f189-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f189-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f189-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9f189-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f189-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9f189-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f189-135">Library</span></span><br/> | <dl> <span data-ttu-id="9f189-136"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="9f189-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f189-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f189-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f189-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="9f189-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="9f189-139">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="9f189-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9f189-140">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="9f189-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





