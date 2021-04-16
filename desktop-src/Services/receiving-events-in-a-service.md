---
description: Un servicio que es una aplicación de consola puede registrar un controlador de control de consola para recibir una notificación cuando un usuario cierra la sesión.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Recepción de eventos en un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546798"
---
# <a name="receiving-events-in-a-service"></a>Recepción de eventos en un servicio

Un servicio que es una aplicación de consola puede registrar un [controlador de control de consola](/windows/console/console-control-handlers) para recibir una notificación cuando un usuario cierra la sesión. Sin embargo, no se envía ningún evento de consola cuando un usuario interactivo inicia sesión. Para obtener información sobre la recepción de notificaciones cuando un usuario inicia sesión, consulte [crear un paquete de notificación de Winlogon](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package).

El sistema difunde los eventos de cambio de dispositivo a todos los servicios. Estos eventos pueden ser recibidos por un servicio en un procedimiento de ventana o en su controlador de control de servicio. Para especificar los eventos que debe recibir el servicio, utilice la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

Asegúrese de controlar Plug and Play eventos de dispositivo lo más rápido posible. De lo contrario, es posible que el sistema deje de responder. Si el controlador de eventos va a realizar una operación que puede bloquear la ejecución (como e/s), es mejor iniciar otro subproceso para realizar la operación de forma asincrónica.

Cuando un servicio llama a [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa), el servicio también especifica un identificador de ventana o un identificador de estado de servicio. Si un servicio especifica un identificador de ventana, el procedimiento de ventana recibe los eventos de notificación. Si un servicio especifica su identificador de estado de servicio, su controlador de control de servicio recibe los eventos de notificación. Para obtener más información, vea [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Los identificadores de notificación de dispositivo devueltos por [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) deben cerrarse llamando a la función [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) cuando ya no se necesiten.

 

 
