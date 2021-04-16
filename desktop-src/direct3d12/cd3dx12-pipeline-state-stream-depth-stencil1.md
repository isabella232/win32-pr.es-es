---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12. h)
description: Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 estructura (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649376"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>CD3DX12 \_ profundidad de flujo de estado de canalización \_ \_ \_ \_ STENCIL1 estructura

Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una \_ profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1.

</dd> <dt>

**\_Profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1 (CD3DX12 de \_ estarcido de profundidad \_ \_ DESC1 const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ STENCIL1, inicializada con un tipo de subobjeto de **\_ \_ tipo subobjeto de estado de canalización de D3D12 \_ \_ \_ profundidad \_ STENCIL1** y datos de subobjeto copiados de *i*, una estructura CD3DX12 de [**\_ \_ estarcido \_ de profundidad**](cd3dx12-depth-stencil-desc1.md) DESC1.

</dd> <dt>

**Operator = (CD3DX12 \_ Depth \_ stencil \_ DESC1 const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Galería de símbolos de profundidad de CD3DX12 de operador \_ \_ \_ DESC1 () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC1 de CD3DX12 Depth**](cd3dx12-depth-stencil-desc1.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ La profundidad de flujo de estado de canalización \_ de CD3DX12 STENCIL1 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

