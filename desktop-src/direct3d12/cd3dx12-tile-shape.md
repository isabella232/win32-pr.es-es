---
title: CD3DX12_TILE_SHAPE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de forma de mosaico de D3D12 \_ \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Estructura de CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707764"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="9bf44-104">CD3DX12 \_ estructura de forma de mosaico \_</span><span class="sxs-lookup"><span data-stu-id="9bf44-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="9bf44-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ forma de mosaico de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="9bf44-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf44-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bf44-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="9bf44-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9bf44-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9bf44-108">**\_Forma de mosaico CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="9bf44-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="9bf44-109">Crea una nueva instancia no inicializada de una \_ forma de mosaico CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="9bf44-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="9bf44-110">**forma de mosaico de CD3DX12 explícita \_ \_ ( \_ forma de mosaico const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="9bf44-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9bf44-111">Crea una nueva instancia de una \_ forma de mosaico CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ forma de mosaico D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="9bf44-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9bf44-112">**\_Forma de mosaico CD3DX12 \_ (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**</span><span class="sxs-lookup"><span data-stu-id="9bf44-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="9bf44-113">Crea una nueva instancia de una \_ forma de mosaico CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="9bf44-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="9bf44-114">UINT widthInTexels</span><span class="sxs-lookup"><span data-stu-id="9bf44-114">UINT widthInTexels</span></span>

<span data-ttu-id="9bf44-115">UINT heightInTexels</span><span class="sxs-lookup"><span data-stu-id="9bf44-115">UINT heightInTexels</span></span>

<span data-ttu-id="9bf44-116">UINT depthInTexels</span><span class="sxs-lookup"><span data-stu-id="9bf44-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="9bf44-117">**operador const D3D12 \_ forma de mosaico \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="9bf44-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="9bf44-118">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="9bf44-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bf44-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bf44-119">Requirements</span></span>



| <span data-ttu-id="9bf44-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bf44-120">Requirement</span></span> | <span data-ttu-id="9bf44-121">Value</span><span class="sxs-lookup"><span data-stu-id="9bf44-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf44-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bf44-122">Header</span></span><br/> | <dl> <span data-ttu-id="9bf44-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bf44-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bf44-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bf44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf44-125">**\_Forma de mosaico D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9bf44-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="9bf44-126">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="9bf44-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





