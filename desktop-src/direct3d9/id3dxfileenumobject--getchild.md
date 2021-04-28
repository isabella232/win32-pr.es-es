---
description: 'Método ID3DXFileEnumObject::GetChild: recupera un objeto secundario en este objeto de datos de archivo.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: Método ID3DXFileEnumObject::GetChild (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090363"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>Método ID3DXFileEnumObject::GetChild

Recupera un objeto secundario en este objeto de datos de archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*id* \[ en\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Identificador del objeto secundario que se recuperará.

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
