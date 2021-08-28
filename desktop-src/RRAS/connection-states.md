---
title: Estados de conexión
description: Durante el proceso de conexión a un servidor remoto, el Connection Manager de acceso remoto y el servidor RAS del equipo remoto realizan varios pasos para establecer la conexión.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e52e1e4ea4a071f6606681aa2dc2fc15e88df659f8fd16746abf2d84727d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074225"
---
# <a name="connection-states"></a>Estados de conexión

Durante el proceso de conexión a un servidor remoto, el Connection Manager de acceso remoto y el servidor RAS del equipo remoto realizan varios pasos para establecer la conexión. Cada uno de estos pasos se identifica mediante un estado de conexión. La [**enumeración RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) es un conjunto de valores que corresponden a estos estados de conexión. Los estados de conexión se pueden dividir en los tres grupos siguientes:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Estados en ejecución
</dt> <dd>

Los estados en ejecución son las partes de la operación de conexión que RAS controla automáticamente, como conectarse a los dispositivos necesarios, autenticar al usuario y esperar una devolución de llamada desde el servidor remoto. A menos que se produzca un error, el cliente RAS no necesita realizar ninguna acción que no sea pasar la notificación al usuario.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Estados en pausa
</dt> <dd>

Los [estados en pausa se](paused-states.md) producen cuando el servidor remoto pausa la operación de conexión para obtener entradas adicionales del usuario. Durante un estado en pausa, [](callback-connections.md) el usuario puede escribir un número de devolución de llamada, un nombre de usuario y una contraseña diferentes si se produce un error en la autenticación del usuario o una nueva contraseña si la antigua ha expirado.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Estados terminales
</dt> <dd>

Los estados de terminal se producen cuando la conexión se ha establecido correctamente, la operación de conexión no se ha realizado correctamente o se ha roto la conexión mediante una [**llamada a RasHangUp.**](/windows/desktop/api/Ras/nf-ras-rashangupa)

</dd> </dl>

Hay varios mecanismos que un cliente RAS puede usar para determinar el estado actual de una operación de conexión. Cuando un cliente RAS ejecuta la función [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma asincrónica, el Connection Manager de [](notification-handlers.md) acceso remoto envía notificaciones de progreso al controlador de notificaciones del cliente cada vez que cambia el estado de conexión. Además, el cliente puede usar la [**función RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de cualquier operación de conexión RAS.

 

 