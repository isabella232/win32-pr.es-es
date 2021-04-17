---
description: Recupera los datos en un búfer de índice.
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'ID3DX10Mesh:: GetIndexBuffer (método) (D3DX10. h)'
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
ms.openlocfilehash: c2777a9d530ac7217b1cc0f3c0f148998cc70ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424400"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>ID3DX10Mesh:: GetIndexBuffer (método)

Recupera los datos en un búfer de índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIndexBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Dirección de un puntero a una interfaz ID3DX10MeshBuffer que representa el búfer de índice asociado a la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




