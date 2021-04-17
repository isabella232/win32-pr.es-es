---
title: CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir los formatos de destino de representación como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698186"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>Estructura de los \_ formatos de destino de representación de secuencia de estado de canalización CD3DX12 \_ \_ \_ \_ \_

Una estructura de aplicación auxiliar que se usa para describir los formatos de destino de representación como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Formatos de \_ \_ destino de representación de secuencia de estado de \_ \_ canalización CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia no inicializada de los formatos de destino de representación de secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**\_Formatos de destino de representación de secuencia de estado de canalización CD3DX12 \_ \_ \_ \_ \_ (D3D12 \_ RT \_ format \_ array const &i)**
</dt> <dd>

Crea una nueva instancia de los \_ formatos de destino de representación de secuencia de estado de canalización de CD3DX12 \_ \_ \_ \_ \_ , inicializado con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 formatos de \_ \_ \_ \_ destino \_ de representación** y datos de subobjeto copiados de *i*, una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**Operator = (D3D12 \_ RT \_ format \_ array const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator D3D12 \_ RT \_ format \_ array () Const**
</dt> <dd>

Conversión implícita a una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ \_ El formato de destino de representación de flujo de estado de canalización CD3DX12 es una especialización de TYPEDEF de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 

