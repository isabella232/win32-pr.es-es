---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura UINT64 del intervalo de SUBRECURSO D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Estructura de CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717594"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="23c1c-104">\_ \_ Estructura UINT64 del intervalo de Subrecursos de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="23c1c-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="23c1c-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ UINT64 del \_ intervalo \_ de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="23c1c-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c1c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23c1c-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="23c1c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23c1c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="23c1c-108">**\_Intervalo de SUBRECURSO CD3DX12 \_ \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="23c1c-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="23c1c-109">Crea una nueva instancia no inicializada de un \_ intervalo de subrecurso de \_ CD3DX12 \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="23c1c-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="23c1c-110">**intervalo de \_ SUBRECURSO CD3DX12 explícito \_ \_ UINT64 (const D3D12 \_ subresource \_ intervalo \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="23c1c-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="23c1c-111">Crea una nueva instancia de un \_ intervalo de SUBRECURSO CD3DX12 \_ \_ UInt64, inicializado con los valores copiados de una estructura UInt64 del [**\_ \_ intervalo \_ de Subrecursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="23c1c-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="23c1c-112">**\_ \_ Intervalo de subrecurso \_ de CD3DX12 UInt64 (subrecurso uint, const D3D12 \_ intervalo \_ UInt64& intervalo)**</span><span class="sxs-lookup"><span data-stu-id="23c1c-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="23c1c-113">Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="23c1c-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="23c1c-114">**\_Intervalo de SUBRECURSO CD3DX12 \_ \_ UInt64 (subrecurso uint, UINT64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="23c1c-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="23c1c-115">Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="23c1c-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="23c1c-116">**operador const D3D12 \_ subresource \_ intervalo \_ UINT64& () Const**</span><span class="sxs-lookup"><span data-stu-id="23c1c-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="23c1c-117">Conversión implícita a una \_ estructura UINT64 del intervalo de SUBRECURSO D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="23c1c-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="23c1c-118">Dado que \_ \_ el intervalo de Subrecursos \_ de D3D12 UInt64 es el tipo subyacente del \_ intervalo de subrecurso de CD3DX12 \_ \_ UInt64, el objeto simplemente se devuelve como una \_ referencia de galería de símbolos de profundidad const D3D12 \_ \_ DESC1 a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="23c1c-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23c1c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23c1c-119">Requirements</span></span>



| <span data-ttu-id="23c1c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c1c-120">Requirement</span></span> | <span data-ttu-id="23c1c-121">Value</span><span class="sxs-lookup"><span data-stu-id="23c1c-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="23c1c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23c1c-122">Header</span></span><br/> | <dl> <span data-ttu-id="23c1c-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c1c-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c1c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="23c1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c1c-125">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="23c1c-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="23c1c-126">**\_Intervalo de SUBrecurso de D3D12 \_ \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="23c1c-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





