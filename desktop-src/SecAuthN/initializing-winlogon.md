---
description: Cuando Winlogon se inicializa, registra la secuencia de atención segura (SAS) CTRL+ALT+SUPR con el sistema y, a continuación, crea tres escritorios dentro de la estación de ventana de WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inicialización de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff33740b77b23577cd7749b8cc745cd06a55e18675e35b817e405a71679b482
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482397"
---
# <a name="initializing-winlogon"></a>Inicialización de Winlogon

Cuando [Winlogon](winlogon.md) se inicializa, registra la secuencia de atención segura [*(SAS)*](../secgloss/s-gly.md) CTRL+ALT+SUPR con el sistema y, a continuación, crea tres escritorios dentro de la estación de ventana de WinSta0.

El registro de CTRL+ALT+SUPR convierte esta inicialización en el primer proceso, lo que garantiza que ninguna otra aplicación haya conectado esa secuencia de claves.

WinSta0 es el nombre del objeto de estación de ventana que representa la pantalla física, el teclado y el mouse. Winlogon crea los siguientes escritorios en el objeto WinSta0.



| Escritorio              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escritorio winlogon     | Este es el escritorio que Winlogon y [*GINA*](../secgloss/g-gly.md) usan para la identificación y autenticación interactivas, y otros cuadros de diálogo seguros. Winlogon cambia automáticamente a este escritorio cuando recibe la notificación de eventos de SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Escritorio de aplicaciones  | Cada vez que un usuario inicia sesión correctamente, se crea un escritorio de aplicación para esa [*sesión de inicio de sesión.*](../secgloss/l-gly.md) El escritorio de la aplicación también se conoce como el escritorio predeterminado o de usuario. Este escritorio es donde tiene lugar toda la actividad del usuario. El escritorio de la aplicación está protegido; solo el sistema y la sesión de inicio de sesión interactiva tienen acceso a él. Tenga en cuenta que solo una instancia determinada del usuario que ha iniciado sesión tiene acceso al escritorio. Si el usuario interactivo activa un proceso mediante el controlador de servicio, esa aplicación de servicio no tendrá acceso al escritorio de la aplicación. |
| Escritorio de protector de pantalla | Este es el escritorio actual cuando se ejecuta un protector de pantalla. Si un usuario ha iniciado sesión, tanto el sistema como la sesión de inicio de sesión interactiva tienen acceso al escritorio. De lo contrario, solo el sistema tiene acceso al escritorio.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Como propietario de estos escritorios, Winlogon puede cambiar el escritorio actual o visible a cualquiera de los tres escritorios y permitir el acceso de GINA a esta funcionalidad. En general, los desarrolladores de GINA no cambiarán el escritorio actual porque Winlogon establece el escritorio correctamente antes de comunicarse con GINA. La descripción de cada función GINA indica qué escritorio está actual para esa llamada.



| Para información acerca de                                    | Vea                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Los distintos estados en los que se puede ejecutar Winlogon           | [Estados de Winlogon](winlogon-states.md)                                                                   |
| Operaciones de tiempo de espera                                      | [Operaciones de tiempo de espera de servicio de cuadro de diálogo admitidas](supported-dialog-box-service-time-out-operations.md) |
| Envío de mensajes a GINA mientras se muestra un cuadro de diálogo | [Envío de mensajes a la GINA](sending-messages-to-the-gina.md)                                         |
| Funciones de soporte técnico                                        | [Funciones de soporte técnico de Winlogon](authentication-functions.md)                    |



 

 

 
