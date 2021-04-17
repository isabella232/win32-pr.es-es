---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un diseño de entrada como un solo objeto adecuado para una descripción de flujo.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653270"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>\_Estructura de \_ \_ diseño de entrada de flujo de estado de \_ canalización CD3DX12 \_

Una estructura de aplicación auxiliar que se usa para describir un diseño de entrada como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Diseño de \_ \_ entrada de flujo de estado de canalización CD3DX12 \_ \_**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ diseño de entrada de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Diseño de entrada de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (D3D12 de diseño de \_ entrada \_ \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de un \_ diseño de entrada de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **\_ \_ \_ \_ tipo \_ \_ de subobjeto de estado de canalización de D3D12** y datos de subobjeto copiados de *i*, una estructura de DESC de [**diseño de entrada de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> <dt>

**Operator = (D3D12 de diseño de entrada de la \_ \_ \_ descripción const const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador de \_ presentación de entrada D3D12 \_ \_ () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC de diseño de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ El diseño de entrada de flujo de estado de canalización CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

