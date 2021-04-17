---
title: CD3DX12_TILE_REGION_SIZE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de tamaño de la región de mosaico de D3D12 \_ \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Estructura de CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707766"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="4fb65-104">CD3DX12 \_ estructura de tamaño de la región de mosaico \_ \_</span><span class="sxs-lookup"><span data-stu-id="4fb65-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="4fb65-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de tamaño de la [**\_ región de mosaico de \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="4fb65-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb65-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fb65-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="4fb65-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4fb65-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4fb65-108">**CD3DX12 \_ tamaño de la región de mosaico \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="4fb65-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="4fb65-109">Crea una nueva instancia no inicializada de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4fb65-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="4fb65-110">**tamaño de la región de mosaico de CD3DX12 explícito \_ \_ \_ (const D3D12 tamaño de la \_ región de mosaico \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="4fb65-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4fb65-111">Crea una nueva instancia de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de tamaño de la [**\_ región de mosaico \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="4fb65-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fb65-112">**CD3DX12 \_ tamaño de la región de mosaico \_ \_ (uint NumTiles, bool useBox, uint width, UINT16 height, UInt16 Depth)**</span><span class="sxs-lookup"><span data-stu-id="4fb65-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="4fb65-113">Crea una nueva instancia de un tamaño de región de mosaico de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4fb65-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="4fb65-114">UINT numTiles</span><span class="sxs-lookup"><span data-stu-id="4fb65-114">UINT numTiles</span></span>

<span data-ttu-id="4fb65-115">BOOL useBox</span><span class="sxs-lookup"><span data-stu-id="4fb65-115">BOOL useBox</span></span>

<span data-ttu-id="4fb65-116">Ancho de UINT</span><span class="sxs-lookup"><span data-stu-id="4fb65-116">UINT width</span></span>

<span data-ttu-id="4fb65-117">Alto de UINT16</span><span class="sxs-lookup"><span data-stu-id="4fb65-117">UINT16 height</span></span>

<span data-ttu-id="4fb65-118">Profundidad UINT16</span><span class="sxs-lookup"><span data-stu-id="4fb65-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="4fb65-119">**operador const D3D12 \_ tamaño de la región de mosaico \_ \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="4fb65-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4fb65-120">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="4fb65-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fb65-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fb65-121">Requirements</span></span>



| <span data-ttu-id="4fb65-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb65-122">Requirement</span></span> | <span data-ttu-id="4fb65-123">Value</span><span class="sxs-lookup"><span data-stu-id="4fb65-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb65-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fb65-124">Header</span></span><br/> | <dl> <span data-ttu-id="4fb65-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb65-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb65-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb65-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb65-127">**D3D12 \_ tamaño de la región de mosaico \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4fb65-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="4fb65-128">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4fb65-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





