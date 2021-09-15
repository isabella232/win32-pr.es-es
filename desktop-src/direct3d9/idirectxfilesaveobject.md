---
description: Las aplicaciones usan los métodos de la interfaz IDirectXFileSaveObject para crear objetos de datos y guardar plantillas y objetos de datos.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interfaz IDirectXFileSaveObject (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569661"
---
# <a name="idirectxfilesaveobject-interface"></a>Interfaz IDirectXFileSaveObject

Las aplicaciones usan los métodos de la interfaz IDirectXFileSaveObject para crear objetos de datos y guardar plantillas y objetos de datos. Tenga en cuenta que las plantillas no son necesarias en todos los archivos. Por ejemplo, podría colocar todas las plantillas en un único archivo de Microsoft DirectX en lugar de duplicarlas en cada archivo DirectX. En desuso.

## <a name="members"></a>Members

La **interfaz IDirectXFileSaveObject** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileSaveObject** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirectXFileSaveObject** tiene estos métodos.



| Método                                                               | Descripción                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | Crea un objeto de datos. En desuso.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Guarda un objeto de datos y sus secundarios en un archivo DirectX. En desuso.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Guarda las plantillas en un archivo DirectX. En desuso.<br/>                      |



 

## <a name="remarks"></a>Observaciones

El identificador único global (GUID) de la interfaz IDirectXFileSaveObject es **IID \_ IDirectXFileSaveObject**.

La **interfaz IDirectXFileSaveObject** se obtiene llamando al método [**IDirectXFile::CreateSaveObject.**](idirectxfile--createsaveobject.md)

El **tipo LPDIRECTXFILESAVEOBJECT** se define como un puntero a esta interfaz.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
