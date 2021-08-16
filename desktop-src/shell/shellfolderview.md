---
description: Representa los objetos de una vista y proporciona propiedades y métodos utilizados para obtener información sobre el contenido de la vista.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objeto ShellFolderView (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a95d57edb7992c9511e34480190580d34ad42da23c64c4297f5e4ebb75a95e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452132"
---
# <a name="shellfolderview-object"></a>Objeto ShellFolderView

Representa los objetos de una vista y proporciona propiedades y métodos utilizados para obtener información sobre el contenido de la vista.

## <a name="members"></a>Miembros

El **objeto ShellFolderView** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto ShellFolderView** tiene estos eventos.



| Evento                                                        | Descripción                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.<br/> |



 

### <a name="methods"></a>Métodos

El **objeto ShellFolderView** tiene estos métodos.



| Método                                                 | Descripción                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Obtiene un [**objeto FolderItems**](folderitems.md) que representa todos los elementos seleccionados en la vista.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Establece el estado de selección de un elemento en la vista.<br/>                                                        |



 

### <a name="properties"></a>Propiedades

El **objeto ShellFolderView** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Application**](shellfolderview-application.md)<br/> | Solo lectura<br/> | Contiene el objeto Application del objeto .<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Solo lectura<br/> | Obtiene un [**objeto FolderItem**](folderitem.md) que representa el elemento que tiene el foco de entrada.<br/> |
| [**Carpeta**](shellfolderview-folder.md)<br/>           | Solo lectura<br/> | Obtiene un [**objeto Folder**](folder.md) que representa la vista.<br/>                                  |
| [**Parent**](shellfolderview-parent.md)<br/>           | Solo lectura<br/> | Sin implementar.<br/>                                                                                  |
| [**Guión**](shellfolderview-script.md)<br/>           | Solo lectura<br/> | En desuso.<br/>                                                                                       |
| [**ViewOptions**](shellfolderview-viewoptions.md)<br/> | Solo lectura<br/> | Obtiene un conjunto de marcas que indican las opciones actuales de la vista.<br/>                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ ShellFolderView<br/>                                                                              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Marcas de ShellFolderViewOptions**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




