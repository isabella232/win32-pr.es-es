---
description: 'Evento ShellFolderView.SelectionChanged: se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.'
title: Evento ShellFolderView.SelectionChanged (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842576"
---
# <a name="shellfolderviewselectionchanged-event"></a>Evento ShellFolderView.SelectionChanged

Se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.

## <a name="syntax"></a>Sintaxis


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parámetros

Este controlador de eventos no tiene parámetros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




