---
title: CD3DX12_PIPELINE_STATE_STREAM_VS estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir un sombreador de vértices como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VS estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4361cf50a97cd3d7bf2abc6995182e9ca24bad6b824505408aca98bd4b3ead42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045733"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>Estructura DE VS \_ DE LA SECUENCIA DE ESTADO DE CANALIZACIÓN \_ \_ \_ DE CD3DX12

Estructura auxiliar que se usa para describir un sombreador de vértices como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ VS**
</dt> <dd>

Crea una nueva instancia sin inicializar de un FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ VS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ VS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nueva instancia de un VS DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ \_ tipo de subobjeto \_ \_ **D3D12 \_ PIPELINE STATE SUBOBJECT TYPE \_ \_ \_ \_ VS** y datos de subobjeto copiados de i , una estructura BYTECODE de SOMBREADOR [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

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

CD3DX12 PIPELINE STATE STREAM VS es una especialización typedef de la plantilla \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

