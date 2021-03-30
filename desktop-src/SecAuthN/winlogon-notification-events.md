---
description: Enumera los eventos de notificación de Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventos de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58827dc2699c92dfc3a814d2366608e1bd3fb662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907861"
---
# <a name="winlogon-notification-events"></a>Eventos de notificación de Winlogon

[*Winlogon*](../secgloss/w-gly.md) puede informar a su paquete de notificación de los siguientes eventos.



| Evento                               | Descripción                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bloquear**<br/>                 | Este evento se produce cuando el usuario bloquea la estación de trabajo.<br/>                                                                                                                                                                                                                                                   |
| **Forzado**<br/>               | Este evento se produce cuando un usuario cierra la sesión del sistema. El evento de **cierre de sesión** se realiza sincrónicamente, aunque la configuración del registro del paquete de notificación indique que puede controlar los eventos de forma asincrónica.<br/>                                                                                         |
| **Iniciar sesión**<br/>                | Este evento se produce cuando un usuario inicia sesión en el sistema.<br/> Tenga en cuenta que el evento **Logon** se produce antes de que se restauren las conexiones de red del usuario. Si el controlador de eventos requiere acceso a las conexiones de red del usuario, debe controlar el evento **StartShell** en lugar del evento **Logon** .<br/> |
| **Apagar**<br/>             | Este evento se produce justo antes de que se cierre el sistema.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Este evento se produce cuando un usuario inicia sesión en el sistema con una tarjeta inteligente.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Este evento se produce cuando se ha iniciado el protector de pantalla. Normalmente, esto sucede cuando un usuario ha estado inactivo durante un período de tiempo establecido.<br/> Las funciones que controlan este evento no deben mostrar una interfaz de usuario. La notificación de eventos **StartScreenSaver** está pensada únicamente con fines informativos.<br/> |
| **StartShell**<br/>           | Este evento se produce una vez que el usuario ha iniciado sesión en el sistema, se han establecido conexiones de red y se ha iniciado el programa de Shell especificado por el usuario (normalmente, el explorador de Windows).<br/>                                                                                                                |
| **Startup**<br/>              | Este evento se produce cuando se inicia o reinicia el sistema.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Este evento se produce cuando se detiene el protector de pantalla. Normalmente esto sucede cuando hay actividad del teclado o del mouse.<br/> Las funciones que controlan este evento no deben mostrar una interfaz de usuario. La notificación de eventos **StopScreenSaver** está pensada únicamente con fines informativos.<br/>                  |
| **Pulsa**<br/>               | Este evento se produce cuando el usuario desbloquea la estación de trabajo o cuando un administrador del sistema invalida el bloqueo y cierra la sesión del usuario.<br/>                                                                                                                                                                         |



 

 

 
