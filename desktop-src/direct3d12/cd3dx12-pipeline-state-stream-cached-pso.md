---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir un PSO almacenado en caché como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11cb4e7a784b89a825f1e1b64083c50cc77731bbadf84d248106d69da9cf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751925"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>ESTRUCTURA DE PSO ALMACENADA EN CACHÉ DE LA SECUENCIA \_ DE ESTADO DE CANALIZACIÓN \_ \_ \_ CD3DX12 \_

Estructura auxiliar que se usa para describir un PSO almacenado en caché como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**
</dt> <dd>

Crea una nueva instancia sin inicializar de un PSO ALMACENADO EN CACHÉ DE STREAM DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM CACHED \_ \_ \_ \_ PSO(D3D12 \_ CACHED PIPELINE STATE \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de un PSO ALMACENADO EN CACHÉ CD3DX12 PIPELINE STATE STREAM, inicializado con un \_ \_ tipo de subobjeto \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE CACHED \_ \_ \_ PSO** y datos de subobjetos copiados de i , una estructura [**D3D12 CACHED PIPELINE \_ \_ \_ STATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> <dt>

**operator=(D3D12 \_ CACHED PIPELINE STATE \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ CACHED \_ PIPELINE \_ STATE() const**
</dt> <dd>

Conversión implícita a una estructura [**D3D12 \_ CACHED \_ PIPELINE \_ STATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM CACHED PSO es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

