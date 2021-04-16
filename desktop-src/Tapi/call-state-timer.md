---
description: Actualmente, todo el tiempo de llamadas se deja en las aplicaciones.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Temporizador de estado de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677451"
---
# <a name="call-state-timer"></a><span data-ttu-id="ba5d0-103">Temporizador de estado de llamada</span><span class="sxs-lookup"><span data-stu-id="ba5d0-103">Call State Timer</span></span>

<span data-ttu-id="ba5d0-104">Actualmente, todo el tiempo de llamadas se deja en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="ba5d0-105">Esto puede ser oneroso si la aplicación está supervisando un gran número de llamadas y, si hay varias aplicaciones presentes, posiblemente en varios servidores, puede ser necesario para todo el mantenimiento de los temporizadores en las mismas llamadas.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="ba5d0-106">Por lo tanto, tiene más sentido que el servidor controle la sincronización del estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="ba5d0-107">El miembro **tStateEntryTime** de [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permite el control de tiempo de las llamadas en los Estados en los que se va a informar.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="ba5d0-108">El miembro (de tipo **SYSTIME**) indica la hora a la que se escribió el estado actual.</span><span class="sxs-lookup"><span data-stu-id="ba5d0-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



