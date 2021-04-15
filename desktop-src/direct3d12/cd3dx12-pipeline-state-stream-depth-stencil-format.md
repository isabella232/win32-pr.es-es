---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir el formato de estarcido de profundidad como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649379"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>\_Estructura de flujo de estado de canalización de CD3DX12 \_ estructura de \_ \_ \_ formato de estarcido \_

Una estructura de aplicación auxiliar que se usa para describir el formato de estarcido de profundidad como un solo objeto adecuado para una descripción de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Formato de \_ \_ estarcido de profundidad de flujo de estado de \_ \_ canalización CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ formato de estarcido de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**Formato de la \_ Galería de símbolos de profundidad de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ \_ (formato de DXGI \_ const &i)**
</dt> <dd>

Crea una nueva instancia de un \_ formato de estarcido de profundidad de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ \_ , inicializado con un tipo de subobjeto de **\_ \_ tipo subobjeto de estado de canalización D3D12 \_ formato de \_ \_ \_ estarcido \_ de profundidad** y datos de subobjeto copiados de *i*, una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> <dt>

**Operator = (formato de DXGI \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator DXGI \_ Format () Const**
</dt> <dd>

Conversión implícita a una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ \_ \_ El formato de la galería de símbolos de profundidad de flujo de estado de canalización de CD3DX12 es una especialización de TYPEDEF de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define como sigue:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

