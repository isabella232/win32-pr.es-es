---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un PSO almacenado en memoria caché como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698199"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ en caché del \_ PSO

Una estructura de aplicación auxiliar que se usa para describir un PSO almacenado en memoria caché como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO**
</dt> <dd>

Crea una nueva instancia no inicializada de un flujo de estado de la \_ canalización CD3DX12 \_ \_ \_ en caché \_ .

</dd> <dt>

**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO (D3D12 \_ Estado de canalización en caché \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de un flujo de estado de la \_ canalización de CD3DX12 \_ \_ \_ en caché \_ PSO, inicializado con un tipo de subobjeto de **tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ en memoria caché del \_ PSO** y los datos de subobjeto copiados de *i*, una estructura de [**\_ Estado de \_ canalización \_ de D3D12 almacenada en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> <dt>

**operador = ( \_ Estado de canalización D3D12 en caché \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador D3D12 de \_ \_ canalización en caché \_ () Const**
</dt> <dd>

Conversión implícita a una estructura de estado de la [**\_ \_ canalización \_ de D3D12 en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ El flujo de estado \_ de canalización de CD3DX12 en caché \_ PSO es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

