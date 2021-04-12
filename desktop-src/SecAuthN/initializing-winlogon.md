---
description: Cuando Winlogon se inicializa, registra la secuencia de atención segura (SAS) CTRL + ALT + SUPR en el sistema y, a continuación, crea tres equipos de escritorio en la estación de ventana de WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inicializando Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278575"
---
# <a name="initializing-winlogon"></a>Inicializando Winlogon

Cuando [Winlogon](winlogon.md) se inicializa, registra la [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Supr en el sistema y, a continuación, crea tres equipos de escritorio en la estación de ventana de WinSta0.

El registro de CTRL + ALT + SUPR hace que esta inicialización sea el primer proceso, lo que garantiza que ninguna otra aplicación ha enlazado esa secuencia de claves.

WinSta0 es el nombre del objeto de la estación de ventana que representa la pantalla física, el teclado y el mouse. Winlogon crea los siguientes escritorios en el objeto WinSta0.



| Escritorio              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escritorio Winlogon     | Este es el escritorio que Winlogon y [*Gina*](../secgloss/g-gly.md) usan para la identificación y autenticación interactiva y otros cuadros de diálogo seguros. Winlogon cambia automáticamente a este escritorio cuando recibe la notificación de eventos SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Escritorio de la aplicación  | Cada vez que un usuario inicia sesión correctamente, se crea un escritorio de aplicación para esa [*sesión de inicio*](../secgloss/l-gly.md)de sesión. El escritorio de la aplicación también se conoce como el escritorio predeterminado o de usuario. Este escritorio es el lugar en el que se realiza toda la actividad del usuario. El escritorio de la aplicación está protegido; solo el sistema y la sesión de inicio de sesión interactiva tienen acceso a ella. Tenga en cuenta que solo una instancia concreta del usuario que ha iniciado sesión tiene acceso al escritorio. Si el usuario interactivo activa un proceso mediante el controlador de servicio, esa aplicación de servicio no tendrá acceso al escritorio de la aplicación. |
| Escritorio del protector de pantalla | Este es el escritorio actual cuando se está ejecutando un protector de pantalla. Si un usuario ha iniciado sesión, tanto el sistema como la sesión de inicio de sesión interactivo tienen acceso al escritorio. De lo contrario, solo el sistema tiene acceso al escritorio.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Como propietario de estos escritorios, Winlogon puede cambiar el escritorio actual o visible a cualquiera de los tres equipos de escritorio y permitir que GINA tenga acceso a esta funcionalidad. En general, los desarrolladores de GINA no cambiarán el escritorio actual porque Winlogon establece el escritorio correctamente antes de comunicarse con GINA. La descripción de cada función de GINA indica qué escritorio es el actual para esa llamada.



| Para información acerca de                                    | Vea                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Los distintos Estados en los que se puede ejecutar Winlogon           | [Estados de Winlogon](winlogon-states.md)                                                                   |
| Operaciones de tiempo de espera                                      | [Cuadro de diálogo compatible Tiempo de servicio operaciones de salida](supported-dialog-box-service-time-out-operations.md) |
| Enviar mensajes a GINA mientras se muestra un cuadro de diálogo | [Envío de mensajes a GINA](sending-messages-to-the-gina.md)                                         |
| Funciones de soporte                                        | [Funciones de compatibilidad con Winlogon](authentication-functions.md)                    |



 

 

 
