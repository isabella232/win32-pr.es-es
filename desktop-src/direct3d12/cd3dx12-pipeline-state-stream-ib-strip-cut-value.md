---
title: CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir el valor de corte de franja del búfer de índice como un único objeto adecuado para una descripción de secuencia.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969884"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>Estructura CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE

Estructura auxiliar que se usa para describir el valor de corte de franja del búfer de índice como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**
</dt> <dd>

Crea una nueva instancia sin inicializar de un valor CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM IB STRIP CUT \_ \_ \_ \_ \_ \_ VALUE(D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de UN VALOR DE CORTE DE FRANJA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ \_ tipo de subobjeto \_ \_ \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE IB STRIP \_ \_ CUT \_ \_ \_ VALUE** y datos de subobjeto copiados de i , una estructura [**D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)

</dd> <dt>

**operator=(D3D12 \_ INDEX BUFFER STRIP CUT VALUE \_ \_ \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE() const**
</dt> <dd>

Conversión implícita en una estructura [**D3D12 \_ INDEX BUFFER STRIP CUT \_ \_ \_ \_ VALUE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM IB STRIP CUT VALUE es una especialización typedef de la plantilla \_ \_ \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

[**TIPO DE \_ SUBOBJETO DE ESTADO \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

