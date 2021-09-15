---
description: Indica que el objeto ShellFolderView ha terminado de enumerar el contenido de la carpeta.
title: Evento ShellFolderViewOC.EnumDone (Shldisp.h)
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
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579517"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC.EnumDone

Indica que el [**objeto ShellFolderView**](shellfolderview.md) ha terminado de enumerar el contenido de la carpeta.

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

El [**objeto ShellFolderView**](shellfolderview.md) debe enumerar el contenido de una carpeta para poder mostrarlo. Con carpetas grandes o ubicadas en un sistema remoto, este proceso puede tardar hasta varios minutos. Durante este tiempo, se muestra un gráfico animado de la luz para indicar al usuario que se está procesando. Una vez completada la enumeración, se desencadena el evento **EnumDone** y el gráfico de la linterna se reemplaza por el contenido de la carpeta.

Proporcione código de control de eventos para este evento como se muestra aquí.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




