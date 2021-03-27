---
title: Interfaz ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Una interfaz de muestra tiene acceso al estado de muestra.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157256"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="3b25b-105">Interfaz ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="3b25b-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="3b25b-106">Una interfaz de muestra tiene acceso al estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="3b25b-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="3b25b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b25b-107">Members</span></span>

<span data-ttu-id="3b25b-108">La interfaz **ID3DX11EffectSamplerVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3b25b-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="3b25b-109">**ID3DX11EffectSamplerVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b25b-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="3b25b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b25b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3b25b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b25b-111">Methods</span></span>

<span data-ttu-id="3b25b-112">La interfaz **ID3DX11EffectSamplerVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3b25b-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="3b25b-113">Método</span><span class="sxs-lookup"><span data-stu-id="3b25b-113">Method</span></span>                                                                  | <span data-ttu-id="3b25b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b25b-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="3b25b-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="3b25b-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="3b25b-116">Obtiene un puntero a una variable que contiene el estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="3b25b-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="3b25b-117">**GetSampler**</span><span class="sxs-lookup"><span data-stu-id="3b25b-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="3b25b-118">Obtiene un puntero a una interfaz de muestra.</span><span class="sxs-lookup"><span data-stu-id="3b25b-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="3b25b-119">**SetSampler**</span><span class="sxs-lookup"><span data-stu-id="3b25b-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="3b25b-120">Establezca el estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="3b25b-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="3b25b-121">**UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="3b25b-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="3b25b-122">Revertir un estado de muestra establecido previamente.</span><span class="sxs-lookup"><span data-stu-id="3b25b-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="3b25b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b25b-123">Remarks</span></span>

<span data-ttu-id="3b25b-124">Una interfaz [**ID3DX11EffectVariable**](id3dx11effectvariable.md) se crea cuando se lee un efecto en la memoria.</span><span class="sxs-lookup"><span data-stu-id="3b25b-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="3b25b-125">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b25b-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="3b25b-126">Puede utilizar cualquiera de estos métodos para devolver el estado.</span><span class="sxs-lookup"><span data-stu-id="3b25b-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="3b25b-127">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="3b25b-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3b25b-128">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3b25b-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3b25b-129">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3b25b-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b25b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b25b-130">Requirements</span></span>



| <span data-ttu-id="3b25b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b25b-131">Requirement</span></span> | <span data-ttu-id="3b25b-132">Value</span><span class="sxs-lookup"><span data-stu-id="3b25b-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b25b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b25b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3b25b-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b25b-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3b25b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b25b-135">Library</span></span><br/> | <dl> <span data-ttu-id="3b25b-136"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="3b25b-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b25b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b25b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b25b-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="3b25b-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="3b25b-139">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="3b25b-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3b25b-140">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="3b25b-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





