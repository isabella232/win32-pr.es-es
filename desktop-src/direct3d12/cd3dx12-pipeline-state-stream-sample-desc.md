---
title: CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir una descripción de ejemplo como un solo objeto adecuado para una descripción de flujo.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698407"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>\_Estructura de \_ \_ ejemplo de flujo de estado de canalización CD3DX12 \_ \_

Una estructura de aplicación auxiliar que se usa para describir una descripción de ejemplo como un solo objeto adecuado para una descripción de flujo.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una \_ secuencia de estado de canalización de CD3DX12 \_ \_ \_ ejemplo \_ desc.

</dd> <dt>

**\_Ejemplo de flujo de estado de canalización CD3DX12 \_ \_ \_ \_ DESC (ejemplo de DXGI, \_ \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de una \_ secuencia de estado de canalización de CD3DX12 \_ \_ \_ ejemplo \_ DESC, inicializada con un tipo de subobjeto de **Estado de canalización D3D12 de \_ \_ \_ \_ \_ ejemplo \_ DESC** y datos de subobjeto copiados de *i*, una estructura de [**\_ \_ DESC de ejemplo de DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> <dt>

**Operator = (ejemplo de DXGI \_ \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**Operator DXGI \_ Sample \_ DESC () Const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ DESC de ejemplo de DXGI**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

\_ \_ \_ El flujo de ejemplo de estado de canalización CD3DX12 \_ \_ DESC es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

