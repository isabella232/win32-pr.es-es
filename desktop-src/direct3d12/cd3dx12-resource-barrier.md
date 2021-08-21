---
title: CD3DX12_RESOURCE_BARRIER estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura RESOURCE BARRIER de D3D12. \_ \_
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- CD3DX12_RESOURCE_BARRIER estructura
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
ms.openlocfilehash: bc3490f48e04c97c845264f514e65db390a01e115ebff7c53aca792d29f0c522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098469"
---
# <a name="cd3dx12_resource_barrier-structure"></a>Estructura DE BARRERA DE \_ RECURSOS CD3DX12 \_

Una estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ RESOURCE BARRIER \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

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

**CD3DX12 \_ RESOURCE \_ BARRIER()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una BARRERA DE RECURSOS CD3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ RESOURCE \_ BARRIER(const D3D12 \_ RESOURCE BARRIER &\_ o)**
</dt> <dd>

Crea una nueva instancia de UNA BARRERA DE RECURSOS CD3DX12, inicializada con el contenido de otra barrera de recursos \_ \_ [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)

</dd> <dt>

**static inline Transition(ID3D12Resource \* pResource, D3D12 \_ RESOURCE \_ STATES stateBefore, D3D12 \_ RESOURCE STATES \_ stateAfter, UINT subresource = D3D12 \_ RESOURCE BARRIER ALL \_ \_ \_ SUBRESOURCES, D3D12 \_ RESOURCE BARRIER \_ \_ FLAGS flags = D3D12 \_ RESOURCE BARRIER FLAG \_ \_ \_ NONE)**
</dt> <dd>

Transiciones entre estados de recursos mediante los parámetros siguientes:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

[**D3D12 \_ RESOURCE \_ STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ RESOURCE \_ STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

(opt) Subcurso UINT = [ **D3D12 \_ RESOURCE \_ BARRIER ALL \_ \_ SUBRESOURCES**](constants.md)

(opt) [**D3D12 \_ MARCAS \_ DE \_ BARRERA DE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) RECURSOS = D3D12 RESOURCE BARRIER FLAG \_ \_ \_ \_ NONE

</dd> <dt>

**static inline Aliasing(ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Crea alias para el recurso antes y después de la transición de barrera. Parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**static inline UAV(ID3D12Resource \* pResource)**
</dt> <dd>

Crea una vista de acceso no ordenado (UAV) para el recurso. Parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResource

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ BARRIER&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ RESOURCE \_ BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





