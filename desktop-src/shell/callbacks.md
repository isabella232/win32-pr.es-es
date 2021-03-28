---
description: En esta sección se describen las funciones de devolución de llamada del shell de Windows.
title: Funciones de devolución de llamada de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423719"
---
# <a name="shell-callback-functions"></a>Funciones de devolución de llamada de Shell

En esta sección se describen las funciones de devolución de llamada del shell de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Especifica una función de devolución de llamada definida por la aplicación que se usa para enviar y procesar mensajes desde un cuadro de diálogo de **exploración** mostrado en respuesta a una llamada a [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos para comunicarse con una extensión del administrador de archivos.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).<br/>                                                                                                                                   |
| [**PAPPSTATE \_ , \_ rutina de cambio**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Especifica una función de devolución de llamada definida por la aplicación que notifica a la aplicación cuando la aplicación entra o sale de un estado suspendido.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Define el prototipo de la función de devolución de llamada usada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) y [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**\_proc UNdelete de FM \_**](undeletefile.md)<br/>                     | Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando **Undelete** en el menú **archivo** .<br/>                                                                   |



 

 

 
