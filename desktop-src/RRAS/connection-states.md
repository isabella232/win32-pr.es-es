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
# <a name="connection-states"></a><span data-ttu-id="7d068-103">Estados de conexión</span><span class="sxs-lookup"><span data-stu-id="7d068-103">Connection States</span></span>

<span data-ttu-id="7d068-104">Durante el proceso de conexión a un servidor remoto, el administrador de conexiones de acceso remoto y el servidor RAS del equipo remoto realizan varios pasos para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="7d068-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="7d068-105">Cada uno de estos pasos se identifica mediante un estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="7d068-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="7d068-106">La enumeración [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) es un conjunto de valores que corresponden a estos Estados de conexión.</span><span class="sxs-lookup"><span data-stu-id="7d068-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="7d068-107">Los Estados de conexión se pueden dividir en los tres grupos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7d068-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="7d068-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Estados en ejecución</span><span class="sxs-lookup"><span data-stu-id="7d068-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="7d068-109">Los Estados en ejecución son las partes de la operación de conexión que RAS administra automáticamente, como la conexión a los dispositivos necesarios, la autenticación del usuario y la espera de una devolución de llamada desde el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="7d068-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="7d068-110">A menos que se produzca un error, el cliente RAS no debe realizar ninguna acción que no sea para pasar la notificación al usuario.</span><span class="sxs-lookup"><span data-stu-id="7d068-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="7d068-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Estados en pausa</span><span class="sxs-lookup"><span data-stu-id="7d068-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="7d068-112">Los [Estados en pausa](paused-states.md) se producen cuando el servidor remoto pausa la operación de conexión para obtener información adicional del usuario.</span><span class="sxs-lookup"><span data-stu-id="7d068-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="7d068-113">Durante un estado de pausa, el usuario puede escribir un número de [devolución de llamada](callback-connections.md) , un nombre de usuario y una contraseña diferentes si se produce un error en la autenticación del usuario, o una nueva contraseña si la antigua ha expirado.</span><span class="sxs-lookup"><span data-stu-id="7d068-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="7d068-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Estados de terminal</span><span class="sxs-lookup"><span data-stu-id="7d068-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="7d068-115">Los Estados de terminal se producen cuando la conexión se ha establecido correctamente, se ha producido un error en la operación de conexión o se ha interrumpido la conexión mediante una llamada a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .</span><span class="sxs-lookup"><span data-stu-id="7d068-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="7d068-116">Hay varios mecanismos que un cliente RAS puede utilizar para determinar el estado actual de una operación de conexión.</span><span class="sxs-lookup"><span data-stu-id="7d068-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="7d068-117">Cuando un cliente RAS ejecuta la función [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de forma asincrónica, el administrador de conexiones de acceso remoto envía notificaciones de progreso al [controlador de notificación](notification-handlers.md) del cliente cada vez que cambia el estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="7d068-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="7d068-118">Además, el cliente puede usar la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de cualquier operación de conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="7d068-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 