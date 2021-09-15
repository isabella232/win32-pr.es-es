---
description: Recupera el objeto de datos que tiene el nombre especificado. En desuso.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: Método IDirectXFileEnumObject::GetDataObjectByName (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569897"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a>IDirectXFileEnumObject::GetDataObjectByName (método)

Recupera el objeto de datos que tiene el nombre especificado. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre solicitado.

</dd> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Dirección de un puntero a una [**interfaz IDirectXFileData,**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
