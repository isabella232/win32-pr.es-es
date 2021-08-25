---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una descripción de mezcla como un único objeto adecuado para una descripción de secuencia.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300506d2c41be5a5380f4f0f64c93779185fd59ced2e0dd613d926f8397ea85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752175"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>Estructura \_ \_ DESC DESC DE STREAM DE STATE \_ STREAM DE \_ CD3DX12 \_

Estructura auxiliar que se usa para describir una descripción de mezcla como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ DESC CD3DX12 PIPELINE \_ STATE \_ STREAM \_ \_ BLEND.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC(CD3DX12 \_ BLEND \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 PIPELINE STATE STREAM BLEND DESC, inicializado con un tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE BLEND y datos de subobjeto copiados de i , una estructura \_ \_ \_ \_ \_ [**CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md) **\_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ BLEND \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador CD3DX12 \_ BLEND \_ DESC() const**
</dt> <dd>

Conversión implícita a una [**estructura CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM BLEND DESC es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

[**TIPO DE \_ SUBOBJETO DE ESTADO \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

