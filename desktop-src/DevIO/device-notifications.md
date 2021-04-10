---
description: El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificaciones de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caeee8ba50a62a3bc393172347be09d1ac58085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153334"
---
# <a name="device-notifications"></a>Notificaciones de dispositivo

El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios. No es necesario registrarse para recibir estos eventos predeterminados. Vea la sección Comentarios en [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) para obtener más información. Para especificar otros eventos que debe recibir la aplicación o el servicio, utilice la función **RegisterDeviceNotification** .

Cuando una aplicación o un servicio llama a [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), también especifica la ventana que recibirá los eventos de notificación. Los servicios pueden especificar un identificador de estado de servicio en lugar de un identificador de ventana. Si un servicio especifica su identificador de estado de servicio, su controlador de control de servicio recibirá los eventos de notificación. Para obtener más información, vea [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Asegúrese de controlar Plug and Play eventos de dispositivo lo más rápido posible. De lo contrario, es posible que el sistema deje de responder. Si el controlador de eventos va a realizar una operación que puede bloquear la ejecución (como e/s), es mejor iniciar otro subproceso para realizar la operación de forma asincrónica.

Los identificadores de notificación de dispositivo devueltos por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) deben cerrarse llamando a la función [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) cuando ya no se necesiten.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro para recibir notificaciones del dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
