---
description: Dado que la API de instalación no proporciona una rutina de devolución de llamada del archivo. cab predeterminada, debe proporcionar una rutina. La rutina de devolución de llamada que requiere la función SetupIterateCabinet debe tener la misma forma que la que señala FileCallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Crear una rutina de devolución de llamada de archivador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277142"
---
# <a name="creating-a-cabinet-callback-routine"></a>Crear una rutina de devolución de llamada de archivador

Dado que la API de instalación no proporciona una rutina de devolución de llamada del archivo. cab predeterminada, debe proporcionar una rutina. La rutina de devolución de llamada que requiere la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) debe tener la misma forma que la que señala [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).

A continuación se encuentra la sintaxis que usa [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para enviar una notificación a la rutina de devolución de llamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

El parámetro de *contexto* es un puntero nulo a una estructura o variable de contexto que puede usar la rutina de devolución de llamada para almacenar información que debe persistir entre las llamadas subsiguientes a la rutina de devolución de llamada.

La implementación de este contexto se especifica mediante la rutina de devolución de llamada y nunca se hace referencia a él ni se modifica mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

El parámetro de *notificación* es un entero sin signo y tendrá uno de los valores siguientes.



| notificación                                                        | Descripción                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | El archivo se ha extraído del archivo. cab.      |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | Se encuentra un archivo en el archivo. cab.              |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | El archivo actual continúa en el siguiente archivo. cab. |



 

Los dos parámetros finales, *Param1* y *Param2*, son también enteros sin signo y contienen información adicional relevante para la notificación. Para obtener más información sobre las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consulte [notificaciones de archivo. cab](cabinet-file-notifications.md).

Una \_ rutina de devolución de llamada de notificación de archivo Sp \_ \_ devuelve un entero sin signo. La rutina de devolución de llamada del archivo. cab debe devolver uno de los valores siguientes en función de la notificación.

En el caso de la notificación de FILEINCABINET de SPFILENOTIFY \_ , [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) espera que la rutina de devolución de llamada devuelva uno de los valores siguientes.



| Value         | Significado                   |
|---------------|---------------------------|
| \_anulación de FILEOP | Anular el procesamiento del archivo. cab. |
| FILEOP \_ Doit  | Extraiga el archivo actual. |
| FILEOP \_ SKIP  | Omitir el archivo actual.    |



 

En el caso de \_ las notificaciones de SPFILENOTIFY NEEDNEWCABINET y SPFILENOTIFY \_ FILEEXTRACTED, **SetupIterateCabinet** espera que la rutina de devolución de llamada devuelva uno de los valores siguientes.



| Value      | Significado                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SIN \_ errores  | No se encontró ningún error y continúe procesando el archivo. cab.                                                                                                                                                                        |
| ERROR \_ XXX | Se produjo un error del tipo especificado. La función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá **false** y el código de error especificado será devuelto por una llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). |



 

Si la rutina de devolución de llamada devuelve FILEOP \_ doit, la rutina también debe proporcionar una ruta de acceso de destino completa. Para obtener más información, vea [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).

 

 
