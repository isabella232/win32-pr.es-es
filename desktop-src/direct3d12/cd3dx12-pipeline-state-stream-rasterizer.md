---
title: CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir una descripción de rasterizador como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969852"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>Estructura RASTERIZER de FLUJO DE ESTADO DE \_ \_ CANALIZACIÓN \_ CD3DX12 \_

Estructura auxiliar que se usa para describir una descripción de rasterizador como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**RASTERIZADOR DE FLUJO DE ESTADO DE \_ \_ CANALIZACIÓN \_ CD3DX12 \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un RASTERIZER DE FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ CD3DX12. \_

</dd> <dt>

**RASTERIZER DE FLUJO DE ESTADO DE CANALIZACIÓN \_ \_ \_ \_ CD3DX12(CD3DX12 \_ RASTERIZER \_ DESC const &i)**
</dt> <dd>

Crea una nueva instancia de UN RASTERIZER DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializado con un \_ tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE RASTERIZER y datos de subobjeto copiados de i , una estructura \_ \_ \_ [**CD3DX12 \_ RASTERIZER \_ DESC.**](cd3dx12-rasterizer-desc.md) **\_ \_ \_ \_ \_** 

</dd> <dt>

**operator=(CD3DX12 \_ RASTERIZER \_ DESC const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operador CD3DX12 \_ RASTERIZER \_ DESC() const**
</dt> <dd>

Conversión implícita a una [**estructura \_ \_ DESC de RASTERIZER CD3DX12.**](cd3dx12-rasterizer-desc.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM RASTERIZER es una especialización typedef de la plantilla \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**SUBOBJETO CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DE \_ SUBOBJETO DE ESTADO \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

