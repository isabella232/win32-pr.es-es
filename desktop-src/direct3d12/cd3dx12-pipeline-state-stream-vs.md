---
title: CD3DX12_PIPELINE_STATE_STREAM_VS estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un sombreador de vértices como un único objeto adecuado para una descripción de flujo.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_VS
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
ms.openlocfilehash: bc7ea426c857893b98b25792ecc8e6c3d5803546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717614"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>\_Secuencia de estado de canalización de CD3DX12 frente a \_ \_ \_ estructura

Una estructura de aplicación auxiliar que se usa para describir un sombreador de vértices como un único objeto adecuado para una descripción de flujo.

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

**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ frente a**
</dt> <dd>

Crea una nueva instancia no inicializada de una secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ frente a

</dd> <dt>

**\_Secuencia de estado de canalización de CD3DX12 frente a código de \_ \_ \_ \_ bytes del sombreador de D3D12 \_ const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ secuencia de estado de canalización de CD3DX12 frente a \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 \_ \_ \_ vs** y datos de subobjeto copiados de *i*, una estructura de [**código de \_ \_ bytes del sombreador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

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

\_ \_ \_ La secuencia de estado \_ de canalización de CD3DX12 vs es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

