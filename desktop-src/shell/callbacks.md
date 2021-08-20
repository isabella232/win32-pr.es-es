---
description: En esta sección se describen las Windows de devolución de llamada de Shell.
title: Funciones de devolución de llamada de shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3fd334dd49d2b9cec3322630866fde4a99ccad0b5f253dd7253e551264737a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460848"
---
# <a name="shell-callback-functions"></a>Funciones de devolución de llamada de shell

En esta sección se describen las Windows de devolución de llamada de Shell.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Especifica una función de devolución de llamada definida por la aplicación  que se usa para enviar y procesar mensajes desde un cuadro de diálogo Examinar que se muestra en respuesta a una llamada a [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos para comunicarse con una extensión del Administrador de archivos.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Se usa para determinar si un elemento está presente en una lista usada más recientemente (MRU).<br/>                                                                                                                                   |
| [**RUTINA DE CAMBIO DE \_ \_ PAPPSTATE**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Especifica una función de devolución de llamada definida por la aplicación que notifica a la aplicación cuando la aplicación entra o sale de un estado suspendido.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Define el prototipo de la función de devolución de llamada utilizada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) [**y SetWindowSubclass.**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)<br/>                                                   |
| [**FM \_ UNDELETE \_ PROC**](undeletefile.md)<br/>                     | Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos cuando el usuario elige el comando **Undelete** en el **menú** Archivo.<br/>                                                                   |



 

 

 
