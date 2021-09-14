---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileEnumObject para recorrer los objetos de datos del archivo y recuperar un objeto de datos por su identificador único global (GUID) o por su nombre. En desuso.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interfaz IDirectXFileEnumObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174730"
---
# <a name="idirectxfileenumobject-interface"></a>Interfaz IDirectXFileEnumObject

Las aplicaciones usan los métodos de la interfaz IDirectXFileEnumObject para recorrer los objetos de datos del archivo y recuperar un objeto de datos por su identificador único global (GUID) o por su nombre. En desuso.

## <a name="members"></a>Members

La **interfaz IDirectXFileEnumObject** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileEnumObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileEnumObject** tiene estos métodos.



| Método                                                                     | Descripción                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | Recupera el objeto de datos que tiene el GUID especificado. En desuso.<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | Recupera el objeto de datos que tiene el nombre especificado. En desuso.<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | Recupera el siguiente objeto de nivel superior en el archivo DirectX. En desuso.<br/> |



 

## <a name="remarks"></a>Observaciones

El GUID de la interfaz IDirectXFileEnumObject es IID \_ IDirectXFileEnumObject.

El tipo LPDIRECTXFILEENUMOBJECT se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
