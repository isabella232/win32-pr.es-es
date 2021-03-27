---
title: Interfaz ID3DX11EffectGroup (D3dx11effect. h)
description: La interfaz ID3DX11EffectGroup obtiene acceso a un grupo de efectos. La duración de un objeto ID3DX11EffectGroup es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaz ID3DX11EffectGroup Direct3D 11
- Interfaz ID3DX11EffectGroup Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986953"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="611ad-105">Interfaz ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="611ad-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="611ad-106">La interfaz **ID3DX11EffectGroup** obtiene acceso a un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="611ad-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="611ad-107">La duración de un objeto **ID3DX11EffectGroup** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.</span><span class="sxs-lookup"><span data-stu-id="611ad-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="611ad-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="611ad-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="611ad-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="611ad-109">Methods</span></span>

<span data-ttu-id="611ad-110">La interfaz **ID3DX11EffectGroup** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="611ad-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="611ad-111">Método</span><span class="sxs-lookup"><span data-stu-id="611ad-111">Method</span></span>                                                                  | <span data-ttu-id="611ad-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="611ad-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="611ad-113">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="611ad-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="611ad-114">Obtiene una anotación por índice.</span><span class="sxs-lookup"><span data-stu-id="611ad-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="611ad-115">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="611ad-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="611ad-116">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="611ad-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="611ad-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="611ad-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="611ad-118">Obtiene una descripción del grupo.</span><span class="sxs-lookup"><span data-stu-id="611ad-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="611ad-119">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="611ad-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="611ad-120">Obtiene una técnica por índice.</span><span class="sxs-lookup"><span data-stu-id="611ad-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="611ad-121">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="611ad-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="611ad-122">Obtener una técnica por nombre.</span><span class="sxs-lookup"><span data-stu-id="611ad-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="611ad-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="611ad-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="611ad-124">Pruebe un efecto para ver si contiene una sintaxis válida.</span><span class="sxs-lookup"><span data-stu-id="611ad-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="611ad-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="611ad-125">Remarks</span></span>

<span data-ttu-id="611ad-126">Para obtener una interfaz **ID3DX11EffectGroup** , llame a un método como [**ID3DX11Effect:: GetGroupByName**](id3dx11effect-getgroupbyname.md).</span><span class="sxs-lookup"><span data-stu-id="611ad-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="611ad-127">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="611ad-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="611ad-128">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="611ad-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="611ad-129">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="611ad-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="611ad-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="611ad-130">Requirements</span></span>



| <span data-ttu-id="611ad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="611ad-131">Requirement</span></span> | <span data-ttu-id="611ad-132">Value</span><span class="sxs-lookup"><span data-stu-id="611ad-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611ad-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="611ad-133">Header</span></span><br/>  | <dl> <span data-ttu-id="611ad-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="611ad-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="611ad-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="611ad-135">Library</span></span><br/> | <dl> <span data-ttu-id="611ad-136"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="611ad-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611ad-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="611ad-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611ad-138">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="611ad-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="611ad-139">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="611ad-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





