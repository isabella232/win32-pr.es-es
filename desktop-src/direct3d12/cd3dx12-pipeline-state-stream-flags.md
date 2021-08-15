---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir las marcas de estado de canalización como un único objeto adecuado para una descripción de secuencia.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8789fb8c393ecaf83e0295654092b22aba7f497abf909c46bac422d442c6fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530715"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>Estructura CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ FLAGS

Estructura auxiliar que se usa para describir las marcas de estado de canalización como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**MARCAS DE FLUJO DE ESTADO DE CANALIZACIÓN \_ CD3DX12 \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una canalización CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ FLAGS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ FLAGS(D3D12 \_ PIPELINE STATE \_ \_ FLAGS const &i)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 PIPELINE STATE STREAM FLAGS, inicializado con un \_ \_ tipo de subobjeto \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE FLAGS \_ \_** y datos de subobjeto copiados de *i*, una estructura [**D3D12 \_ PIPELINE STATE \_ \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> <dt>

**operator=(D3D12 \_ PIPELINE \_ STATE \_ FLAGS const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ PIPELINE \_ STATE \_ FLAGS() const**
</dt> <dd>

Conversión implícita a una [**estructura D3D12 \_ PIPELINE STATE \_ \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM FLAGS es una especialización typedef de la plantilla \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

