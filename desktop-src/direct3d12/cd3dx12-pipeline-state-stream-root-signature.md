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
ms.openlocfilehash: ccddd5663b6a079656823efed4cb48b3183d88d0688149c7ae05d96e8dc1cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530714"
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



## <a name="members"></a>Miembros

<dl> <dt>

**FIRMA RAÍZ DE LA SECUENCIA DE ESTADO DE CANALIZACIÓN CD3DX12 \_ \_ \_ \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una FIRMA RAÍZ DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM ROOT \_ \_ \_ \_ SIGNATURE(ID3D12RootSignature \* const &i)**
</dt> <dd>

Crea una nueva instancia de UNA FIRMA RAÍZ DE FLUJO DE ESTADO DE CANALIZACIÓN CD3DX12, inicializada con un tipo de subobjeto D3D12 PIPELINE STATE SUBOBJECT TYPE ROOT SIGNATURE y datos de subobjetos copiados de i , una estructura \_ \_ \_ \_ \_ **\_ \_ \_ \_ \_ \_** [**ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) 

</dd> <dt>

**operator=(ID3D12RootSignature \* const& i)**
</dt> <dd>

Operador de asignación de copia.

</dd> <dt>

**operator ID3D12RootSignature \* () const**
</dt> <dd>

Conversión implícita a un [**puntero de estructura ID3D12RootSignature.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature)

</dd> </dl>

## <a name="remarks"></a>Comentarios

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

[**TIPO DE SUBOBJETO DE ESTADO \_ \_ DE CANALIZACIÓN \_ D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

