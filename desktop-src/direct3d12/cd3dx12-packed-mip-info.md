---
title: CD3DX12_PACKED_MIP_INFO estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de información de MIP empaquetada D3D12 \_ \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Estructura de CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707771"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="7b9e4-104">CD3DX12 \_ \_ estructura de información de MIP empaquetada \_</span><span class="sxs-lookup"><span data-stu-id="7b9e4-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="7b9e4-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ información de MIP empaquetada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="7b9e4-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9e4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b9e4-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="7b9e4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b9e4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b9e4-108">**CD3DX12 \_ información de MIP empaquetada \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="7b9e4-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e4-109">Crea una nueva instancia no inicializada de una \_ información de MIP empaquetada de CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b9e4-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="7b9e4-110">**información de \_ MIP empaquetada CD3DX12 explícita \_ \_ (const D3D12 \_ empaquetada de \_ información de MIP \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="7b9e4-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e4-111">Crea una nueva instancia de una \_ información de MIP empaquetada CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de [**\_ \_ \_ información de MIP empaquetada de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="7b9e4-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b9e4-112">**CD3DX12 \_ \_ información de MIP empaquetada \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="7b9e4-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e4-113">Crea una nueva instancia de una \_ información de MIP empaquetada CD3DX12 \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="7b9e4-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="7b9e4-114">UINT8 numStandardMips</span><span class="sxs-lookup"><span data-stu-id="7b9e4-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="7b9e4-115">UINT8 numPackedMips</span><span class="sxs-lookup"><span data-stu-id="7b9e4-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="7b9e4-116">UINT numTilesForPackedMips</span><span class="sxs-lookup"><span data-stu-id="7b9e4-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="7b9e4-117">UINT startTileIndexInOverallResource</span><span class="sxs-lookup"><span data-stu-id="7b9e4-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="7b9e4-118">**operador const D3D12 \_ empaquetado de la \_ información de MIP \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="7b9e4-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="7b9e4-119">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="7b9e4-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b9e4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b9e4-120">Requirements</span></span>



| <span data-ttu-id="7b9e4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9e4-121">Requirement</span></span> | <span data-ttu-id="7b9e4-122">Value</span><span class="sxs-lookup"><span data-stu-id="7b9e4-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b9e4-123">Header</span></span><br/> | <dl> <span data-ttu-id="7b9e4-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b9e4-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9e4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b9e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9e4-126">**D3D12 \_ \_ información de MIP empaquetada \_**</span><span class="sxs-lookup"><span data-stu-id="7b9e4-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="7b9e4-127">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="7b9e4-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





