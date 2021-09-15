---
description: Recupera el objeto de datos que tiene el GUID especificado.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: Método ID3DXFileEnumObject::GetDataObjectById (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568961"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>Método ID3DXFileEnumObject::GetDataObjectById

Recupera el objeto de datos que tiene el GUID especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rguid* \[ En\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Referencia al GUID solicitado.

</dd> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Dirección de un puntero a una [**interfaz ID3DXFileData,**](id3dxfiledata.md) que representa el objeto de datos de archivo devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.

## <a name="remarks"></a>Observaciones

Obtenga el guid rguid del objeto de datos de archivo actual con el [**método ID3DXFileData::GetId.**](id3dxfiledata--getid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
