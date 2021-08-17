---
description: Enumera los eventos de notificación de Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventos de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7359ef4d1d053e438d30564fcededbf3a0ccb10275cd6e4f669c2a20c54b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785725"
---
# <a name="winlogon-notification-events"></a>Eventos de notificación de Winlogon

[*Winlogon puede*](../secgloss/w-gly.md) informar al paquete de notificación de los siguientes eventos.



| Evento                               | Descripción                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bloquear**<br/>                 | Este evento tiene lugar cuando el usuario bloquea la estación de trabajo.<br/>                                                                                                                                                                                                                                                   |
| **Cerrar sesión**<br/>               | Este evento tiene lugar cuando un usuario cierra sesión del sistema. El **evento Logoff** se realiza de forma sincrónica, incluso si la configuración del Registro del paquete de notificación indica que puede controlar eventos de forma asincrónica.<br/>                                                                                         |
| **Iniciar sesión**<br/>                | Este evento tiene lugar cuando un usuario inicia sesión en el sistema.<br/> Tenga en cuenta que **el evento Logon** tiene lugar antes de restaurar las conexiones de red del usuario. Si el controlador de eventos requiere acceso a las conexiones de red del usuario, debe controlar el evento **de StartShell** en lugar del **evento Logon.**<br/> |
| **Apagar**<br/>             | Este evento tiene lugar justo antes de que se cierre el sistema.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Este evento tiene lugar cuando un usuario inicia sesión en el sistema con una tarjeta inteligente.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Este evento tiene lugar cuando se ha iniciado el protector de pantalla. Normalmente, esto sucede después de que un usuario haya estado inactivo durante un período de tiempo establecido.<br/> Las funciones que administran este evento no deben mostrar una interfaz de usuario. **La notificación de eventos StartScreenSaver** está pensada solo con fines informativos.<br/> |
| **StartShell**<br/>           | Este evento se produce después de que el usuario haya iniciado sesión en el sistema, se hayan establecido conexiones de red y se haya iniciado el programa de shell especificado por el usuario (normalmente Windows Explorer).<br/>                                                                                                                |
| **Startup**<br/>              | Este evento tiene lugar cuando se inicia o reinicia el sistema.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Este evento tiene lugar cuando se ha detenido el protector de pantalla. Normalmente esto sucede cuando hay actividad de teclado o mouse.<br/> Las funciones que administran este evento no deben mostrar una interfaz de usuario. **La notificación de eventos StopScreenSaver** está pensada solo con fines informativos.<br/>                  |
| **Desbloquear**<br/>               | Este evento tiene lugar cuando el usuario desbloquea la estación de trabajo o cuando un administrador del sistema invalida el bloqueo y cierra la sesión del usuario.<br/>                                                                                                                                                                         |



 

 

 
