---
title: Estados de conexión
description: Durante el proceso de conexión a un servidor remoto, el administrador de conexiones de acceso remoto y el servidor RAS del equipo remoto realizan varios pasos para establecer la conexión.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904715"
---
# <a name="connection-states"></a>Estados de conexión

Durante el proceso de conexión a un servidor remoto, el administrador de conexiones de acceso remoto y el servidor RAS del equipo remoto realizan varios pasos para establecer la conexión. Cada uno de estos pasos se identifica mediante un estado de conexión. La enumeración [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) es un conjunto de valores que corresponden a estos Estados de conexión. Los Estados de conexión se pueden dividir en los tres grupos siguientes:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Estados en ejecución
</dt> <dd>

Los Estados en ejecución son las partes de la operación de conexión que RAS administra automáticamente, como la conexión a los dispositivos necesarios, la autenticación del usuario y la espera de una devolución de llamada desde el servidor remoto. A menos que se produzca un error, el cliente RAS no debe realizar ninguna acción que no sea para pasar la notificación al usuario.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Estados en pausa
</dt> <dd>

Los [Estados en pausa](paused-states.md) se producen cuando el servidor remoto pausa la operación de conexión para obtener información adicional del usuario. Durante un estado de pausa, el usuario puede escribir un número de [devolución de llamada](callback-connections.md) , un nombre de usuario y una contraseña diferentes si se produce un error en la autenticación del usuario, o una nueva contraseña si la antigua ha expirado.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Estados de terminal
</dt> <dd>

Los Estados de terminal se producen cuando la conexión se ha establecido correctamente, se ha producido un error en la operación de conexión o se ha interrumpido la conexión mediante una llamada a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

</dd> </dl>

Hay varios mecanismos que un cliente RAS puede utilizar para determinar el estado actual de una operación de conexión. Cuando un cliente RAS ejecuta la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma asincrónica, el administrador de conexiones de acceso remoto envía notificaciones de progreso al [controlador de notificación](notification-handlers.md) del cliente cada vez que cambia el estado de la conexión. Además, el cliente puede usar la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de cualquier operación de conexión RAS.

 

 