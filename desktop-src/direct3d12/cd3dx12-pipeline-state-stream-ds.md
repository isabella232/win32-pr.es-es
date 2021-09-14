---
title: CD3DX12_PIPELINE_STATE_STREAM_DS estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DS estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbae1d75894e1fb8ffaa5bf95a45cc1eb3b2d9f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969891"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a>Estructura DS de \_ STREAM DE ESTADO DE CANALIZACIÓN \_ \_ CD3DX12 \_

Estructura auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DS**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DS DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ DS(D3D12 \_ SHADER \_ BYTECODE const &i)**
</dt> <dd>

Crea una nueva instancia de un DS DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ \_ tipo de subobjeto \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE \_ \_ DS** y datos de subobjeto copiados de i , una estructura BYTECODE del SOMBREADOR [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ BYTECODE de SOMBREADOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM DS es una especialización typedef de la plantilla \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
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

 

