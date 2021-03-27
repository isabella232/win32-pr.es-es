---
title: Interfaz ID3DX11EffectBlendVariable (D3dx11effect. h)
description: La interfaz de la variable de Blend tiene acceso al estado de Blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interfaz ID3DX11EffectBlendVariable Direct3D 11
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003975"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="068a1-105">Interfaz ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="068a1-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="068a1-106">La interfaz de la variable de Blend tiene acceso al estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="068a1-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="068a1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="068a1-107">Members</span></span>

<span data-ttu-id="068a1-108">La interfaz **ID3DX11EffectBlendVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="068a1-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="068a1-109">**ID3DX11EffectBlendVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="068a1-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="068a1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="068a1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="068a1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="068a1-111">Methods</span></span>

<span data-ttu-id="068a1-112">La interfaz **ID3DX11EffectBlendVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="068a1-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="068a1-113">Método</span><span class="sxs-lookup"><span data-stu-id="068a1-113">Method</span></span>                                                                    | <span data-ttu-id="068a1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="068a1-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="068a1-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="068a1-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="068a1-116">Obtiene un puntero a una variable de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="068a1-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="068a1-117">**GetBlendState**</span><span class="sxs-lookup"><span data-stu-id="068a1-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="068a1-118">Obtiene un puntero a una interfaz de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="068a1-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="068a1-119">**SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="068a1-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="068a1-120">Establece el estado de fusión de un efecto.</span><span class="sxs-lookup"><span data-stu-id="068a1-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="068a1-121">**UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="068a1-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="068a1-122">Revierte un estado de Blend establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="068a1-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="068a1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="068a1-123">Remarks</span></span>

<span data-ttu-id="068a1-124">Una interfaz [**ID3DX11EffectVariable**](id3dx11effectvariable.md) se crea cuando se lee un efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="068a1-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="068a1-125">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="068a1-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="068a1-126">Puede utilizar cualquiera de estos métodos para devolver el estado.</span><span class="sxs-lookup"><span data-stu-id="068a1-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="068a1-127">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="068a1-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="068a1-128">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="068a1-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="068a1-129">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="068a1-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="068a1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="068a1-130">Requirements</span></span>



| <span data-ttu-id="068a1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="068a1-131">Requirement</span></span> | <span data-ttu-id="068a1-132">Value</span><span class="sxs-lookup"><span data-stu-id="068a1-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068a1-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="068a1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="068a1-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="068a1-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="068a1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="068a1-135">Library</span></span><br/> | <dl> <span data-ttu-id="068a1-136"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="068a1-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068a1-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="068a1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068a1-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="068a1-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="068a1-139">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="068a1-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="068a1-140">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="068a1-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





