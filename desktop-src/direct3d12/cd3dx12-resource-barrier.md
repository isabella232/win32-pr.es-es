---
title: CD3DX12_RESOURCE_BARRIER estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de barrera de recursos de D3D12 \_ \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Estructura de CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718498"
---
# <a name="cd3dx12_resource_barrier-structure"></a><span data-ttu-id="b542e-104">CD3DX12 \_ estructura de barrera de recursos \_</span><span class="sxs-lookup"><span data-stu-id="b542e-104">CD3DX12\_RESOURCE\_BARRIER structure</span></span>

<span data-ttu-id="b542e-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ barrera de recursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .</span><span class="sxs-lookup"><span data-stu-id="b542e-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b542e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b542e-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a><span data-ttu-id="b542e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b542e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b542e-108">**\_Barrera de recursos CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="b542e-108">**CD3DX12\_RESOURCE\_BARRIER()**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-109">Crea una nueva instancia no inicializada de una \_ barrera de recursos CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b542e-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_BARRIER.</span></span>

</dd> <dt>

<span data-ttu-id="b542e-110">**barrera de \_ recursos CD3DX12 explícita \_ (la barrera de recursos const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="b542e-110">**explicit CD3DX12\_RESOURCE\_BARRIER(const D3D12\_RESOURCE\_BARRIER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-111">Crea una nueva instancia de una \_ barrera de recursos CD3DX12 \_ , inicializada con el contenido de [**otra \_ \_ barrera de recursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span><span class="sxs-lookup"><span data-stu-id="b542e-111">Creates a new instance of a CD3DX12\_RESOURCE\_BARRIER, initialized with the contents of another [**D3D12\_RESOURCE\_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).</span></span>

</dd> <dt>

<span data-ttu-id="b542e-112">**Transición en línea estática (ID3D12Resource \* PreSource, \_ Estados de recursos D3D12 \_ stateBefore, D3D12 de \_ Estados de recursos \_ stateAfter, uint subresource = D3D12 \_ \_ barrera de recursos todos los Subrecursos \_ \_ , D3D12 de \_ indicadores de barrera de recursos \_ \_ Flags = D3D12 \_ marca de barrera de recursos \_ \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="b542e-112">**static inline Transition(ID3D12Resource\* pResource, D3D12\_RESOURCE\_STATES stateBefore, D3D12\_RESOURCE\_STATES stateAfter, UINT subresource = D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES, D3D12\_RESOURCE\_BARRIER\_FLAGS flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-113">Transiciones entre Estados de recursos, mediante los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="b542e-113">Transitions between resource states, using the following parameters:</span></span>

<span data-ttu-id="b542e-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* código fuente</span><span class="sxs-lookup"><span data-stu-id="b542e-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

<span data-ttu-id="b542e-115">[**D3D12 \_ \_Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span><span class="sxs-lookup"><span data-stu-id="b542e-115">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore</span></span>

<span data-ttu-id="b542e-116">[**D3D12 \_ \_Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span><span class="sxs-lookup"><span data-stu-id="b542e-116">[**D3D12\_RESOURCE\_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter</span></span>

<span data-ttu-id="b542e-117">rechace UINT subresource = [ **\_ barrera de recursos D3D12 \_ \_ todos los \_** Subrecursos](constants.md)</span><span class="sxs-lookup"><span data-stu-id="b542e-117">(opt) UINT subresource = [**D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES**](constants.md)</span></span>

<span data-ttu-id="b542e-118">rechace [**D3D12 \_ Marcas \_ de \_ barrera de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) marcadores = marca de barrera de recursos de D3D12 \_ \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="b542e-118">(opt) [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) flags = D3D12\_RESOURCE\_BARRIER\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="b542e-119">**Alias en línea estático (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**</span><span class="sxs-lookup"><span data-stu-id="b542e-119">**static inline Aliasing(ID3D12Resource\* pResourceBefore, ID3D12Resource\* pResourceAfter)**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-120">Crea alias para el recurso antes y después de la transición de la barrera.</span><span class="sxs-lookup"><span data-stu-id="b542e-120">Creates aliases for the resource before and after the barrier transition.</span></span> <span data-ttu-id="b542e-121">Parámetros:</span><span class="sxs-lookup"><span data-stu-id="b542e-121">Parameters:</span></span>

<span data-ttu-id="b542e-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore</span><span class="sxs-lookup"><span data-stu-id="b542e-122">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceBefore</span></span>

<span data-ttu-id="b542e-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter</span><span class="sxs-lookup"><span data-stu-id="b542e-123">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResourceAfter</span></span>

</dd> <dt>

<span data-ttu-id="b542e-124">**Static inline UAV (ID3D12Resource \* PreSource)**</span><span class="sxs-lookup"><span data-stu-id="b542e-124">**static inline UAV(ID3D12Resource\* pResource)**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-125">Crea una vista de acceso sin ordenar (UAV) para el recurso.</span><span class="sxs-lookup"><span data-stu-id="b542e-125">Creates an unordered-access-view (UAV) for the resource.</span></span> <span data-ttu-id="b542e-126">Parámetros:</span><span class="sxs-lookup"><span data-stu-id="b542e-126">Parameters:</span></span>

<span data-ttu-id="b542e-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* código fuente</span><span class="sxs-lookup"><span data-stu-id="b542e-127">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pResource</span></span>

</dd> <dt>

<span data-ttu-id="b542e-128">**Operator const D3D12 \_ barrera de recursos \_& () Const**</span><span class="sxs-lookup"><span data-stu-id="b542e-128">**operator const D3D12\_RESOURCE\_BARRIER&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b542e-129">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="b542e-129">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b542e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b542e-130">Requirements</span></span>



| <span data-ttu-id="b542e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b542e-131">Requirement</span></span> | <span data-ttu-id="b542e-132">Value</span><span class="sxs-lookup"><span data-stu-id="b542e-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b542e-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b542e-133">Header</span></span><br/> | <dl> <span data-ttu-id="b542e-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b542e-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b542e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b542e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b542e-136">**\_Barrera de recursos de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b542e-136">**D3D12\_RESOURCE\_BARRIER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[<span data-ttu-id="b542e-137">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="b542e-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





