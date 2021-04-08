---
description: Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer en iteración los objetos de datos de archivo secundarios en el archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interfaz ID3DXFileEnumObject (D3DX9Xof. h)
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
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003871"
---
# <a name="id3dxfileenumobject-interface"></a>Interfaz ID3DXFileEnumObject

Las aplicaciones usan los métodos de la interfaz ID3DXFileEnumObject para recorrer en iteración los objetos de datos de archivo secundarios en el archivo y recuperar un objeto secundario por su identificador único global (GUID) o por su nombre.

## <a name="members"></a>Miembros

La interfaz **ID3DXFileEnumObject** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileEnumObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXFileEnumObject** tiene estos métodos.



| Método                                                                  | Descripción                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Recupera un objeto secundario en este objeto de datos de archivo.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Recupera el número de objetos secundarios de este objeto de datos de archivo.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Recupera el objeto de datos que tiene el GUID especificado.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Recupera el objeto de datos que tiene el nombre especificado.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Recupera el objeto [**ID3DXFile**](id3dxfile.md) .<br/>            |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz ID3DXFileEnumObject es IID \_ ID3DXFileEnumObject.

El tipo LPD3DXFILEENUMOBJECT se define como un puntero a esta interfaz.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
