---
title: CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una descripción de rasterizador como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698187"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>\_Estructura del \_ \_ rasterizador de flujo de estado de CANALización de CD3DX12 \_

Una estructura de aplicación auxiliar que se usa para describir una descripción de rasterizador como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ \_ \_ Rasterizador de flujo de estado de CANALización de CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia no inicializada de un rasterizador de \_ flujo de estado de la canalización CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_Rasterizador de flujo de estado de canalización de CD3DX12 \_ \_ \_ (CD3DX12 \_ rasterizador \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de un \_ rasterizador de flujo de estado de canalización de CD3DX12 \_ \_ \_ , inicializada con un tipo de subobjeto de **D3D12 de \_ \_ \_ \_ tipo \_ de subobjeto de estado de canalización de** y datos de subobjeto copiados de *i*, una estructura de [**\_ \_ DESC del rasterizador CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 \_ rasterizador \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator CD3DX12 \_ rasterizator \_ DESC () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ DESC de rasterizador CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ \_ El rasterizador de flujo de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

