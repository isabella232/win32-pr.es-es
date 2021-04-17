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
# <a name="cd3dx12_heap_properties-structure"></a>CD3DX12 \_ estructura de propiedades del montón \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ propiedades del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**\_ \_ Propiedades del montón CD3DX12 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de \_ las propiedades del montón CD3DX12 \_ .

</dd> <dt>

**\_propiedades del montón CD3DX12 explícitas \_ ( \_ propiedades del montón const D3D12 \_ &o)**
</dt> <dd>

Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ propiedades del montón D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

</dd> <dt>

**CD3DX12 \_ \_ propiedades del montón ( \_ D3D12 \_ de la \_ propiedad de la página de CPU cpuPageProperty, D3D12 de \_ \_ bloque de memoria MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**
</dt> <dd>

Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Propiedad de página CPU**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MemoryPoolPreference del \_ bloque de memoria**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

rechace UINT creationNodeMask = 1

rechace UINT nodeMask = 1

</dd> <dt>

**propiedades del \_ montón de CD3DX12 explícitas \_ ( \_ \_ tipo de tipo de montón D3D12, uint CREATIONNODEMASK = 1, uint nodeMask = 1)**
</dt> <dd>

Crea una nueva instancia de \_ las propiedades del montón CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ Tipo \_ de montón**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

rechace UINT creationNodeMask = 1

rechace UINT nodeMask = 1

</dd> <dt>

**operador const D3D12 \_ \_ propiedades del montón& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> <dt>

**operador en línea = = (propiedades del \_ montón const D3D12 \_& l, propiedades del montón const D3D12 \_ \_& r)**
</dt> <dd>

Comprueba la igualdad entre las \_ instancias de las propiedades del montón D3D12 especificadas \_ , en función de la igualdad de todos los campos de miembro.

</dd> <dt>

**operador insertado! = (propiedades del \_ montón const D3D12 \_& l, propiedades del montón const D3D12 \_ \_& r)**
</dt> <dd>

Comprueba la desigualdad entre las instancias de propiedades del montón D3D12 especificadas \_ \_ . Se implementa tomando el inverso del valor del **operador = =** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Propiedades del montón D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





