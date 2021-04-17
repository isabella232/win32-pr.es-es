---
title: CD3DX12_SUBRESOURCE_TILING estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de mosaico de Subrecursos de D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Estructura de CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717593"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="48552-104">CD3DX12 \_ estructura de mosaico de SUBrecursos \_</span><span class="sxs-lookup"><span data-stu-id="48552-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="48552-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ mosaico de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="48552-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="48552-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48552-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="48552-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="48552-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="48552-108">**\_Mosaico de SUBrecursos de CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="48552-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="48552-109">Crea una nueva instancia no inicializada de un \_ mosaico de Subrecursos de CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="48552-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="48552-110">**mosaico de Subrecursos CD3DX12 explícito \_ \_ (const D3D12 \_ subresource \_ mosaico &o)**</span><span class="sxs-lookup"><span data-stu-id="48552-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="48552-111">Crea una nueva instancia de un \_ mosaico de SUBrecursos de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ mosaicos de Subrecursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="48552-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="48552-112">**\_Mosaico de SUBrecursos de CD3DX12 \_ (uint WIDTHINTILES, UINT16 HEIGHTINTILES, UINT16 DEPTHINTILES, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="48552-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="48552-113">Crea una nueva instancia de un \_ mosaico de Subrecursos de CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="48552-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="48552-114">UINT widthInTiles</span><span class="sxs-lookup"><span data-stu-id="48552-114">UINT widthInTiles</span></span>

<span data-ttu-id="48552-115">UINT16 heightInTiles</span><span class="sxs-lookup"><span data-stu-id="48552-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="48552-116">UINT16 depthInTiles</span><span class="sxs-lookup"><span data-stu-id="48552-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="48552-117">UINT startTileIndexInOverallResource</span><span class="sxs-lookup"><span data-stu-id="48552-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="48552-118">**operador const D3D12 \_ subresource \_ mosaico& () Const**</span><span class="sxs-lookup"><span data-stu-id="48552-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="48552-119">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="48552-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48552-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48552-120">Requirements</span></span>



| <span data-ttu-id="48552-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48552-121">Requirement</span></span> | <span data-ttu-id="48552-122">Value</span><span class="sxs-lookup"><span data-stu-id="48552-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48552-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48552-123">Header</span></span><br/> | <dl> <span data-ttu-id="48552-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="48552-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48552-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="48552-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48552-126">**\_Mosaico de SUBrecursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="48552-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="48552-127">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="48552-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





