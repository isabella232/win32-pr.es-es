---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una máscara de nodo como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4850ff986f2006c506d79a8ece1ced873529c2a4939869cd704a4b7c3c4b03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119685"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>Estructura DE MÁSCARA DE NODO DE FLUJO DE ESTADO DE \_ \_ CANALIZACIÓN \_ \_ CD3DX12 \_

Estructura auxiliar que se usa para describir una máscara de nodo como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**MÁSCARA DE NODO DE FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ CD3DX12 \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una MÁSCARA DE NODO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK(UINT const &i)**
</dt> <dd>

Crea una nueva instancia de UNA MÁSCARA DE NODO DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un \_ \_ tipo de subobjeto \_ \_ \_ **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE NODE \_ \_ \_ MASK**   y datos de subobjeto copiados de i , una máscara de nodo UINT.

</dd> <dt>

**operator=(UINT const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador UINT() const**
</dt> <dd>

Conversión implícita en una **máscara de nodo UINT.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

CD3DX12 PIPELINE STATE STREAM NODE MASK es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

