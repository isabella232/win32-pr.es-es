---
title: Interfaz ID3DX11EffectTechnique (D3dx11effect. h)
description: Una interfaz ID3DX11EffectTechnique es una colección de pasadas. La duración de un objeto ID3DX11EffectTechnique es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interfaz ID3DX11EffectTechnique Direct3D 11
- Interfaz ID3DX11EffectTechnique Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987193"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="ad4ba-105">Interfaz ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="ad4ba-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="ad4ba-106">Una interfaz **ID3DX11EffectTechnique** es una colección de pasadas.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="ad4ba-107">La duración de un objeto **ID3DX11EffectTechnique** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="ad4ba-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad4ba-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad4ba-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad4ba-109">Methods</span></span>

<span data-ttu-id="ad4ba-110">La interfaz **ID3DX11EffectTechnique** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="ad4ba-111">Método</span><span class="sxs-lookup"><span data-stu-id="ad4ba-111">Method</span></span>                                                                        | <span data-ttu-id="ad4ba-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad4ba-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ad4ba-113">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="ad4ba-114">Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="ad4ba-115">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="ad4ba-116">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="ad4ba-117">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="ad4ba-118">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="ad4ba-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="ad4ba-120">Obtener una descripción de la técnica.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="ad4ba-121">**GetPassByIndex**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="ad4ba-122">Obtiene un paso por índice.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="ad4ba-123">**GetPassByName**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="ad4ba-124">Obtiene un paso por nombre.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="ad4ba-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="ad4ba-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="ad4ba-126">Pruebe una técnica para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="ad4ba-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad4ba-127">Remarks</span></span>

<span data-ttu-id="ad4ba-128">Un efecto contiene una o más técnicas; cada técnica contiene uno o varios pasos; cada paso contiene asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="ad4ba-129">Para obtener una interfaz de la técnica de efectos, llame a un método como [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span><span class="sxs-lookup"><span data-stu-id="ad4ba-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad4ba-130">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ad4ba-131">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ad4ba-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ad4ba-132">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ad4ba-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad4ba-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad4ba-133">Requirements</span></span>



| <span data-ttu-id="ad4ba-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad4ba-134">Requirement</span></span> | <span data-ttu-id="ad4ba-135">Value</span><span class="sxs-lookup"><span data-stu-id="ad4ba-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4ba-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad4ba-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ad4ba-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ba-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ad4ba-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad4ba-138">Library</span></span><br/> | <dl> <span data-ttu-id="ad4ba-139"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ba-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4ba-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad4ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4ba-141">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="ad4ba-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ad4ba-142">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="ad4ba-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





