---
description: Representa una carpeta shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Objeto Folder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032623"
---
# <a name="folder-object"></a>Objeto Folder

Representa una carpeta shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la carpeta.

## <a name="members"></a>Miembros

El **objeto Folder** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Folder** tiene estos métodos.



| Método                                      | Descripción                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Copia un elemento o elementos en una carpeta.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Recupera detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de su última modificación.<br/> |
| [**Elementos**](folder-items.md)               | Recupera un objeto [**FolderItems**](folderitems.md) que representa la colección de elementos de la carpeta .<br/>    |
| [**MoveHere**](folder-movehere.md)         | Mueve un elemento o elementos a esta carpeta.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Crea una nueva carpeta.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Crea y devuelve un [**objeto FolderItem**](folderitem.md) que representa un elemento especificado.<br/>                 |



 

### <a name="properties"></a>Propiedades

El **objeto Folder** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso          | Descripción                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | Solo lectura<br/> | Contiene el objeto Application de la carpeta.<br/> |
| [**Parent**](folder-parent.md)<br/>             | Solo lectura<br/> | Sin implementar.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Solo lectura<br/> | Contiene el objeto **Folder** primario.<br/>    |
| [**Título**](folder-title.md)<br/>               | Solo lectura<br/> | Contiene el título de la carpeta.<br/>         |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS). Si intenta llamar a un método sin implementar, se 0x800A01BD error (decimal 445).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                 |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




