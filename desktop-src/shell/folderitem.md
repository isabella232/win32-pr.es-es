---
description: Representa un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.
title: Objeto FolderItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579588"
---
# <a name="folderitem-object"></a>Objeto FolderItem

Representa un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre el elemento.

## <a name="members"></a>Members

El **objeto FolderItem** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto FolderItem** tiene estos métodos.



| Método                                      | Descripción                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Ejecuta un verbo en el elemento.<br/>                                                                                                                     |
| [**Verbos**](folderitem-verbs.md)           | Recupera el objeto [**FolderItemVerbs del**](folderitemverbs.md) elemento. Este objeto es la colección de verbos que se pueden ejecutar en el elemento.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto FolderItem** tiene estas propiedades.



| Propiedad.                                                   | Tipo de acceso           | Descripción                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | Solo lectura<br/>  | Contiene el [**objeto Application**](folderitem-application.md) del elemento de carpeta.<br/>                                                                                                                   |
| [**Getfolder**](folderitem-getfolder.md)<br/>       | Solo lectura<br/>  | Contiene el objeto [**Folder del**](folder.md) elemento, si el elemento es una carpeta.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Solo lectura<br/>  | Contiene el objeto [**ShellLinkObject del**](shelllinkobject-object.md) elemento, si el elemento es un acceso directo.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Solo lectura<br/>  | Indica si el elemento se puede hospedar dentro de un explorador o Windows explorador.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Solo lectura<br/>  | Indica si el elemento forma parte del sistema de archivos.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Solo lectura<br/>  | Indica si el elemento es una carpeta.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Solo lectura<br/>  | Indica si el elemento es un acceso directo.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lectura y escritura<br/> | Establece u obtiene la fecha y hora en que se modificó por última vez un archivo. [**ModifyDate**](folderitem-modifydate.md) se puede usar para recuperar la fecha y hora en que se modificó por última vez una carpeta, pero no se puede establecer.<br/> |
| [**Nombre**](folderitem-name.md)<br/>                 | Lectura y escritura<br/> | Establece u obtiene el nombre del elemento.<br/>                                                                                                                                                                           |
| [**Parent**](folderitem-parent.md)<br/>             | Solo lectura<br/>  | Obtiene un objeto que representa el elemento primario del elemento.<br/>                                                                                                                                                  |
| [**Camino**](folderitem-path.md)<br/>                 | Solo lectura<br/>  | Contiene la ruta de acceso completa y el nombre del elemento.<br/>                                                                                                                                                                 |
| [**Tamaño**](folderitem-size.md)<br/>                 | Solo lectura<br/>  | Contiene el tamaño del elemento.<br/>                                                                                                                                                                               |
| [**Tipo**](folderitem-type.md)<br/>                 | Solo lectura<br/>  | Contiene una representación de cadena del tipo del elemento.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




