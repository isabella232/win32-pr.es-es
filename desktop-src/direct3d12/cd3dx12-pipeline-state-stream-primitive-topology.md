---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la topología primitiva como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698191"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>CD3DX12 \_ estructura de la topología de flujo de estado de canalización \_ \_ \_ primitiva \_

Una estructura de aplicación auxiliar que se usa para describir la topología primitiva como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ \_ \_ Topología primitiva de flujo de estado \_ de canalización de CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia no inicializada de una topología primitiva de \_ flujo de estado de la canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Topología de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (tipo de \_ topología primitiva D3D12 \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ topología primitiva de secuencia de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de la **\_ \_ \_ \_ \_ \_ topología primitiva del tipo de subobjeto de estado de canalización D3D12** y datos de subobjeto copiados de *i*, una estructura de [**\_ \_ \_ tipo de topología primitiva de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> <dt>

**operador = ( \_ tipo de topología D3D12 primitiva \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador de \_ \_ topología primitiva D3D12 \_ () Const**
</dt> <dd>

Conversión implícita a una estructura de [**\_ \_ \_ tipo de topología primitiva D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ La topología de la secuencia de estado de canalización CD3DX12 \_ \_ \_ es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

