---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12. h)
description: Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia. | CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL estructura (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678773"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>\_Estructura de \_ \_ estarcido de profundidad de flujo de estado de \_ canalización CD3DX12 \_

Una estructura auxiliar que se usa para describir una descripción de la galería de símbolos de profundidad como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Galería de \_ \_ símbolos de profundidad de flujo de estado de \_ canalización CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ Galería de símbolos de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**Estarcido de profundidad de flujo de estado de canalización de CD3DX12 (Galería de \_ símbolos de \_ \_ \_ \_ \_ profundidad CD3DX12 \_ \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de la galería de símbolos de  **profundidad de \_ \_ \_ tipo de subobjeto \_ \_ \_ de estado de canalización de D3D12** y datos de subobjeto copiados de i, una estructura de [**\_ \_ \_ Descripción de estarcido**](cd3dx12-depth-stencil-desc.md) de

</dd> <dt>

**Operator = (CD3DX12 \_ Depth \_ estarcido \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**CD3DX12 de la \_ Galería de símbolos de profundidad del operador \_ \_ () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ \_ DESC de estarcido de profundidad de CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ La galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

