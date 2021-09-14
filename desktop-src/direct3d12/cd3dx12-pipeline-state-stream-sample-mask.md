---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una máscara de ejemplo como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969840"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a>Estructura DE MÁSCARA DE EJEMPLO DE \_ FLUJO DE ESTADO DE \_ \_ CANALIZACIÓN \_ \_ CD3DX12

Estructura auxiliar que se usa para describir una máscara de ejemplo como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**MÁSCARA DE EJEMPLO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una MÁSCARA DE EJEMPLO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM SAMPLE \_ \_ \_ \_ MASK(UINT const &i)**
</dt> <dd>

Crea una nueva instancia de UNA MÁSCARA DE EJEMPLO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un \_ \_ tipo de subobjeto \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE SAMPLE \_ \_ \_ MASK** y datos de subobjeto  copiados de i , una máscara de ejemplo UINT.

</dd> <dt>

**operator=(UINT const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador UINT() const**
</dt> <dd>

Conversión implícita a una **máscara de ejemplo UINT.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM SAMPLE MASK es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
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

 

