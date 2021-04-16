---
description: Recupera el objeto de datos que tiene el nombre especificado.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject:: GetDataObjectByName (método) (D3DX9Xof. h)'
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
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707969"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>ID3DXFileEnumObject:: GetDataObjectByName (método)

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

*szName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre solicitado.

</dd> <dt>

*ppObj* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Dirección de un puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="remarks"></a>Observaciones

Obtiene el nombre szName del objeto de datos de archivo actual con el método [**ID3DXFileData:: GetName**](id3dxfiledata--getname.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
