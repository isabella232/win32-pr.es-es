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
# <a name="cd3dx12_heap_desc-structure"></a>CD3DX12 \_ \_ estructura DESC del montón

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ DESC del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ montón \_ DESC ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una \_ DESC del montón CD3DX12 \_ .

</dd> <dt>

**CD3DX12 de \_ montón de memoria de pila explícito \_ (const D3D12 \_ montón \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ DESC del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (tamaño UINT64, propiedades del montón D3D12, \_ \_ propiedad, alineación UInt64 = 0, D3D12 indicadores de pila de \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

UINT64 size

[**D3D12 \_ Propiedades de \_ las propiedades del montón**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

rechace Alineación UINT64 = 0

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ montón \_ DESC (UINT64 size, D3D12 \_ heap Type Type \_ , UINT64 Alignment = 0, D3D12 \_ heap \_ Flag Flags = D3D12 \_ heap Flag \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

UINT64 size

[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

rechace Alineación UINT64 = 0

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (tamaño UINT64, \_ propiedad de página D3D12 CPU \_ \_ CpuPageProperty, D3D12 \_ Memory \_ Pool MEMORYPOOLPREFERENCE, UINT64 Alignment = 0, D3D12 \_ heap Flag Flags \_ = D3D12 \_ marcador de montón \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

UINT64 size

[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

rechace Alineación UINT64 = 0

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ montón \_ DESC (const D3D12 \_ información de asignación de recursos \_ \_& resAllocInfo, D3D12 propiedades \_ \_ de las propiedades del montón, D3D12 indicadores del montón Flags \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Propiedades de \_ las propiedades del montón**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ montón \_ DESC (const D3D12 \_ información de asignación de recursos \_ \_& resAllocInfo, D3D12 \_ \_ tipo de tipo de montón, D3D12 marcadores de pila marcas \_ \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**CD3DX12 \_ montón \_ DESC (const D3D12 \_ \_ información de asignación de recursos \_& resAllocInfo, D3D12 \_ propiedad de \_ Página CPU \_ CPUPAGEPROPERTY, D3D12 \_ \_ bloque de memoria memoryPoolPreference, D3D12 \_ marcadores de pila marcas \_ = D3D12 \_ marcador de montón \_ \_ ninguno)**
</dt> <dd>

Crea una nueva instancia de una \_ DESC de montón CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Información de asignación de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

rechace [**D3D12 \_ Marcas \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) Flags = marcador de montón D3D12 \_ \_ \_ ninguno

</dd> <dt>

**Operator const D3D12 \_ heap \_ DESC& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de \_ estructura DESC del montón CD3DX12 \_ .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ montón \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





