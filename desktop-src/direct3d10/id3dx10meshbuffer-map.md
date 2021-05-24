---
description: Obtenga un puntero a la memoria del búfer de malla para modificar su contenido.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: Método ID3DX10MeshBuffer::Map (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335359"
---
# <a name="id3dx10meshbuffermap-method"></a>Método ID3DX10MeshBuffer::Map

Obtenga un puntero a la memoria del búfer de malla para modificar su contenido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Puntero a los datos del búfer.

</dd> <dt>

*pSize* \[ out\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Tamaño del búfer en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios



 Diferencias entre Direct3D 9 y Direct3D 10:

- Map() en Direct3D 10 es análogo al recurso Map() en Direct3D 9.



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
