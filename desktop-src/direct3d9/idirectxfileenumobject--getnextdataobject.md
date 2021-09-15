---
description: Recupera el siguiente objeto de nivel superior en el archivo DirectX. En desuso.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: Método IDirectXFileEnumObject::GetNextDataObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466051"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>IDirectXFileEnumObject::GetNextDataObject (método)

Recupera el siguiente objeto de nivel superior en el archivo DirectX. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDataObj* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Dirección de un puntero a una [**interfaz IDirectXFileData,**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>Observaciones

Los objetos de nivel superior siempre son objetos de datos. Los objetos de referencia de datos y los objetos binarios solo pueden ser secundarios de objetos de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




