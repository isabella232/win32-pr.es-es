---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la firma raíz como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698408"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>\_Estructura de \_ la \_ \_ firma raíz de flujo de estado de canalización CD3DX12 \_

Una estructura de aplicación auxiliar que se usa para describir la firma raíz como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ \_ \_ \_ Firma raíz de la secuencia de estado de canalización CD3DX12 \_**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una firma raíz de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**Firma raíz de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ firma raíz de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ \_ firma raíz** y datos de subobjeto copiados de *i*, una estructura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> <dt>

**Operator = (ID3D12RootSignature \* const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador ID3D12RootSignature \* () Const**
</dt> <dd>

Conversión implícita a un puntero de estructura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ La firma raíz de la secuencia de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

