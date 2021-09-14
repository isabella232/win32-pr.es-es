---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12.h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969896"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>Estructura STENCIL DE PROFUNDIDAD DE FLUJO DE \_ \_ ESTADO DE CANALIZACIÓN \_ \_ CD3DX12 \_

Estructura auxiliar que se usa para describir una descripción de galería de símbolos de profundidad como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE FLUJO DE \_ \_ ESTADO DE \_ CANALIZACIÓN \_ \_ CD3DX12**
</dt> <dd>

Crea una nueva instancia sin inicializar de una \_ STENCIL CD3DX12 PIPELINE \_ STATE \_ STREAM \_ \_ DEPTH.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de una STENCIL DE PROFUNDIDAD DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un \_ tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE DEPTH STENCIL y datos de subobjetos copiados de i , una estructura \_ \_ \_ \_ [**CD3DX12 \_ DEPTH \_ STENCIL \_ DESC.**](cd3dx12-depth-stencil-desc.md) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ DEPTH \_ STENCIL \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador CD3DX12 \_ DEPTH \_ STENCIL \_ DESC() const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC de STENCIL DEPTH de CD3DX12.**](cd3dx12-depth-stencil-desc.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

