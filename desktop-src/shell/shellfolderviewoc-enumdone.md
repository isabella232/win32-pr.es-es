---
description: Indica que el objeto ShellFolderView ha terminado de enumerar el contenido de la carpeta.
title: Evento ShellFolderViewOC. EnumDone (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997861"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC. EnumDone

Indica que el objeto [**ShellFolderView**](shellfolderview.md) ha terminado de enumerar el contenido de la carpeta.

## <a name="syntax"></a>Sintaxis


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Parámetros

Este controlador de eventos no tiene parámetros.

## <a name="remarks"></a>Observaciones

El objeto [**ShellFolderView**](shellfolderview.md) debe enumerar el contenido de una carpeta antes de poder mostrarla. Con las carpetas que son grandes o se encuentran en un sistema remoto, este proceso puede tardar hasta varios minutos. Durante este tiempo, se muestra un gráfico de linterna animada para indicar al usuario que el procesamiento está en curso. Una vez completada la enumeración, se desencadena el evento **EnumDone** y el gráfico de linterna se sustituye por el contenido de la carpeta.

Proporcione el código de control de eventos para este evento, tal como se muestra aquí.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




