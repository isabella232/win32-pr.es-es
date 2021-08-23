---
description: El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios.
ms.assetid: 672ad753-210b-41c3-b8c7-e041ce7b1671
title: Notificaciones de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12186ab6349057258d723f7e690e889b7e79af4abe47f714055599cb6f648333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636625"
---
# <a name="device-notifications"></a>Notificaciones de dispositivos

El sistema difunde un conjunto de eventos de cambio de dispositivo predeterminados a todas las aplicaciones y servicios. No es necesario registrarse para recibir estos eventos predeterminados. Consulte la sección Comentarios de [**RegisterDeviceNotification para**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) obtener más información. Para especificar otros eventos que la aplicación o el servicio deben recibir, use **la función RegisterDeviceNotification.**

Cuando una aplicación o servicio llama [**a RegisterDeviceNotification,**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)también especifica la ventana que recibirá los eventos de notificación. Los servicios pueden especificar un identificador de estado de servicio en lugar de un identificador de ventana. Si un servicio especifica su identificador de estado de servicio, su controlador de control de servicio recibirá los eventos de notificación. Para obtener más información, vea [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Asegúrese de controlar los eventos Plug and Play dispositivo lo antes posible. De lo contrario, el sistema puede dejar de responder. Si el controlador de eventos va a realizar una operación que puede bloquear la ejecución (por ejemplo, E/S), es mejor iniciar otro subproceso para realizar la operación de forma asincrónica.

Los identificadores de notificación de dispositivo devueltos por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) deben cerrarse llamando a la función [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) cuando ya no sean necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro para recibir notificaciones del dispositivo](registering-for-device-notification.md)
</dt> </dl>

 

 
