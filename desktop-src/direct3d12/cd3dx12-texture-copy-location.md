---
title: CD3DX12_TEXTURE_COPY_LOCATION estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de ubicación de la copia de textura de D3D12 \_ \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Estructura de CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707767"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="c07e6-104">CD3DX12 \_ \_ estructura de ubicación de copia de textura \_</span><span class="sxs-lookup"><span data-stu-id="c07e6-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="c07e6-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de ubicación de la [**\_ copia de textura de \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="c07e6-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c07e6-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="c07e6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c07e6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c07e6-108">**CD3DX12 \_ Ubicación de copia de textura \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="c07e6-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="c07e6-109">Crea una nueva instancia no inicializada de una \_ Ubicación de copia de textura CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c07e6-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="c07e6-110">**Ubicación de copia de textura de CD3DX12 explícita \_ \_ \_ (const D3D12 \_ Ubicación de copia de textura \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="c07e6-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="c07e6-111">Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de [**Ubicación de copia de textura de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="c07e6-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c07e6-112">**CD3DX12 \_ Ubicación de copia de textura \_ \_ (ID3D12Resource \* )**</span><span class="sxs-lookup"><span data-stu-id="c07e6-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="c07e6-113">Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c07e6-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="c07e6-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="c07e6-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="c07e6-115">**\_ \_ \_ Ubicación de copia de textura de CD3DX12 (ID3D12Resource \* , D3D12 \_ colocada en la \_ superficie de Subrecursos \_ const& superficie)**</span><span class="sxs-lookup"><span data-stu-id="c07e6-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="c07e6-116">Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c07e6-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="c07e6-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="c07e6-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="c07e6-118">[**D3D12 \_ \_ \_ Superficie de Subrecursos colocada**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& superficie</span><span class="sxs-lookup"><span data-stu-id="c07e6-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="c07e6-119">**CD3DX12 \_ \_ \_ Ubicación de copia de textura (ID3D12RESOURCE \* pRes, uint sub)**</span><span class="sxs-lookup"><span data-stu-id="c07e6-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="c07e6-120">Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c07e6-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="c07e6-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="c07e6-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="c07e6-122">UINT sub</span><span class="sxs-lookup"><span data-stu-id="c07e6-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c07e6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c07e6-123">Requirements</span></span>



| <span data-ttu-id="c07e6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07e6-124">Requirement</span></span> | <span data-ttu-id="c07e6-125">Value</span><span class="sxs-lookup"><span data-stu-id="c07e6-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c07e6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c07e6-126">Header</span></span><br/> | <dl> <span data-ttu-id="c07e6-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07e6-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07e6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c07e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07e6-129">**D3D12 \_ \_ Ubicación de copia de textura \_**</span><span class="sxs-lookup"><span data-stu-id="c07e6-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="c07e6-130">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="c07e6-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





