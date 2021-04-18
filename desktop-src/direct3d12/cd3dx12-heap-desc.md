---
title: CD3DX12_HEAP_DESC estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de Desc del montón D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Estructura de CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707772"
---
# <a name="cd3dx12_heap_desc-structure"></a><span data-ttu-id="f9f45-104">CD3DX12 \_ \_ estructura DESC del montón</span><span class="sxs-lookup"><span data-stu-id="f9f45-104">CD3DX12\_HEAP\_DESC structure</span></span>

<span data-ttu-id="f9f45-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ DESC del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f9f45-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f45-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9f45-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a><span data-ttu-id="f9f45-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9f45-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9f45-108">**CD3DX12 \_ montón \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="f9f45-108">**CD3DX12\_HEAP\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-109">Crea una instancia nueva, no inicializada, de una \_ DESC del montón CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f9f45-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-110">**CD3DX12 de \_ montón de memoria de pila explícito \_ (const D3D12 \_ montón \_ DESC &o)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-110">**explicit CD3DX12\_HEAP\_DESC(const D3D12\_HEAP\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-111">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ DESC del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .</span><span class="sxs-lookup"><span data-stu-id="f9f45-111">Creates a new instance of a CD3DX12\_HEAP\_DESC, initialized with the contents of another [**D3D12\_HEAP\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-112">**CD3DX12 \_ heap \_ DESC (tamaño UINT64, propiedades del montón D3D12, \_ \_ propiedad, alineación UInt64 = 0, D3D12 indicadores de pila de \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-112">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_PROPERTIES properties, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-113">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-113">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-114">UINT64 size</span><span class="sxs-lookup"><span data-stu-id="f9f45-114">UINT64 size</span></span>

<span data-ttu-id="f9f45-115">[**D3D12 \_ Propiedades de \_ las propiedades del montón**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f9f45-115">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f9f45-116">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f9f45-116">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f9f45-117">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-117">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-118">**CD3DX12 \_ montón \_ DESC (UINT64 size, D3D12 \_ heap Type Type \_ , UINT64 Alignment = 0, D3D12 \_ heap \_ Flag Flags = D3D12 \_ heap Flag \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-118">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_HEAP\_TYPE type, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-119">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-119">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-120">UINT64 size</span><span class="sxs-lookup"><span data-stu-id="f9f45-120">UINT64 size</span></span>

<span data-ttu-id="f9f45-121">[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f9f45-121">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f9f45-122">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f9f45-122">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f9f45-123">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-123">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-124">**CD3DX12 \_ heap \_ DESC (tamaño UINT64, \_ propiedad de página D3D12 CPU \_ \_ CpuPageProperty, D3D12 \_ Memory \_ Pool MEMORYPOOLPREFERENCE, UINT64 Alignment = 0, D3D12 \_ heap Flag Flags \_ = D3D12 \_ marcador de montón \_ \_ None)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-124">**CD3DX12\_HEAP\_DESC(UINT64 size, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-125">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-125">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-126">UINT64 size</span><span class="sxs-lookup"><span data-stu-id="f9f45-126">UINT64 size</span></span>

<span data-ttu-id="f9f45-127">[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="f9f45-127">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f9f45-128">[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="f9f45-128">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f9f45-129">rechace Alineación UINT64 = 0</span><span class="sxs-lookup"><span data-stu-id="f9f45-129">(opt) UINT64 alignment = 0</span></span>

<span data-ttu-id="f9f45-130">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-130">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-131">**CD3DX12 \_ montón \_ DESC (const D3D12 \_ información de asignación de recursos \_ \_& resAllocInfo, D3D12 propiedades \_ \_ de las propiedades del montón, D3D12 indicadores del montón Flags \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-131">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_PROPERTIES properties, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-132">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-132">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-133">[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f9f45-133">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f9f45-134">[**D3D12 \_ Propiedades de \_ las propiedades del montón**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)</span><span class="sxs-lookup"><span data-stu-id="f9f45-134">[**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) properties</span></span>

<span data-ttu-id="f9f45-135">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-135">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-136">**CD3DX12 \_ montón \_ DESC (const D3D12 \_ información de asignación de recursos \_ \_& resAllocInfo, D3D12 \_ \_ tipo de tipo de montón, D3D12 marcadores de pila marcas \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-136">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_HEAP\_TYPE type, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-137">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-137">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-138">[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f9f45-138">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f9f45-139">[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="f9f45-139">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="f9f45-140">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-140">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-141">**CD3DX12 \_ montón \_ DESC (const D3D12 \_ \_ información de asignación de recursos \_& resAllocInfo, D3D12 \_ propiedad de \_ Página CPU \_ CPUPAGEPROPERTY, D3D12 \_ \_ bloque de memoria memoryPoolPreference, D3D12 \_ marcadores de pila marcas \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**</span><span class="sxs-lookup"><span data-stu-id="f9f45-141">**CD3DX12\_HEAP\_DESC(const D3D12\_RESOURCE\_ALLOCATION\_INFO& resAllocInfo, D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, D3D12\_HEAP\_FLAGS flags = D3D12\_HEAP\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-142">Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="f9f45-142">Creates a new instance of a CD3DX12\_HEAP\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="f9f45-143">[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span><span class="sxs-lookup"><span data-stu-id="f9f45-143">[**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo</span></span>

<span data-ttu-id="f9f45-144">[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="f9f45-144">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="f9f45-145">[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="f9f45-145">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="f9f45-146">rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="f9f45-146">(opt) [**D3D12\_HEAP\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) flags = D3D12\_HEAP\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="f9f45-147">**Operator const D3D12 \_ heap \_ DESC& () Const**</span><span class="sxs-lookup"><span data-stu-id="f9f45-147">**operator const D3D12\_HEAP\_DESC&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f9f45-148">Define el & operador de paso por referencia para el tipo de \_ estructura DESC del montón CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="f9f45-148">Defines the & pass-by-reference operator for the CD3DX12\_HEAP\_DESC structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9f45-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9f45-149">Requirements</span></span>



| <span data-ttu-id="f9f45-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f45-150">Requirement</span></span> | <span data-ttu-id="f9f45-151">Value</span><span class="sxs-lookup"><span data-stu-id="f9f45-151">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f45-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9f45-152">Header</span></span><br/> | <dl> <span data-ttu-id="f9f45-153"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9f45-153"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f45-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9f45-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f45-155">**D3D12 \_ montón \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="f9f45-155">**D3D12\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[<span data-ttu-id="f9f45-156">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="f9f45-156">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





