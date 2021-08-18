---
title: CD3DX12_HEAP_PROPERTIES estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura DE PROPIEDADES DE MONTÓN de D3D12. \_ \_
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- CD3DX12_HEAP_PROPERTIES estructura
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
ms.openlocfilehash: 36a4d2241568d98957ecd809f33f27c343bb0e73d0d246284e5635f22a594108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752325"
---
# <a name="cd3dx12_heap_properties-structure"></a>Estructura DE PROPIEDADES DEL \_ MONTÓN CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura DE PROPIEDADES [**\_ DE MONTÓN de \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

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

**CD3DX12 \_ HEAP \_ PROPERTIES()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una INSTANCIA DE MONTÓN DE CD3DX12 \_ \_ PROPERTIES.

</dd> <dt>

**propiedades explícitas del montón \_ CD3DX12(const \_ D3D12 \_ HEAP \_ PROPERTIES &o)**
</dt> <dd>

Crea una nueva instancia de UNA PROPIEDAD DE MONTÓN CD3DX12, inicializada con el contenido de otra estructura DE PROPIEDADES \_ DEL MONTÓN \_ de [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

</dd> <dt>

**CD3DX12 \_ HEAP \_ PROPERTIES(D3D12 \_ CPU PAGE PROPERTY \_ \_ cpuPageProperty, D3D12 \_ MEMORY POOL \_ memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Crea una nueva instancia de LAS PROPIEDADES DEL MONTÓN DE CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**D3D12 \_ CPU \_ PAGE \_ PROPERTY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) cpuPageProperty

[**D3D12 \_ MEMORY \_ POOL**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

(opt) UINT creationNodeMask = 1

(opt) NodeMask de UINT = 1

</dd> <dt>

**explicit CD3DX12 \_ HEAP \_ PROPERTIES(D3D12 \_ HEAP \_ TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1)**
</dt> <dd>

Crea una nueva instancia de LAS PROPIEDADES DEL MONTÓN DE CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**D3D12 \_ TIPO DE \_ MONTÓN**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

(opt) UINT creationNodeMask = 1

(opt) NodeMask de UINT = 1

</dd> <dt>

**operator const D3D12 \_ HEAP \_ PROPERTIES&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> <dt>

**inline operator==( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Comprueba la igualdad entre las instancias de PROPIEDADES DE MONTÓN de D3D12 especificadas, en función de la \_ igualdad de todos los campos de \_ miembro.

</dd> <dt>

**inline operator!=( const D3D12 \_ HEAP \_ PROPERTIES& l, const D3D12 \_ HEAP PROPERTIES& r \_ )**
</dt> <dd>

Comprueba la desigualdad entre las instancias de PROPIEDADES DE MONTÓN de D3D12 \_ \_ especificadas. Se implementa tomando el inverso del **valor operator==.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PROPIEDADES DEL MONTÓN D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





