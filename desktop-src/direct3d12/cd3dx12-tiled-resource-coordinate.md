---
title: CD3DX12_TILED_RESOURCE_COORDINATE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de coordenadas de recursos en mosaico de D3D12 \_ \_ \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Estructura de CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707760"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="4d7e2-104">CD3DX12 \_ estructura de \_ coordenadas de recursos en mosaico \_</span><span class="sxs-lookup"><span data-stu-id="4d7e2-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="4d7e2-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**coordenadas de recursos en mosaico de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="4d7e2-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7e2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d7e2-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="4d7e2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d7e2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d7e2-108">**CD3DX12 \_ \_ coordenada de recursos en mosaico \_ ()**</span><span class="sxs-lookup"><span data-stu-id="4d7e2-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="4d7e2-109">Crea una nueva instancia no inicializada de una \_ coordenada de recursos en mosaico de CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4d7e2-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="4d7e2-110">**coordenada de recursos en mosaico de CD3DX12 explícita \_ \_ \_ (const D3D12 \_ \_ coordenada de recursos en mosaico \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="4d7e2-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4d7e2-111">Crea una nueva instancia de una \_ \_ coordenada de recursos \_ en mosaico CD3DX12, inicializada con el contenido de otra estructura de [**coordenadas de \_ recursos en mosaico \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="4d7e2-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d7e2-112">**CD3DX12 \_ \_ coordenada de recursos en mosaico \_ (UINT x, UINT y, UINT z, uint subresource)**</span><span class="sxs-lookup"><span data-stu-id="4d7e2-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="4d7e2-113">Crea una nueva instancia de una \_ coordenada de recursos en mosaico CD3DX12 \_ \_ , inicializando los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="4d7e2-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="4d7e2-114">UINT x</span><span class="sxs-lookup"><span data-stu-id="4d7e2-114">UINT x</span></span>

<span data-ttu-id="4d7e2-115">UINT y</span><span class="sxs-lookup"><span data-stu-id="4d7e2-115">UINT y</span></span>

<span data-ttu-id="4d7e2-116">UINT z</span><span class="sxs-lookup"><span data-stu-id="4d7e2-116">UINT z</span></span>

<span data-ttu-id="4d7e2-117">Subrecurso UINT</span><span class="sxs-lookup"><span data-stu-id="4d7e2-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="4d7e2-118">**operador const D3D12 \_ \_ coordenada de recursos en mosaico \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="4d7e2-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4d7e2-119">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="4d7e2-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d7e2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7e2-120">Requirements</span></span>



| <span data-ttu-id="4d7e2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7e2-121">Requirement</span></span> | <span data-ttu-id="4d7e2-122">Value</span><span class="sxs-lookup"><span data-stu-id="4d7e2-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7e2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d7e2-123">Header</span></span><br/> | <dl> <span data-ttu-id="4d7e2-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7e2-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7e2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d7e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7e2-126">**D3D12 \_ \_ coordenada de recursos en mosaico \_**</span><span class="sxs-lookup"><span data-stu-id="4d7e2-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="4d7e2-127">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="4d7e2-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





