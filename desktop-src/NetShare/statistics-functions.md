---
description: El sistema operativo Windows acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia el servicio de estación de trabajo o servidor.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funciones de estadísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678205"
---
# <a name="statistics-functions"></a><span data-ttu-id="3b4eb-103">Funciones de estadísticas</span><span class="sxs-lookup"><span data-stu-id="3b4eb-103">Statistics Functions</span></span>

<span data-ttu-id="3b4eb-104">El sistema operativo Windows acumula un conjunto de estadísticas de funcionamiento para estaciones de trabajo y servidores desde el momento en que se inicia el servicio de estación de trabajo o servidor.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="3b4eb-105">Para recuperar estas estadísticas, puede llamar a la siguiente función de estadísticas de administración de redes.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="3b4eb-106">Función</span><span class="sxs-lookup"><span data-stu-id="3b4eb-106">Function</span></span>                                     | <span data-ttu-id="3b4eb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b4eb-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b4eb-108">**NetStatisticsGet**</span><span class="sxs-lookup"><span data-stu-id="3b4eb-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="3b4eb-109">Recupera las estadísticas de funcionamiento de un servicio. admite los servicios de estación de trabajo y servidor.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="3b4eb-110">La función **NetStatisticsGet** devuelve una estructura de la [**estación de trabajo de STAT \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) cuando se solicitan estadísticas de la estación de trabajo; la función devuelve una estructura de [**\_ servidor \_**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) de estadísticas cuando se solicitan estadísticas del servidor.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



