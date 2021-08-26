---
title: CD3DX12_PIPELINE_STATE_STREAM_HS estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir un sombreador de casco como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 4958161D-3E79-4227-ADD7-7F53E34B2175
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_HS estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_HS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b13c32c9da13a3cfce03605494bc8608a233f5979cb7b2757f203571c7901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028365"
---
# <a name="cd3dx12_pipeline_state_stream_hs-structure"></a>Estructura DE STREAM HS DE \_ ESTADO DE \_ CANALIZACIÓN \_ CD3DX12 \_

Estructura auxiliar que se usa para describir un sombreador de casco como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_HS {
                                   CD3DX12_PIPELINE_STATE_STREAM_HS;
                                   CD3DX12_PIPELINE_STATE_STREAM_HS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_HS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ HS**
</dt> <dd>

Crea una nueva instancia, sin inicializar, de un FLUJO DE ESTADO DE CANALIZACIÓN DE CD3DX12 \_ \_ \_ \_ HS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ HS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nueva instancia de un HS DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ \_ tipo de subobjeto \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE \_ \_ HS** y datos de subobjeto copiados de i , una estructura BYTECODE DEL SOMBREADOR [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversión implícita en una [**estructura \_ \_ BYTECODE del SOMBREADOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM HS es una especialización typedef de la plantilla \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS>
    CD3DX12_PIPELINE_STATE_STREAM_HS;
          
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

 

