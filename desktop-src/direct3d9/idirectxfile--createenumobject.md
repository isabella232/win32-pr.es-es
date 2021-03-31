---
description: Crea un objeto de enumerador. En desuso.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile:: CreateEnumObject (método) (DXFile. h)'
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
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821354"
---
# <a name="idirectxfilecreateenumobject-method"></a>IDirectXFile:: CreateEnumObject (método)

Crea un objeto de enumerador. En desuso.

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

*pvSource* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a los datos cuyo contenido depende del valor de dwLoadOptions

</dd> <dt>

*dwLoadOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**

Valor que especifica el origen de los datos. Este valor puede ser una de las \_ marcas DXFILELOAD XXX en las [constantes DXFILE](dxfile.md).

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

Dirección de un puntero a una interfaz [**IDirectXFileEnumObject**](idirectxfileenumobject.md) que representa el objeto de enumerador creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Observaciones

Después de usar este método, use uno de los métodos IDirectXFileEnumObject para recuperar un objeto de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
