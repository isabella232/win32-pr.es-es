---
description: En esta sección se describen las estructuras NPP utilizadas por los métodos NPP.
ms.assetid: f0729dc5-6b5f-4f24-85d6-47c45f1bf9be
title: Estructuras NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b514bded37450f6a7c33a016b231bb38f0c1812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686997"
---
# <a name="npp-structures"></a><span data-ttu-id="93c2a-103">Estructuras NPP</span><span class="sxs-lookup"><span data-stu-id="93c2a-103">NPP Structures</span></span>

<span data-ttu-id="93c2a-104">En esta sección se describen las estructuras NPP utilizadas por los métodos NPP.</span><span class="sxs-lookup"><span data-stu-id="93c2a-104">This section describes the NPP structures used by NPP methods.</span></span> <span data-ttu-id="93c2a-105">Estas estructuras se utilizan para recuperar estadísticas, proporcionar el estado del sistema e información estadística e indicar qué equipos ejecutan Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="93c2a-105">These structures are used to retrieve statistics, provide system status and statistical information, and indicate which computers are running Network Monitor.</span></span> <span data-ttu-id="93c2a-106">En las tablas siguientes se describen estas estructuras.</span><span class="sxs-lookup"><span data-stu-id="93c2a-106">The following tables describes these structures.</span></span>



| <span data-ttu-id="93c2a-107">Estructuras NPP</span><span class="sxs-lookup"><span data-stu-id="93c2a-107">NPP Structures</span></span>                     | <span data-ttu-id="93c2a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="93c2a-108">Description</span></span>                                                                                                                      |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93c2a-109">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="93c2a-109">SESSIONSTATS</span></span>](sessionstats.md)   | <span data-ttu-id="93c2a-110">Proporciona información de sesión cuando se recuperan las estadísticas de conversación.</span><span class="sxs-lookup"><span data-stu-id="93c2a-110">Provides session information when conversation statistics are retrieved.</span></span>                                                         |
| [<span data-ttu-id="93c2a-111">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="93c2a-111">STATIONSTATS</span></span>](stationstats.md)   | <span data-ttu-id="93c2a-112">Proporciona estadísticas sobre una [*estación*](s.md)específica.</span><span class="sxs-lookup"><span data-stu-id="93c2a-112">Provides statistics about a specific [*station*](s.md).</span></span>                                                     |
| [<span data-ttu-id="93c2a-113">STATISTICS</span><span class="sxs-lookup"><span data-stu-id="93c2a-113">STATISTICS</span></span>](statistics.md)       | <span data-ttu-id="93c2a-114">Proporciona estadísticas de red cuando se recuperan Estadísticas totales y cuando la captura actual se ha pausado o detenido.</span><span class="sxs-lookup"><span data-stu-id="93c2a-114">Provides network statistics when total statistics are retrieved and when the current capture has paused or stopped.</span></span>              |
| [<span data-ttu-id="93c2a-115">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="93c2a-115">QUERYTABLE</span></span>](querytable.md)       | <span data-ttu-id="93c2a-116">Indica qué equipos están usando Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="93c2a-116">Indicates which computers are using Network Monitor.</span></span>                                                                             |
| [<span data-ttu-id="93c2a-117">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="93c2a-117">STATIONQUERY</span></span>](stationquery.md)   | <span data-ttu-id="93c2a-118">Proporciona información acerca de un equipo que usa Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="93c2a-118">Provides information about a computer that is using Network Monitor.</span></span> <span data-ttu-id="93c2a-119">La estructura de la **QUERYTABLE** NPP usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="93c2a-119">This structure is used by the NPP **QUERYTABLE** structure.</span></span> |
| [<span data-ttu-id="93c2a-120">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="93c2a-120">NETWORKSTATUS</span></span>](networkstatus.md) | <span data-ttu-id="93c2a-121">Proporciona el estado actual de la red en términos de estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="93c2a-121">Provides current network status in terms of system state.</span></span>                                                                        |



 

 

 



