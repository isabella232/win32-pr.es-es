---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir la descripción de salida del flujo como un único objeto adecuado para una descripción de secuencia.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969831"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>Estructura CD3DX12 \_ PIPELINE STATE STREAM STREAM \_ \_ \_ \_ OUTPUT

Estructura auxiliar que se usa para describir la descripción de salida del flujo como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**SALIDA DE FLUJO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una SALIDA DE FLUJO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM STREAM \_ \_ \_ \_ OUTPUT(D3D12 \_ STREAM OUTPUT \_ \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de UNA SALIDA DE STREAM STREAM DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE STREAM OUTPUT y datos de subobjetos copiados de i , una estructura \_ \_ \_ \_ \_ [**D3D12 \_ STREAM \_ OUTPUT \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(D3D12 \_ STREAM \_ OUTPUT \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ STREAM \_ OUTPUT \_ DESC() const**
</dt> <dd>

Conversión implícita a una [**estructura D3D12 \_ STREAM OUTPUT \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM STREAM OUTPUT es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

