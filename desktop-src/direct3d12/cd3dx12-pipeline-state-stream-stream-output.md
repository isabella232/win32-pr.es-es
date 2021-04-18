---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la descripción de salida de flujo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717615"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>Estructura de la secuencia de salida de flujo de \_ Estado de canalización CD3DX12 \_ \_ \_ \_

Una estructura de aplicación auxiliar que se usa para describir la descripción de salida de flujo como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Salida de \_ \_ flujo de flujo de estado de canalización CD3DX12 \_ \_**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ salida de flujo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Salida de flujo de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ (DESC de salida de secuencia de D3D12 de \_ \_ salida \_ const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ salida de flujo de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ salida de flujo** y datos de subobjeto copiados de *i*, una estructura de DESC de [**salida de flujo de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> <dt>

**Operator = (D3D12 \_ Stream \_ Output \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator D3D12 \_ Stream \_ Output \_ DESC () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC de salida de secuencia D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ La salida de flujo de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

