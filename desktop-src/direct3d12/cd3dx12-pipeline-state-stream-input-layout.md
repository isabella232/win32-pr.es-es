---
title: CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir un diseño de entrada como un único objeto adecuado para una descripción de secuencia.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969872"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>Estructura DE DISEÑO DE ENTRADA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_

Estructura auxiliar que se usa para describir un diseño de entrada como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**DISEÑO DE ENTRADA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DISEÑO DE ENTRADA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM INPUT \_ \_ \_ \_ LAYOUT(D3D12 \_ INPUT LAYOUT \_ \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de UN DISEÑO DE ENTRADA DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE INPUT LAYOUT y datos de subobjetos copiados de i , una estructura \_ \_ \_ \_ \_ [**\_ \_ \_ DESC INPUT LAYOUT de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) **\_ \_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(D3D12 \_ INPUT \_ LAYOUT \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 \_ INPUT \_ LAYOUT \_ DESC() const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC D3D12 INPUT LAYOUT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM INPUT LAYOUT es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

