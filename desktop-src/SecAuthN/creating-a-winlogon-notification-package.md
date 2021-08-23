---
description: Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos logon de cada paquete de notificación para proporcionar información sobre el evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Creación de un paquete de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84d0290f7afeba7a427f5c50caf1638fd88bfdb4b52ee513a9b1c0506aed9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008873"
---
# <a name="creating-a-winlogon-notification-package"></a>Creación de un paquete de notificación de Winlogon

Un [*paquete de notificación de Winlogon*](/windows/desktop/SecGloss/w-gly) es un archivo DLL que exporta funciones que controlan eventos winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos logon de cada paquete de notificación para proporcionar información sobre el evento.

Los nombres de las funciones de controlador de eventos implementadas en un paquete de notificación se deja al desarrollador. Winlogon comprueba el Registro para obtener los nombres de las funciones del controlador de eventos. Por ejemplo, un paquete de notificación podría implementar la función de controlador de eventos logon como `WLEventLogon` , mientras que otro podría usar `HandleLogonEvent` .

No es necesario implementar y registrar controladores de eventos para cada evento winlogon, solo para los eventos que son útiles para la aplicación. Cada función de controlador de eventos debe usar el prototipo de función descrito en [Prototipo de función del controlador de eventos](event-handler-function-prototype.md). Este prototipo tiene un único parámetro: una estructura [**DE INFORMACIÓN DE \_ NOTIFICACIÓN \_ DE WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene detalles sobre el evento.

Winlogon omite la salida de las funciones del controlador de eventos. Si controlar un evento requiere interactuar con Winlogon, use las funciones de soporte [técnico de Winlogon](authentication-functions.md).

Para usar el paquete de notificación de Winlogon, el archivo DLL debe copiarse en la carpeta %SystemRoot% system32 y se debe realizar una actualización del Registro para el \\ paquete de notificación. Para obtener información sobre la actualización del Registro, [vea Registrar un paquete de notificación de Winlogon.](registering-a-winlogon-notification-package.md)

 

 
