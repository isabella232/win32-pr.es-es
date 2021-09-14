---
title: CD3DX12_HEAP_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ DESC de MONTÓN de D3D12. \_
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- CD3DX12_HEAP_DESC estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360857"
---
# <a name="cd3dx12_heap_desc-structure"></a>Cd3DX12 \_ HEAP \_ DESC (estructura)

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ DESC de MONTÓN de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ HEAP \_ DESC()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ DESC de MONTÓN DE CD3DX12. \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ HEAP \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC de HEAP CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ DESC de MONTÓN de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(UINT64 size, D3D12 \_ HEAP \_ PROPERTIES properties, UINT64 alignment = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

Tamaño de UINT64

[**D3D12 \_ Propiedades de \_ HEAP PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) Alineación de UINT64 = 0

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP DESC(tamaño UINT64, tipo de TIPO DE MONTÓN \_ D3D12, alineación \_ de \_ UINT64 = 0, D3D12 MARCAS DE MONTÓN DE MONTÓN \_ = \_ D3D12 \_ HEAP FLAG \_ \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

Tamaño de UINT64

[**D3D12 \_ Tipo de \_ TIPO DE MONTÓN**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) Alineación de UINT64 = 0

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(tamaño UINT64, D3D12 \_ CPU PAGE PROPERTY \_ \_ cpuPageProperty, D3D12 \_ MEMORY POOL \_ memoryPoolPreference, alineación de UINT64 = 0, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP FLAG \_ \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

Tamaño de UINT64

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) Alineación de UINT64 = 0

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ PROPERTIES properties, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO&**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) resAllocInfo

[**D3D12 \_ Propiedades de \_ HEAP PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ HEAP \_ TYPE type, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO&**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) resAllocInfo

[**D3D12 \_ Tipo de \_ TIPO DE MONTÓN**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**CD3DX12 \_ HEAP \_ DESC(const D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO& resAllocInfo, D3D12 \_ CPU \_ PAGE \_ PROPERTY cpuPageProperty, D3D12 \_ MEMORY \_ POOL memoryPoolPreference, D3D12 \_ HEAP \_ FLAGS flags = D3D12 \_ HEAP \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un \_ DESC HEAP DESC de CD3DX12, \_ inicializando los parámetros siguientes:

[**D3D12 \_ RESOURCE \_ ALLOCATION \_ INFO&**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) resAllocInfo

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) [**D3D12 \_ Marcas de \_ HEAP FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ HEAP \_ FLAG \_ NONE

</dd> <dt>

**operator const D3D12 \_ HEAP \_ DESC&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura \_ DESC HEAP \_ CD3DX12.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ HEAP \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





