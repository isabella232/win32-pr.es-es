---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFile para crear instancias de las interfaces IDirectXFileEnumObject e IDirectXFileSaveObject y para registrar plantillas. En desuso.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interfaz IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914794"
---
# <a name="idirectxfile-interface"></a>Interfaz IDirectXFile

Las aplicaciones usan los métodos de la interfaz IDirectXFile para crear instancias de las interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) y para registrar plantillas. En desuso.

## <a name="members"></a>Miembros

La interfaz **IDirectXFile** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDirectXFile** tiene estos métodos.



| Método                                                       | Descripción                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**CreateEnumObject**](idirectxfile--createenumobject.md)   | Crea un objeto de enumerador. En desuso.<br/> |
| [**CreateSaveObject**](idirectxfile--createsaveobject.md)   | Crea un objeto Save. En desuso.<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | Registra plantillas personalizadas. En desuso.<br/>   |



 

## <a name="remarks"></a>Observaciones

El identificador único global (GUID) de la interfaz IDirectXFile es IID \_ IDirectXFile.

La interfaz IDirectXFile se obtiene mediante una llamada a la función [**DirectXFileCreate**](directxfilecreate.md) .

El tipo LPDIRECTXFILE se define como un puntero a esta interfaz.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de archivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
