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
# <a name="cd3dx12_resource_barrier-structure"></a>CD3DX12 \_ estructura de barrera de recursos \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ barrera de recursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**\_Barrera de recursos CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ barrera de recursos CD3DX12 \_ .

</dd> <dt>

**barrera de \_ recursos CD3DX12 explícita \_ (la barrera de recursos const D3D12 \_ \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ barrera de recursos CD3DX12 \_ , inicializada con el contenido de [**otra \_ \_ barrera de recursos de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).

</dd> <dt>

**Transición en línea estática (ID3D12Resource \* PreSource, \_ Estados de recursos D3D12 \_ stateBefore, D3D12 de \_ Estados de recursos \_ stateAfter, uint subresource = D3D12 \_ \_ barrera de recursos todos los Subrecursos \_ \_ , D3D12 de \_ indicadores de barrera de recursos \_ \_ Flags = D3D12 \_ marca de barrera de recursos \_ \_ \_ ninguno)**
</dt> <dd>

Transiciones entre Estados de recursos, mediante los siguientes parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* código fuente

[**D3D12 \_ \_Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ \_Estados de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

rechace UINT subresource = [ **\_ barrera de recursos D3D12 \_ \_ todos los \_** Subrecursos](constants.md)

rechace [**D3D12 \_ Marcas \_ de \_ barrera de recursos**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) marcadores = marca de barrera de recursos de D3D12 \_ \_ \_ \_ ninguno

</dd> <dt>

**Alias en línea estático (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Crea alias para el recurso antes y después de la transición de la barrera. Parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**Static inline UAV (ID3D12Resource \* PreSource)**
</dt> <dd>

Crea una vista de acceso sin ordenar (UAV) para el recurso. Parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* código fuente

</dd> <dt>

**Operator const D3D12 \_ barrera de recursos \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Barrera de recursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





