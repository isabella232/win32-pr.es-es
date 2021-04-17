---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir el valor de corte de la franja del búfer de índice como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c14924828c924b3bbbca3bb1a5f822437ec4c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653271"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>Secuencia de estado de canalización de CD3DX12 de la \_ estructura de valor de \_ \_ \_ \_ corte de franja \_ \_

Una estructura de aplicación auxiliar que se usa para describir el valor de corte de la franja del búfer de índice como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**Flujo de estado de canalización de CD3DX12 de \_ Estado de canalización \_ \_ \_ IB \_ \_ \_**
</dt> <dd>

Crea una instancia nueva, no inicializada, de un valor de corte de la franja de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ \_ \_ .

</dd> <dt>

**\_Valor de canalización CD3DX12 flujo de estado de canalización \_ \_ \_ IB \_ \_ \_ (D3D12 \_ valor de corte de franja de búfer de índice \_ \_ \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de un valor de corte de la \_ franja de estado de la canalización de CD3DX12 \_ \_ \_ \_ \_ \_ , inicializada con un tipo de subobjeto del **\_ \_ \_ tipo de subobjeto \_ \_ \_ \_ \_ de estado de canalización** IB y datos de subobjeto copiados de *i*, una estructura de [**valor de corte de \_ franja de búfer de índice \_ \_ \_ \_ de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> <dt>

**Operator = (D3D12 \_ Índice de la franja de búfer de índice \_ \_ \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ index de búfer de índice \_ \_ \_ \_ () Const**
</dt> <dd>

Conversión implícita a una estructura de [**valor de corte de franja del búfer de índice de D3D12 \_ \_ \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_La secuencia de estado de la canalización de CD3DX12 \_ \_ \_ \_ \_ \_ valor de corte de franjas de división es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

