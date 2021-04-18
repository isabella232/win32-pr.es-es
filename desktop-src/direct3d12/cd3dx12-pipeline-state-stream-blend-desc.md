---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una descripción de Blend como un solo objeto adecuado para una descripción de flujo.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698197"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>CD3DX12 de \_ canalización de estado de canalización de flujo de la \_ \_ \_ \_ estructura DESC

Una estructura de aplicación auxiliar que se usa para describir una descripción de Blend como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC**
</dt> <dd>

Crea una instancia nueva, sin inicializar, de una \_ Descripción de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**CD3DX12 de \_ canalización de estado de canalización \_ \_ \_ \_ DESC (CD3DX12 \_ Blend \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de un \_ flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC, inicializada con un tipo de subobjeto de **D3D12 de tipo de \_ \_ subobjeto de estado de canalización de \_ \_ \_ mezcla** y datos de subobjeto copiados de *i*, una estructura de [**DESC de CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 \_ Blend \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator CD3DX12 \_ Blend \_ DESC () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ DESC de CD3DX12 Blend**](cd3dx12-blend-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ La secuencia de estado de canalización CD3DX12 \_ \_ Blend \_ es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

