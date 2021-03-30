---
title: Interfaz ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Obtiene acceso a una vista de acceso desordenado.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998317"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a><span data-ttu-id="5ec74-105">Interfaz ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="5ec74-105">ID3DX11EffectUnorderedAccessViewVariable interface</span></span>

<span data-ttu-id="5ec74-106">Obtiene acceso a una vista de acceso desordenado.</span><span class="sxs-lookup"><span data-stu-id="5ec74-106">Accesses an unordered access view.</span></span>

## <a name="members"></a><span data-ttu-id="5ec74-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ec74-107">Members</span></span>

<span data-ttu-id="5ec74-108">La interfaz **ID3DX11EffectUnorderedAccessViewVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="5ec74-108">The **ID3DX11EffectUnorderedAccessViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="5ec74-109">**ID3DX11EffectUnorderedAccessViewVariable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5ec74-109">**ID3DX11EffectUnorderedAccessViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="5ec74-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ec74-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ec74-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ec74-111">Methods</span></span>

<span data-ttu-id="5ec74-112">La interfaz **ID3DX11EffectUnorderedAccessViewVariable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5ec74-112">The **ID3DX11EffectUnorderedAccessViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="5ec74-113">Método</span><span class="sxs-lookup"><span data-stu-id="5ec74-113">Method</span></span>                                                                                                      | <span data-ttu-id="5ec74-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ec74-114">Description</span></span>                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="5ec74-115">**GetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="5ec74-115">**GetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | <span data-ttu-id="5ec74-116">Obtiene una vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="5ec74-116">Get an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="5ec74-117">**GetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="5ec74-117">**GetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | <span data-ttu-id="5ec74-118">Obtiene una matriz de vistas de acceso desordenados.</span><span class="sxs-lookup"><span data-stu-id="5ec74-118">Get an array of unordered-access-views.</span></span><br/> |
| [<span data-ttu-id="5ec74-119">**SetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="5ec74-119">**SetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | <span data-ttu-id="5ec74-120">Establecer una vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="5ec74-120">Set an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="5ec74-121">**SetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="5ec74-121">**SetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | <span data-ttu-id="5ec74-122">Establezca una matriz de vistas de acceso desordenados.</span><span class="sxs-lookup"><span data-stu-id="5ec74-122">Set an array of unordered-access-views.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ec74-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ec74-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ec74-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5ec74-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5ec74-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5ec74-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5ec74-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5ec74-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ec74-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec74-127">Requirements</span></span>



| <span data-ttu-id="5ec74-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec74-128">Requirement</span></span> | <span data-ttu-id="5ec74-129">Value</span><span class="sxs-lookup"><span data-stu-id="5ec74-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec74-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ec74-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5ec74-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec74-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5ec74-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ec74-132">Library</span></span><br/> | <dl> <span data-ttu-id="5ec74-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5ec74-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec74-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec74-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec74-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="5ec74-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="5ec74-136">Effects 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="5ec74-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5ec74-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="5ec74-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





