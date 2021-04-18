---
title: CD3DX12_SUBRESOURCE_FOOTPRINT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de superficie de SUBRECURSO D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Estructura de CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717596"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="b56f1-104">\_Estructura de superficie de SUBrecurso de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="b56f1-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="b56f1-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ superficie de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="b56f1-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b56f1-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="b56f1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b56f1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b56f1-108">**\_Superficie de SUBrecursos de CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="b56f1-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-109">Crea una nueva instancia no inicializada de una \_ superficie de SUBRECURSO CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b56f1-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-110">**superficie de subrecurso CD3DX12 explícita \_ \_ ( \_ espacio de Subrecurso const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="b56f1-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-111">Crea una nueva instancia de una \_ superficie de SUBrecurso de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ superficie de subrecurso de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="b56f1-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-112">**\_Superficie de SUBrecursos de CD3DX12 \_ ( \_ formato de formato de DXGI, ancho uint, alto de UINT, profundidad uint, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="b56f1-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-113">Crea una nueva instancia de una \_ superficie de subrecurso de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="b56f1-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="b56f1-114">[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="b56f1-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="b56f1-115">Ancho de UINT</span><span class="sxs-lookup"><span data-stu-id="b56f1-115">UINT width</span></span>

<span data-ttu-id="b56f1-116">Alto de UINT</span><span class="sxs-lookup"><span data-stu-id="b56f1-116">UINT height</span></span>

<span data-ttu-id="b56f1-117">Profundidad de UINT</span><span class="sxs-lookup"><span data-stu-id="b56f1-117">UINT depth</span></span>

<span data-ttu-id="b56f1-118">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="b56f1-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-119">**\_superficie de SUBrecurso de CD3DX12 explícita \_ (const D3D12 \_ \_ de DESC& resDesc, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="b56f1-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-120">Crea una nueva instancia de una \_ superficie de subrecurso de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="b56f1-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="b56f1-121">[**D3D12 \_& de \_ DESC de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) resDesc</span><span class="sxs-lookup"><span data-stu-id="b56f1-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="b56f1-122">UINT rowPitch</span><span class="sxs-lookup"><span data-stu-id="b56f1-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="b56f1-123">**operador const D3D12 \_ subresource \_ superficie& () Const**</span><span class="sxs-lookup"><span data-stu-id="b56f1-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b56f1-124">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="b56f1-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b56f1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b56f1-125">Requirements</span></span>



| <span data-ttu-id="b56f1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56f1-126">Requirement</span></span> | <span data-ttu-id="b56f1-127">Value</span><span class="sxs-lookup"><span data-stu-id="b56f1-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b56f1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b56f1-128">Header</span></span><br/> | <dl> <span data-ttu-id="b56f1-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56f1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b56f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56f1-131">**\_Superficie de SUBrecursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b56f1-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="b56f1-132">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="b56f1-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

