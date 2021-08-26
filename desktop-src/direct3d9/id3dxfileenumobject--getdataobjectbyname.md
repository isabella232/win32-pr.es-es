---
description: Recupera el objeto de datos que tiene el nombre especificado.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: Método ID3DXFileEnumObject::GetDataObjectByName (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f42c82fb2eeedf6c1ec6c0f8099e6fbc1f6bac8d9e96bafbb6a94bacbf8f20e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951545"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>Método ID3DXFileEnumObject::GetDataObjectByName

Recupera el objeto de datos que tiene el nombre especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre solicitado.

</dd> <dt>

*ppObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Dirección de un puntero a una [**interfaz ID3DXFileData,**](id3dxfiledata.md) que representa el objeto de datos de archivo devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="remarks"></a>Comentarios

Obtenga el nombre szName del objeto de datos de archivo actual con el [**método ID3DXFileData::GetName.**](id3dxfiledata--getname.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
