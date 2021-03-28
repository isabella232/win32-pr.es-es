---
title: Interfaz ID3DX11EffectClassInstanceVariable (D3dx11effect. h)
description: Obtiene acceso a una instancia de clase.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- Interfaz ID3DX11EffectClassInstanceVariable Direct3D 11
- Interfaz ID3DX11EffectClassInstanceVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362796"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="a81d3-105">Interfaz ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="a81d3-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="a81d3-106">Obtiene acceso a una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="a81d3-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="a81d3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a81d3-107">Members</span></span>

<span data-ttu-id="a81d3-108">La interfaz **ID3DX11EffectClassInstanceVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a81d3-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a81d3-109">**ID3DX11EffectClassInstanceVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a81d3-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="a81d3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a81d3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a81d3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a81d3-111">Methods</span></span>

<span data-ttu-id="a81d3-112">La interfaz **ID3DX11EffectClassInstanceVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a81d3-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="a81d3-113">Método</span><span class="sxs-lookup"><span data-stu-id="a81d3-113">Method</span></span>                                                                          | <span data-ttu-id="a81d3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a81d3-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="a81d3-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="a81d3-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="a81d3-116">Obtiene una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="a81d3-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a81d3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a81d3-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a81d3-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a81d3-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a81d3-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a81d3-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a81d3-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a81d3-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a81d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a81d3-121">Requirements</span></span>



| <span data-ttu-id="a81d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a81d3-122">Requirement</span></span> | <span data-ttu-id="a81d3-123">Value</span><span class="sxs-lookup"><span data-stu-id="a81d3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a81d3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a81d3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a81d3-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a81d3-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a81d3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a81d3-126">Library</span></span><br/> | <dl> <span data-ttu-id="a81d3-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a81d3-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a81d3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a81d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a81d3-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="a81d3-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="a81d3-130">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="a81d3-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a81d3-131">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="a81d3-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





