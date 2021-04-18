---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interfaz IDirectXFileData (DXFile. h)
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
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718386"
---
# <a name="idirectxfiledata-interface"></a>Interfaz IDirectXFileData

Las aplicaciones usan los métodos de la interfaz IDirectXFileData para compilar o tener acceso a la jerarquía inmediata del objeto de datos. Las restricciones de las plantillas determinan la jerarquía. Los tipos de datos permitidos por la plantilla se denominan miembros opcionales. Los miembros opcionales no son necesarios, pero es posible que un objeto pierda información importante sin ellos. Estos miembros opcionales se guardan como elementos secundarios del objeto de datos. Los elementos secundarios pueden ser otro objeto de datos, una referencia a un objeto de datos anterior o un objeto binario. En desuso.

## <a name="members"></a>Miembros

La interfaz **IDirectXFileData** hereda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDirectXFileData** tiene estos métodos.



| Método                                                         | Descripción                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AddBinaryObject**](idirectxfiledata--addbinaryobject.md)   | Crea un objeto binario y lo agrega como un objeto secundario. En desuso.<br/>                                             |
| [**AddDataObject**](idirectxfiledata--adddataobject.md)       | Agrega un objeto de datos como un objeto secundario. En desuso.<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | Crea y agrega un objeto de referencia de datos como un objeto secundario. En desuso.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Recupera los datos para uno de los miembros del objeto o los datos de todos los miembros. En desuso.<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | Recupera el siguiente objeto de datos secundario, el objeto de referencia de datos o el objeto binario del archivo de DirectX. En desuso.<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | Recupera el GUID de la plantilla del objeto. En desuso.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz IDirectXFileData es IID \_ IDirectXFileData.

El tipo LPDIRECTXFILEDATA se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




