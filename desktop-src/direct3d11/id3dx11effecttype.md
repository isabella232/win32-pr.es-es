---
title: Interfaz ID3DX11EffectType (D3dx11effect. h)
description: La interfaz ID3DX11EffectType obtiene acceso a las variables de efecto por tipo. La duración de un objeto ID3DX11EffectType es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interfaz ID3DX11EffectType Direct3D 11
- Interfaz ID3DX11EffectType Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820999"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="c90d0-105">Interfaz ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="c90d0-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="c90d0-106">La interfaz **ID3DX11EffectType** obtiene acceso a las variables de efecto por tipo.</span><span class="sxs-lookup"><span data-stu-id="c90d0-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="c90d0-107">La duración de un objeto **ID3DX11EffectType** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.</span><span class="sxs-lookup"><span data-stu-id="c90d0-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="c90d0-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c90d0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c90d0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c90d0-109">Methods</span></span>

<span data-ttu-id="c90d0-110">La interfaz **ID3DX11EffectType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c90d0-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="c90d0-111">Método</span><span class="sxs-lookup"><span data-stu-id="c90d0-111">Method</span></span>                                                                       | <span data-ttu-id="c90d0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c90d0-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="c90d0-113">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="c90d0-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="c90d0-114">Obtiene una descripción del tipo de efecto.</span><span class="sxs-lookup"><span data-stu-id="c90d0-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="c90d0-115">**GetMemberName**</span><span class="sxs-lookup"><span data-stu-id="c90d0-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="c90d0-116">Obtiene el nombre de un miembro.</span><span class="sxs-lookup"><span data-stu-id="c90d0-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="c90d0-117">**GetMemberSemantic**</span><span class="sxs-lookup"><span data-stu-id="c90d0-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="c90d0-118">Obtiene la semántica asociada a un miembro.</span><span class="sxs-lookup"><span data-stu-id="c90d0-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="c90d0-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="c90d0-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="c90d0-120">Obtiene un tipo de miembro por índice.</span><span class="sxs-lookup"><span data-stu-id="c90d0-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="c90d0-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="c90d0-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="c90d0-122">Obtiene un tipo de miembro por nombre.</span><span class="sxs-lookup"><span data-stu-id="c90d0-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="c90d0-123">**GetMemberTypeBySemantic**</span><span class="sxs-lookup"><span data-stu-id="c90d0-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="c90d0-124">Obtiene un tipo de miembro por semántica.</span><span class="sxs-lookup"><span data-stu-id="c90d0-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="c90d0-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="c90d0-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="c90d0-126">Comprueba que el tipo de efecto es válido.</span><span class="sxs-lookup"><span data-stu-id="c90d0-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="c90d0-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c90d0-127">Remarks</span></span>

<span data-ttu-id="c90d0-128">Para obtener información sobre un tipo de efecto de una variable de efecto, llame a [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="c90d0-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="c90d0-129">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="c90d0-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c90d0-130">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c90d0-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c90d0-131">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c90d0-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c90d0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c90d0-132">Requirements</span></span>



| <span data-ttu-id="c90d0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c90d0-133">Requirement</span></span> | <span data-ttu-id="c90d0-134">Value</span><span class="sxs-lookup"><span data-stu-id="c90d0-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c90d0-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c90d0-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c90d0-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c90d0-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c90d0-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c90d0-137">Library</span></span><br/> | <dl> <span data-ttu-id="c90d0-138"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="c90d0-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c90d0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c90d0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c90d0-140">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="c90d0-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c90d0-141">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="c90d0-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





