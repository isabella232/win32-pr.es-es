---
description: 'Método ID3DX10Mesh::GetVertexBuffer: recupera el búfer de vértices asociado a la malla.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: Método ID3DX10Mesh::GetVertexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 804ece9ca82fbdd8dc5778b888fecc4ca8fbc04b8fc45976b857b417343f4b32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069985"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>Método ID3DX10Mesh::GetVertexBuffer

Recupera el búfer de vértices asociado a la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Búfer de vértice que se obtiene. Se trata de un valor de índice.

</dd> <dt>

*ppVertexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Búfer de vértice. Consulte [ **ID3DX10MeshBuffer.**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
