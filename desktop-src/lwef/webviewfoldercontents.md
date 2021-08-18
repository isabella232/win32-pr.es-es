---
title: Objeto WebViewFolderContents (Shldisp.h)
description: Implementado por el shell para su uso dentro de una vista web.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Características heredadas del entorno de Windows objeto WebViewFolderContents
- Objeto WebViewFolderContents Características heredadas del entorno Windows , descrito
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fe0146f49d0e5172410ca119953a7b3f245af20c0e4c2d83ff78fa23b93e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035963"
---
# <a name="webviewfoldercontents-object"></a>Objeto WebViewFolderContents

Implementado por el shell para su uso dentro de *un control WebView*. **WebViewFolderContents** se inicializa automáticamente en la carpeta actual de WebView. Crea una vista de carpeta de Shell que muestra el contenido de la carpeta en uno de estos cinco formatos: Icono pequeño, Icono grande, Lista, Detalles o Miniatura. No es válido fuera de webView.

Los métodos y propiedades **expuestos por WebViewFolderContents** son idénticos a los del [**objeto ShellFolderView.**](/windows/desktop/shell/shellfolderview)

## <a name="members"></a>Miembros

El **objeto WebViewFolderContents** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Eventos

El **objeto WebViewFolderContents** tiene estos eventos.



| Evento                                                              | Descripción                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.<br/> |



 

### <a name="methods"></a>Métodos

El **objeto WebViewFolderContents** tiene estos métodos.



| Método                                                       | Descripción                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Obtiene un [**objeto FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Establece el estado de selección de un elemento en la vista.<br/>                                                          |



 

### <a name="properties"></a>Propiedades

El **objeto WebViewFolderContents** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso          | Descripción                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](webviewfoldercontents-application.md)<br/> | Solo lectura<br/> | Sin implementar.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Solo lectura<br/> | Obtiene un [**objeto FolderItem**](../shell/folderitem.md) que representa el elemento que tiene el foco de entrada.<br/>                           |
| [**Carpeta**](webviewfoldercontents-folder.md)<br/>           | Solo lectura<br/> | Obtiene un [**objeto Folder**](../shell/folder.md) que representa la vista.<br/>                                                            |
| [**Parent**](webviewfoldercontents-parent.md)<br/>           | Solo lectura<br/> | Sin implementar.<br/>                                                                                                              |
| [**Guión**](webviewfoldercontents-script.md)<br/>           | Solo lectura<br/> | Obtiene el objeto de scripting para la vista.<br/>                                                                                       |
| [**ViewOptions**](webviewfoldercontents-viewoptions.md)<br/> | Solo lectura<br/> | Obtiene un conjunto de [**marcas ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indican las opciones actuales de la vista.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

