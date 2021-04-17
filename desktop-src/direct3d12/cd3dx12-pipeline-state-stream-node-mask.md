---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una máscara de nodo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
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
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105653269"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>Estructura de la \_ máscara del nodo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_

Una estructura de aplicación auxiliar que se usa para describir una máscara de nodo como un solo objeto adecuado para una descripción de flujo.

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

**CD3DX12 \_ \_ máscara de \_ nodo de flujo de estado de \_ canalización \_**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ máscara de nodo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_Máscara de nodo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ (uint const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ máscara de nodo de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ máscara de nodo** y datos de subobjeto copiados de *i*, una máscara de nodo **uint** .

</dd> <dt>

**Operator = (UINT const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator UINT () Const**
</dt> <dd>

Conversión implícita a una máscara de nodo **uint** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ La máscara del nodo de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

