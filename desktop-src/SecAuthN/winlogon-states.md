---
description: Winlogon mantiene el estado de la estación de trabajo que usa GINA para determinar qué acciones de autenticación son necesarias.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Estados de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558342"
---
# <a name="winlogon-states"></a>Estados de Winlogon

[*Winlogon*](../secgloss/w-gly.md) mantiene el estado de la estación de trabajo que usa [*Gina*](../secgloss/g-gly.md) para determinar qué acciones de autenticación son necesarias.

En cualquier momento, Winlogon está en uno de estos tres Estados:

-   [Estado de cierre de sesión](#logged-off-state)
-   [Estado de la sesión iniciada](#logged-on-state)
-   [Estado de estación de trabajo bloqueada](#workstation-locked-state)

Estos tres Estados se muestran en la siguiente ilustración.

![Estados de Winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>Estado de Logged-Off

Cuando Winlogon está en el estado de cierre de sesión, se pide a los usuarios que se identifiquen y proporcionen información de autenticación. Si un usuario proporciona la información de la cuenta de usuario correcta y no hay restricciones que lo impidan, el usuario inicia sesión y se ejecuta un programa de Shell (como el explorador de Windows) en el escritorio de la aplicación. Winlogon cambia al estado de la sesión iniciada.

## <a name="logged-on-state"></a>Estado de Logged-On

Cuando Winlogon está en el estado de la sesión iniciada, los usuarios pueden interactuar con el Shell, activar aplicaciones adicionales y realizar su trabajo. Desde el estado de inicio de sesión, los usuarios pueden detener todo el trabajo y cerrar la sesión, o bien bloquear sus estaciones de trabajo (lo que deja todo el trabajo en su lugar). Si el usuario decide cerrar sesión, Winlogon finalizará todos los procesos asociados a esa [*sesión de inicio*](../secgloss/l-gly.md) de sesión y la estación de trabajo estará disponible para otro usuario. Si, en su lugar, el usuario decide bloquear la estación de trabajo, Winlogon cambia al estado bloqueado de la estación de trabajo.

## <a name="workstation-locked-state"></a>Estado de Workstation-Locked

Cuando Winlogon está en el estado de la estación de trabajo bloqueada, se muestra un escritorio seguro hasta que el usuario desbloquea la estación de trabajo proporcionando la misma información de identificación y autenticación que el usuario que inició sesión originalmente, o hasta que un administrador fuerza un cierre de sesión. Si la estación de trabajo está desbloqueada, se muestra el escritorio de la aplicación y se puede reanudar el trabajo. Sin embargo, si un administrador desbloquea la estación de trabajo (proporcionando la información de identificación y autenticación de una cuenta de administrador), los procesos del usuario que ha iniciado sesión se terminan y Winlogon cambia al estado de cierre de sesión.

En cada uno de los Estados de Winlogon se pueden realizar varias acciones diferentes. Un archivo DLL de GINA puede implementar acciones que no forman parte del sistema operativo Windows estándar. Por ejemplo, un sistema de alta seguridad podría bloquear automáticamente una estación de trabajo cada 10 minutos y forzar a los usuarios a volver a autenticarse.

Para obtener información sobre la creación de escritorios y el registro de una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS), consulte [inicializar Winlogon](initializing-winlogon.md). Para obtener información acerca de las operaciones de tiempo de espera, vea el [cuadro de diálogo compatible tiempo de servicio operaciones de salida](supported-dialog-box-service-time-out-operations.md). Para obtener información acerca de cómo enviar mensajes a GINA mientras se muestra un cuadro de diálogo, vea [envío de mensajes a Gina](sending-messages-to-the-gina.md). Para obtener más información sobre las funciones de soporte, consulte [funciones de compatibilidad de Winlogon](authentication-functions.md).

 

 
