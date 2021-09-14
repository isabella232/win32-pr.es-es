---
description: Winlogon mantiene el estado de la estación de trabajo que usa la GINA para determinar qué acciones de autenticación son necesarias.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Estados de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160870"
---
# <a name="winlogon-states"></a>Estados de Winlogon

[*Winlogon mantiene*](../secgloss/w-gly.md) el estado de la estación de trabajo que usa [*la GINA*](../secgloss/g-gly.md) para determinar qué acciones de autenticación son necesarias.

En cualquier momento, Winlogon se encuentra en uno de estos tres estados:

-   [Estado de la sesión iniciada](#logged-off-state)
-   [Estado de la sesión iniciada](#logged-on-state)
-   [Estado bloqueado de estación de trabajo](#workstation-locked-state)

Estos tres estados se muestran en la ilustración siguiente.

![Estados de winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>Logged-Off estado

Cuando Winlogon está en el estado de apagado, se pide a los usuarios que se identifiquen y proporcionen información de autenticación. Si un usuario proporciona la información correcta de la cuenta de usuario y ninguna restricción lo impide, el usuario inicia sesión y se ejecuta un programa de shell (como Windows Explorer) en el escritorio de la aplicación. Winlogon cambia al estado de la sesión iniciada.

## <a name="logged-on-state"></a>Logged-On estado

Cuando Winlogon está en estado de sesión iniciada, los usuarios pueden interactuar con el shell, activar aplicaciones adicionales y realizar su trabajo. Desde el estado de inicio de sesión, los usuarios pueden detener todo el trabajo y cerrar la sesión, o bloquear sus estaciones de trabajo (dejando todo el trabajo en su lugar). Si el usuario decide cerrar sesión, Winlogon finalizará [](../secgloss/l-gly.md) todos los procesos asociados a esa sesión de inicio de sesión y la estación de trabajo estará disponible para otro usuario. Si, en su lugar, el usuario decide bloquear la estación de trabajo, Winlogon cambia al estado bloqueado por la estación de trabajo.

## <a name="workstation-locked-state"></a>Workstation-Locked estado

Cuando Winlogon está en estado bloqueado en la estación de trabajo, se muestra un escritorio seguro hasta que el usuario desbloquea la estación de trabajo proporcionando la misma información de identificación y autenticación que el usuario que inició sesión originalmente, o hasta que un administrador fuerza un cierre de sesión. Si la estación de trabajo está desbloqueada, se muestra el escritorio de la aplicación y se puede reanudar el trabajo. Sin embargo, si un administrador desbloquea la estación de trabajo (proporcionando la información de identificación y autenticación de una cuenta de administrador), los procesos del usuario que ha iniciado sesión finalizan y Winlogon cambia al estado de apagado.

Se pueden realizar varias acciones diferentes en cada uno de los estados de Winlogon. Un archivo DLL de GINA puede implementar acciones que no forman parte del sistema operativo Windows estándar. Por ejemplo, un sistema de alta seguridad podría bloquear automáticamente una estación de trabajo cada 10 minutos y forzar a los usuarios a que se vuelvan a autenticar.

Para obtener información sobre cómo crear escritorios y registrar una secuencia de [*atención*](../secgloss/s-gly.md) segura (SAS), consulte [Inicialización de Winlogon.](initializing-winlogon.md) Para obtener información sobre las operaciones de tiempo de espera, vea Operaciones de tiempo de espera del servicio de cuadro de [diálogo admitidas.](supported-dialog-box-service-time-out-operations.md) Para obtener información sobre cómo enviar mensajes a la GINA mientras se muestra un cuadro de diálogo, vea Envío de [mensajes a la GINA](sending-messages-to-the-gina.md). Para obtener información sobre las funciones de soporte técnico, [consulte Funciones de soporte técnico de Winlogon.](authentication-functions.md)

 

 
