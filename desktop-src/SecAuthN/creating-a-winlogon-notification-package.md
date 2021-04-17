---
description: Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos de Winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos Logon de cada paquete de notificaciones para proporcionar información sobre el evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Crear un paquete de notificación Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652683"
---
# <a name="creating-a-winlogon-notification-package"></a>Crear un paquete de notificación Winlogon

Un paquete de notificación de [*Winlogon*](/windows/desktop/SecGloss/w-gly) es un archivo DLL que exporta funciones que controlan eventos de Winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos Logon de cada paquete de notificaciones para proporcionar información sobre el evento.

Los nombres de las funciones del controlador de eventos que se implementan en un paquete de notificación se dejan al desarrollador; Winlogon comprueba el registro para obtener los nombres de las funciones de controlador de eventos. Por ejemplo, un paquete de notificación podría implementar la función de controlador de eventos Logon como, `WLEventLogon` mientras que otra podría usar `HandleLogonEvent` .

No es necesario implementar y registrar controladores de eventos para todos los eventos Winlogon, solo para los eventos que son útiles para la aplicación. Cada función de controlador de eventos debe usar el prototipo de función descrito en [prototipo de función de controlador de eventos](event-handler-function-prototype.md). Este prototipo tiene un único parámetro: una estructura de [**\_ \_ información de notificación WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene detalles sobre el evento.

Winlogon omite la salida de las funciones de controlador de eventos. Si el control de un evento requiere interactuar con Winlogon, use las [funciones de compatibilidad de Winlogon](authentication-functions.md).

Para usar el paquete de notificación de Winlogon, el archivo DLL debe copiarse en la carpeta% SystemRoot% \\ system32 y debe realizarse una actualización del registro para el paquete de notificación. Para obtener información acerca de la actualización del registro, consulte [registrar un paquete de notificación de Winlogon](registering-a-winlogon-notification-package.md).

 

 
