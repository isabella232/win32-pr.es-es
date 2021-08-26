---
description: Crea un objeto enumerador. En desuso.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: Método IDirectXFile::CreateEnumObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af10a0f46877a159ab8c6543fba9c1406d083e6b3f4a57cf1c41b9fb2d92612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985155"
---
# <a name="idirectxfilecreateenumobject-method"></a>IDirectXFile::CreateEnumObject (método)

Crea un objeto enumerador. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pvSource* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a datos cuyo contenido depende del valor de dwLoadOptions

</dd> <dt>

*dwLoadOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**

Valor que especifica el origen de los datos. Este valor puede ser una de las marcas \_ DXFILELOAD xxx en constantes [DXFILE](dxfile.md).

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

Dirección de un puntero a una [**interfaz IDirectXFileEnumObject,**](idirectxfileenumobject.md) que representa el objeto enumerador creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Comentarios

Después de usar este método, use uno de los métodos IDirectXFileEnumObject para recuperar un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
