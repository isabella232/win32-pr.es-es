---
description: 'Método ID3DX10Mesh::GetIndexBuffer: recupera los datos de un búfer de índice.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: Método ID3DX10Mesh::GetIndexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084033"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>Método ID3DX10Mesh::GetIndexBuffer

Recupera los datos de un búfer de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Dirección de un puntero a una interfaz ID3DX10MeshBuffer, que representa el búfer de índice asociado a la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




