---
description: Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos logon de cada paquete de notificación para proporcionar información sobre el evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Creación de un paquete de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161011"
---
# <a name="creating-a-winlogon-notification-package"></a>Creación de un paquete de notificación de Winlogon

Un [*paquete de notificación de Winlogon*](/windows/desktop/SecGloss/w-gly) es un archivo DLL que exporta funciones que controlan eventos winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos logon de cada paquete de notificación para proporcionar información sobre el evento.

El desarrollador deja los nombres de las funciones de controlador de eventos implementadas en un paquete de notificación. Winlogon comprueba el registro para obtener los nombres de las funciones del controlador de eventos. Por ejemplo, un paquete de notificación podría implementar la función de controlador de eventos logon como `WLEventLogon` , mientras que otro podría usar `HandleLogonEvent` .

No es necesario implementar ni registrar controladores de eventos para cada evento winlogon, solo para los eventos que son útiles para la aplicación. Cada función de controlador de eventos debe usar el prototipo de función descrito en [Prototipo de función de controlador de eventos](event-handler-function-prototype.md). Este prototipo tiene un único parámetro: una estructura [**DE INFORMACIÓN DE NOTIFICACIÓN \_ DE \_ WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene detalles sobre el evento.

Winlogon omite la salida de las funciones del controlador de eventos. Si para controlar un evento es necesario interactuar con Winlogon, use las [funciones de soporte técnico de Winlogon](authentication-functions.md).

Para usar el paquete de notificación de Winlogon, el archivo DLL debe copiarse en la carpeta %SystemRoot% system32 y se debe realizar una actualización del Registro para el \\ paquete de notificación. Para obtener información sobre la actualización del Registro, vea [Registrar un paquete de notificación de Winlogon.](registering-a-winlogon-notification-package.md)

 

 
