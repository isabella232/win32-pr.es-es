---
title: Información de conexión y configuración de RAS
description: Las aplicaciones que se ejecutan en Windows NT 4,0 y versiones posteriores, y Windows 95, pueden usar la función RasEnumConnections para obtener información acerca de las conexiones existentes en el equipo local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuración y conexión, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676149"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="aab12-104">Información de conexión y configuración de RAS</span><span class="sxs-lookup"><span data-stu-id="aab12-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="aab12-105">Las aplicaciones que se ejecutan en Windows NT 4,0 y versiones posteriores, y Windows 95, pueden usar la función [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obtener información acerca de las conexiones existentes en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="aab12-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="aab12-106">La información de cada conexión incluye un identificador de conexión y el nombre de la entrada de la libreta de teléfonos utilizada para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="aab12-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="aab12-107">Puede usar el identificador de conexión en una llamada a la función [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) para obtener el estado actual de la conexión.</span><span class="sxs-lookup"><span data-stu-id="aab12-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="aab12-108">Windows NT Server 4,0 y versiones posteriores proporcionan dos funciones nuevas para recuperar información de RAS.</span><span class="sxs-lookup"><span data-stu-id="aab12-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="aab12-109">Windows 95does no admite estas funciones.</span><span class="sxs-lookup"><span data-stu-id="aab12-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="aab12-110">La función [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) devuelve el nombre y el tipo de los dispositivos compatibles con ras que están configurados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="aab12-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="aab12-111">La función [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica un objeto de evento que el sistema señala cuando se crea o finaliza una conexión RAS.</span><span class="sxs-lookup"><span data-stu-id="aab12-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




