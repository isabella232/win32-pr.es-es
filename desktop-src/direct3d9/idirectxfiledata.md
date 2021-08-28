---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o acceder a la jerarquía inmediata del objeto de datos.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interfaz IDirectXFileData (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 72b3ffa54d9ec0362100b2e2f1ac54b417d1425d0e6e311da3f9b5b7d30a553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800215"
---
# <a name="idirectxfiledata-interface"></a>Interfaz IDirectXFileData

Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o acceder a la jerarquía inmediata del objeto de datos. Las restricciones de plantilla determinan la jerarquía. Los tipos de datos permitidos por la plantilla se denominan miembros opcionales. Los miembros opcionales no son necesarios, pero un objeto podría perder información importante sin ellos. Estos miembros opcionales se guardan como elementos secundarios del objeto de datos. Los secundarios pueden ser otro objeto de datos, una referencia a un objeto de datos anterior o un objeto binario. En desuso.

## <a name="members"></a>Miembros

La **interfaz IDirectXFileData** hereda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileData también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileData tiene** estos métodos.



| Método                                                         | Descripción                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AddBinaryObject**](idirectxfiledata--addbinaryobject.md)   | Crea un objeto binario y lo agrega como un objeto secundario. En desuso.<br/>                                             |
| [**AddDataObject**](idirectxfiledata--adddataobject.md)       | Agrega un objeto de datos como un objeto secundario. En desuso.<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | Crea y agrega un objeto de referencia de datos como un objeto secundario. En desuso.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Recupera los datos de uno de los miembros del objeto o los datos de todos los miembros. En desuso.<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario en el archivo DirectX. En desuso.<br/> |
| [**Gettype**](idirectxfiledata--gettype.md)                   | Recupera el GUID de la plantilla del objeto. En desuso.<br/>                                                       |



 

## <a name="remarks"></a>Comentarios

El GUID de la interfaz IDirectXFileData es IID \_ IDirectXFileData.

El tipo LPDIRECTXFILEDATA se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




