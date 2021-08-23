---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer los objetos de datos de archivo secundarios del archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaz ID3DXFileEnumObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4c274a42a5e07f05af3b0b2ffe18dc3fbaf546591f23e6f24906cd1723578303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121364"
---
# <a name="id3dxfileenumobject-interface"></a>Interfaz ID3DXFileEnumObject

Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer los objetos de datos de archivo secundarios del archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.

## <a name="members"></a>Miembros

La **interfaz ID3DXFileEnumObject** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileEnumObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXFileEnumObject** tiene estos métodos.



| Método                                                                  | Descripción                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Recupera un objeto secundario en este objeto de datos de archivo.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Recupera el número de objetos secundarios de este objeto de datos de archivo.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Recupera el objeto de datos que tiene el GUID especificado.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Recupera el objeto de datos que tiene el nombre especificado.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Recupera el [**objeto ID3DXFile.**](id3dxfile.md)<br/>            |



 

## <a name="remarks"></a>Comentarios

El GUID de la interfaz ID3DXFileEnumObject es IID \_ ID3DXFileEnumObject.

El tipo LPD3DXFILEENUMOBJECT se define como un puntero a esta interfaz.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivos D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
