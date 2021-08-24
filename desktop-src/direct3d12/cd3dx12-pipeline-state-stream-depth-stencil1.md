---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12.h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632541"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>Estructura \_ STENCIL1 DE PROFUNDIDAD DE \_ FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ CD3DX12

Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**STENCIL1 DE PROFUNDIDAD DEL FLUJO \_ DE ESTADO DE CANALIZACIÓN \_ \_ \_ CD3DX12 \_**
</dt> <dd>

Crea una instancia de CD3DX12 \_ PIPELINE STATE \_ STREAM DEPTH \_ \_ \_ STENCIL1, sin inicializar.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const &i)**
</dt> <dd>

Crea una nueva instancia de un objeto CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1, inicializado con un \_ tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH STENCIL1 y datos de subobjeto copiados de i , una estructura \_ \_ \_ \_ [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1.**](cd3dx12-depth-stencil-desc1.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1 const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1() const**
</dt> <dd>

Conversión implícita en una [**estructura CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1.**](cd3dx12-depth-stencil-desc1.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL1 es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

