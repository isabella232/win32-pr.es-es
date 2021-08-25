---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir el formato de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9658f1df1fbe316fa9f308b9f8e0589f0f93858916c6dbde4607fd11a6f0707f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751955"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>Estructura \_ \_ \_ \_ \_ STENCIL \_ FORMAT DE PROFUNDIDAD DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12

Estructura auxiliar que se usa para describir el formato de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**FORMATO DE GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE \_ FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ \_ CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un FORMATO \_ \_ \_ \_ \_ STENCIL CD3DX12 PIPELINE STATE STREAM \_ DEPTH.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL \_ FORMAT (DXGI \_ FORMAT const &i)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL FORMAT, inicializado con un \_ \_ tipo de subobjeto \_ \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE DEPTH \_ \_ \_ STENCIL \_ FORMAT** y datos de subobjetos [**\_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) copiados de i , una enumeración DXGI FORMAT.

</dd> <dt>

**operator=(DXGI \_ FORMAT const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operator DXGI \_ FORMAT() const**
</dt> <dd>

Conversión implícita a una [**enumeración \_ DXGI FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL FORMAT es una especialización typedef de la plantilla \_ \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

