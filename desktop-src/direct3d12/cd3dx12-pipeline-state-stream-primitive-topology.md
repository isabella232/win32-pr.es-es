---
title: CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir la topología primitiva como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969863"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>Estructura DE TOPOLOGÍA PRIMITIVA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_

Estructura auxiliar que se usa para describir la topología primitiva como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**TOPOLOGÍA PRIMITIVA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una TOPOLOGÍA PRIMITIVA CD3DX12 \_ PIPELINE \_ STATE \_ \_ \_ STREAM.

</dd> <dt>

**TOPOLOGÍA PRIMITIVA DE FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ \_ CD3DX12(TIPO DE TOPOLOGÍA PRIMITIVA \_ D3D12 \_ \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de una TOPOLOGÍA PRIMITIVA DE STREAM DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un \_ \_ tipo de subobjeto \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE PRIMITIVE \_ \_ \_ TOPOLOGY** y datos de subobjetos copiados de i , una estructura [**D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)

</dd> <dt>

**operator=(D3D12 \_ PRIMITIVE \_ TOPOLOGY TYPE \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE() const**
</dt> <dd>

Conversión implícita a una estructura DE TIPO DE TOPOLOGÍA PRIMITIVA [**\_ \_ \_ D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM PRIMITIVE TOPOLOGY es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

