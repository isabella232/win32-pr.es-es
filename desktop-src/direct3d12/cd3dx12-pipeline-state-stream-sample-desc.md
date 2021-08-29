---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una descripción de ejemplo como un único objeto adecuado para una descripción de secuencia.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44025670dc6a2f435f304494e9f31f69b12789e152f867a6efc85423c092f8e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858145"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>CD3DX12 \_ PIPELINE STATE STREAM SAMPLE \_ \_ \_ \_ DESC structure

Estructura auxiliar que se usa para describir una descripción de ejemplo como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SAMPLE \_ DESC**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ \_ \_ \_ \_ DESC DESC DE STREAM DE ESTADO DE CANALIZACIÓN CD3DX12.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM SAMPLE \_ \_ \_ \_ DESC(DXGI \_ SAMPLE \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC DE SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ \_ tipo de subobjeto \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE SAMPLE \_ \_ \_ DESC** y datos de subobjeto copiados de i , una estructura [**DXGI SAMPLE \_ \_ DESC.**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**)

</dd> <dt>

**operator=(DXGI \_ SAMPLE \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operator DXGI \_ SAMPLE \_ DESC() const**
</dt> <dd>

Conversión implícita en una [**estructura \_ \_ DESC DESC DEGI SAMPLE de DXGI.**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM SAMPLE DESC es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

