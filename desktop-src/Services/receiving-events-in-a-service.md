---
description: Un servicio que es una aplicación de consola puede registrar un controlador de control de consola para recibir una notificación cuando un usuario cierra la sesión.
ms.assetid: 86ace8b8-c1cb-4646-bc92-86bd578a82c5
title: Recepción de eventos en un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95f7329383ffc8aea08102a2fe8cf8b49e0ef9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476344"
---
# <a name="receiving-events-in-a-service"></a>Recepción de eventos en un servicio

Un servicio que es una aplicación de consola puede registrar un controlador [de control de](/windows/console/console-control-handlers) consola para recibir una notificación cuando un usuario cierra la sesión. Sin embargo, no se envía ningún evento de consola cuando un usuario interactivo inicia sesión. Para obtener información sobre cómo recibir notificaciones cuando un usuario inicia sesión, consulte [Creación de un paquete de notificación de Winlogon.](/windows/desktop/SecAuthN/creating-a-winlogon-notification-package)

El sistema difunde eventos de cambio de dispositivo a todos los servicios. Un servicio puede recibir estos eventos en un procedimiento de ventana o en su controlador de control de servicio. Para especificar qué eventos debe recibir el servicio, use [**la función RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

Asegúrese de controlar los eventos Plug and Play dispositivo lo antes posible. De lo contrario, es posible que el sistema deje de responder. Si el controlador de eventos va a realizar una operación que puede bloquear la ejecución (como E/S), es mejor iniciar otro subproceso para realizar la operación de forma asincrónica.

Cuando un servicio llama a [**RegisterDeviceNotification,**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)el servicio también especifica un identificador de ventana o un identificador de estado de servicio. Si un servicio especifica un identificador de ventana, el procedimiento de ventana recibe los eventos de notificación. Si un servicio especifica su identificador de estado de servicio, su controlador de control de servicio recibe los eventos de notificación. Para obtener más información, [**vea HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex).

Los identificadores de notificación de dispositivo devueltos por [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) deben cerrarse llamando a la función [**UnregisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification) cuando ya no sean necesarios.

 

 
