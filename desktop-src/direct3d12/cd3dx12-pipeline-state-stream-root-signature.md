---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE estructura (D3dx12.h)
description: Estructura auxiliar que se usa para describir la firma raíz como un único objeto adecuado para una descripción de secuencia.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE estructura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969847"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>Estructura DE FIRMA RAÍZ DE LA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_

Estructura auxiliar que se usa para describir la firma raíz como un único objeto adecuado para una descripción de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**FIRMA RAÍZ DE LA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una FIRMA RAÍZ DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE(ID3D12RootSignature \* const &i)**
</dt> <dd>

Crea una nueva instancia de UNA FIRMA RAÍZ DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE ROOT SIGNATURE y datos de subobjeto copiados de i , una estructura \_ \_ \_ \_ \_ **\_ \_ \_ \_ \_ \_** [**ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) 

</dd> <dt>

**operator=(ID3D12RootSignature \* const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operator ID3D12RootSignature \* () const**
</dt> <dd>

Conversión implícita a un [**puntero de estructura ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature)

</dd> </dl>

## <a name="remarks"></a>Observaciones

CD3DX12 PIPELINE STATE STREAM ROOT SIGNATURE es una especialización typedef de la plantilla \_ \_ \_ \_ \_ [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

