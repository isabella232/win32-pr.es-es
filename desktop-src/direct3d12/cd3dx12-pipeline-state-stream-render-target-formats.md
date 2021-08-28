---
title: CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir los formatos de destino de representación como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS estructura
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
ms.openlocfilehash: 0580453c838f154aaed58a1df5b327fbccb0e947bd311d7353cf505d1fd46959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098890"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>Estructura CD3DX12 PIPELINE STATE STREAM RENDER TARGET FORMATS (FORMATOS DE DESTINO DE REPRESENTACIÓN DE FLUJO DE ESTADO \_ \_ DE CANALIZACIÓN \_ \_ \_ \_ CD3DX12)

Estructura auxiliar que se usa para describir los formatos de destino de representación como un único objeto adecuado para una descripción de secuencia.

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

**FORMATOS DE DESTINO DE REPRESENTACIÓN DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un CD3DX12 \_ PIPELINE STATE STREAM RENDER TARGET \_ \_ \_ \_ \_ FORMATS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM RENDER TARGET FORMATS \_ \_ \_ \_ \_ (D3D12 \_ RT FORMAT ARRAY \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 PIPELINE STATE STREAM RENDER TARGET FORMATS, inicializado con un \_ \_ tipo de subobjeto \_ \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE RENDER TARGET \_ \_ \_ \_ FORMATS** y datos de subobjetos copiados de i , una estructura [**D3D12 \_ RT FORMAT \_ \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

</dd> <dt>

**operator=(D3D12 \_ RT FORMAT ARRAY \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ RT \_ FORMAT \_ ARRAY() const**
</dt> <dd>

Conversión implícita a una estructura [**D3D12 \_ RT \_ FORMAT \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM RENDER TARGET FORMATS es una especialización typedef de la plantilla \_ \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

