---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS estructura (D3dx12. h)
description: Estructura auxiliar que se usa para describir las marcas de estado de canalización como un solo objeto adecuado para una descripción de flujo.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649457"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>\_Estructura de \_ \_ marcas de flujo de estado de canalización CD3DX12 \_

Estructura auxiliar que se usa para describir las marcas de estado de canalización como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Marcas de \_ flujo de estado de CANALización CD3DX12 \_ \_**
</dt> <dd>

Crea una nueva instancia no inicializada de las marcas de flujo de estado de la \_ canalización CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_Marcas de flujo de estado de canalización de CD3DX12 \_ \_ \_ (marcas de estado de \_ canalización de D3D12 \_ \_ const &i)**
</dt> <dd>

Crea una nueva instancia de las \_ marcas de flujo de estado de canalización de CD3DX12 \_ \_ \_ , inicializadas con un tipo de subobjeto de **D3D12 de \_ \_ \_ \_ tipo \_ de subobjeto de estado de canalización de** y datos de subobjeto copiados de *i*, una estructura de marcas de [**\_ \_ estado \_ de canalización de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> <dt>

**operador = ( \_ marcas de estado de canalización de D3D12 \_ \_ const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador de \_ Estado de canalización D3D12 \_ \_ () Const**
</dt> <dd>

Conversión implícita a una estructura de marcas de estado de la [**\_ canalización \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ El flujo de estado de canalización CD3DX12 \_ Flags es una especialización typedef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

