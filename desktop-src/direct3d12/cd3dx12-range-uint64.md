---
title: CD3DX12_RANGE_UINT64 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura UINT64 de intervalo de D3D12 \_ .
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Estructura de CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718501"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="6b093-104">CD3DX12 \_ intervalo \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="6b093-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="6b093-105">Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ UINT64 de intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="6b093-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b093-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b093-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="6b093-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b093-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b093-108">**CD3DX12 \_ intervalo \_ UINT64 ()**</span><span class="sxs-lookup"><span data-stu-id="6b093-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="6b093-109">Crea una nueva instancia no inicializada de un CD3DX12 de \_ intervalo \_ UINT64.</span><span class="sxs-lookup"><span data-stu-id="6b093-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="6b093-110">**CD3DX12 \_ intervalo \_ UInt64 explícito (const D3D12 \_ intervalo \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="6b093-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6b093-111">Crea una nueva instancia de un CD3DX12 de \_ intervalo \_ UInt64, inicializada con los valores copiados de una estructura [**\_ \_ UInt64 del intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="6b093-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b093-112">**CD3DX12 \_ intervalo \_ UINT64 (UInt64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="6b093-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="6b093-113">Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="6b093-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="6b093-114">**Operator const D3D12 \_ intervalo \_ UINT64& () Const**</span><span class="sxs-lookup"><span data-stu-id="6b093-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6b093-115">Conversión implícita a una \_ estructura UINT64 del intervalo de D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="6b093-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="6b093-116">Dado que D3D12 \_ Range \_ UInt64 es el tipo subyacente de CD3DX12 \_ Range \_ UInt64, el objeto simplemente se devuelve como una referencia UINT64 del intervalo const D3D12 \_ \_ a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="6b093-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b093-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b093-117">Requirements</span></span>



| <span data-ttu-id="6b093-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b093-118">Requirement</span></span> | <span data-ttu-id="6b093-119">Value</span><span class="sxs-lookup"><span data-stu-id="6b093-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b093-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b093-120">Header</span></span><br/> | <dl> <span data-ttu-id="6b093-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b093-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b093-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b093-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b093-123">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="6b093-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="6b093-124">**D3D12 \_ intervalo \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="6b093-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





