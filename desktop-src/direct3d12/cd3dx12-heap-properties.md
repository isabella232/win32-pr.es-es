---
title: CD3DX12_HEAP_PROPERTIES estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de propiedades del montón D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Estructura de CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698198"
---
# <a name="cd3dx12_heap_properties-structure"></a><span data-ttu-id="ae5b5-104">CD3DX12 \_ estructura de propiedades del montón \_</span><span class="sxs-lookup"><span data-stu-id="ae5b5-104">CD3DX12\_HEAP\_PROPERTIES structure</span></span>

<span data-ttu-id="ae5b5-105">Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ propiedades del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-105">A helper structure to enable easy initialization of a [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5b5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae5b5-106">Syntax</span></span>


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a><span data-ttu-id="ae5b5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae5b5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae5b5-108">**\_ \_ Propiedades del montón CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-108">**CD3DX12\_HEAP\_PROPERTIES()**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-109">Crea una nueva instancia no inicializada de \_ las propiedades del montón CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-109">Creates a new, uninitialized, instance of a CD3DX12\_HEAP\_PROPERTIES.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-110">**\_propiedades del montón CD3DX12 explícitas \_ ( \_ propiedades del montón const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-110">**explicit CD3DX12\_HEAP\_PROPERTIES(const D3D12\_HEAP\_PROPERTIES &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-111">Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ propiedades del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-111">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initialized with the contents of another [**D3D12\_HEAP\_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-112">**CD3DX12 \_ \_ propiedades del montón ( \_ D3D12 \_ de la \_ propiedad de la página de CPU cpuPageProperty, D3D12 de \_ \_ bloque de memoria MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-112">**CD3DX12\_HEAP\_PROPERTIES(D3D12\_CPU\_PAGE\_PROPERTY cpuPageProperty, D3D12\_MEMORY\_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-113">Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="ae5b5-113">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="ae5b5-114">[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span><span class="sxs-lookup"><span data-stu-id="ae5b5-114">[**D3D12\_CPU\_PAGE\_PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty</span></span>

<span data-ttu-id="ae5b5-115">[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)</span><span class="sxs-lookup"><span data-stu-id="ae5b5-115">[**D3D12\_MEMORY\_POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference</span></span>

<span data-ttu-id="ae5b5-116">rechace UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="ae5b5-116">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="ae5b5-117">rechace UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="ae5b5-117">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-118">**propiedades del \_ montón de CD3DX12 explícitas \_ ( \_ \_ tipo de tipo de montón D3D12, uint CREATIONNODEMASK = 1, uint nodeMask = 1)**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-118">**explicit CD3DX12\_HEAP\_PROPERTIES(D3D12\_HEAP\_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-119">Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="ae5b5-119">Creates a new instance of a CD3DX12\_HEAP\_PROPERTIES, initializing the following parameters:</span></span>

<span data-ttu-id="ae5b5-120">[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="ae5b5-120">[**D3D12\_HEAP\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) type</span></span>

<span data-ttu-id="ae5b5-121">rechace UINT creationNodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="ae5b5-121">(opt) UINT creationNodeMask = 1</span></span>

<span data-ttu-id="ae5b5-122">rechace UINT nodeMask = 1</span><span class="sxs-lookup"><span data-stu-id="ae5b5-122">(opt) UINT nodeMask = 1</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-123">**operador const D3D12 \_ \_ propiedades del montón& () Const**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-123">**operator const D3D12\_HEAP\_PROPERTIES&() const**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-124">Define el & operador de paso por referencia para el tipo de estructura primaria.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-125">**operador en línea = = (propiedades del \_ montón const D3D12 \_& l, propiedades del montón const D3D12 \_ \_& r)**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-125">**inline operator==( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-126">Comprueba la igualdad entre las \_ instancias de las propiedades del montón D3D12 especificadas \_ , en función de la igualdad de todos los campos de miembro.</span><span class="sxs-lookup"><span data-stu-id="ae5b5-126">Tests for equality between the specified D3D12\_HEAP\_PROPERTIES instances, based on equality of all member fields.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b5-127">**operador insertado! = (propiedades del \_ montón const D3D12 \_& l, propiedades del montón const D3D12 \_ \_& r)**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-127">**inline operator!=( const D3D12\_HEAP\_PROPERTIES& l, const D3D12\_HEAP\_PROPERTIES& r )**</span></span>
</dt> <dd>

<span data-ttu-id="ae5b5-128">Comprueba la desigualdad entre las instancias de propiedades del montón D3D12 especificadas \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-128">Tests for inequality between the specified D3D12\_HEAP\_PROPERTIES instances.</span></span> <span data-ttu-id="ae5b5-129">Se implementa tomando el inverso del valor del **operador = =** .</span><span class="sxs-lookup"><span data-stu-id="ae5b5-129">Implemented by taking the inverse of the **operator==** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae5b5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae5b5-130">Requirements</span></span>



| <span data-ttu-id="ae5b5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae5b5-131">Requirement</span></span> | <span data-ttu-id="ae5b5-132">Value</span><span class="sxs-lookup"><span data-stu-id="ae5b5-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5b5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae5b5-133">Header</span></span><br/> | <dl> <span data-ttu-id="ae5b5-134"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b5-134"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae5b5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae5b5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5b5-136">**\_Propiedades del montón D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="ae5b5-136">**D3D12\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[<span data-ttu-id="ae5b5-137">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="ae5b5-137">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





