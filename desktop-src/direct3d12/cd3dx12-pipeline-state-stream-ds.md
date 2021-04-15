---
title: CD3DX12_PIPELINE_STATE_STREAM_DS estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de flujo.
ms.assetid: 42F8B7C1-B754-4B07-BF04-DBF450A942E6
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DS
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649375"
---
# <a name="cd3dx12_pipeline_state_stream_ds-structure"></a>Estructura de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_

Una estructura de aplicación auxiliar que se usa para describir un sombreador de dominio como un único objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DS {
                                   CD3DX12_PIPELINE_STATE_STREAM_DS;
                                   CD3DX12_PIPELINE_STATE_STREAM_DS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ DS**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ flujo de estado de canalización de CD3DX12 \_ \_ \_ .

</dd> <dt>

**Secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ DS ( \_ código de bytes del sombreador de D3D12 \_ const &i)**
</dt> <dd>

Crea una nueva instancia de un \_ flujo de estado de canalización CD3DX12 \_ \_ \_ DS, inicializado con un tipo de subobjeto de **D3D12 de \_ \_ \_ \_ tipo \_ de subobjeto de estado de canalización de** y datos de subobjeto copiados de *i*, una estructura de [**código de \_ \_ bytes del sombreador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**Operator = (D3D12 de \_ código de bytes de sombreador \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 de \_ \_ código de bytes del sombreador () Const**
</dt> <dd>

Conversión implícita a una estructura de [**\_ código de \_ bytes del sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ La secuencia de estado \_ de la canalización CD3DX12 DS es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS>
    CD3DX12_PIPELINE_STATE_STREAM_DS;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

