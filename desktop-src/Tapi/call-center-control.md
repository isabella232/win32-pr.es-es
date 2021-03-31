---
description: El TAPI 2,2 básico se puede usar para administrar centros de llamadas y otros elementos de la infraestructura de red de telefonía (por ejemplo, servidores de correo de voz y IVR) a través del control de llamadas de terceros.
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: Control de centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911546"
---
# <a name="call-center-control"></a><span data-ttu-id="301b7-103">Control de centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="301b7-103">Call Center Control</span></span>

<span data-ttu-id="301b7-104">El TAPI 2,2 básico se puede usar para administrar centros de llamadas y otros elementos de la infraestructura de red de telefonía (por ejemplo, servidores de correo de voz y IVR) a través del control de llamadas de terceros.</span><span class="sxs-lookup"><span data-stu-id="301b7-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="301b7-105">Para ayudar a crear proxies ACD que se ejecutarán en servidores, se han agregado funciones a TAPI 2,2 para proporcionar asistencia adicional a los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="301b7-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="301b7-106">En los temas siguientes se describen las características de TAPI 2,2 que puede usar para implementar controles de centro de llamadas:</span><span class="sxs-lookup"><span data-stu-id="301b7-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="301b7-107">Modelado de un centro de llamadas</span><span class="sxs-lookup"><span data-stu-id="301b7-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="301b7-108">Cadenas</span><span class="sxs-lookup"><span data-stu-id="301b7-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="301b7-109">Marcado predictivo</span><span class="sxs-lookup"><span data-stu-id="301b7-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="301b7-110">Colas de llamadas y puntos de ruta</span><span class="sxs-lookup"><span data-stu-id="301b7-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="301b7-111">Supervisión y control del agente ACD</span><span class="sxs-lookup"><span data-stu-id="301b7-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="301b7-112">Control de estado de la estación</span><span class="sxs-lookup"><span data-stu-id="301b7-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="301b7-113">Control de estado de la estación</span><span class="sxs-lookup"><span data-stu-id="301b7-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="301b7-114">Temporizador de estado de llamada</span><span class="sxs-lookup"><span data-stu-id="301b7-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="301b7-115">Temporizadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="301b7-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="301b7-116">TAPI 3. x es la API preferida para escribir aplicaciones del agente ACD.</span><span class="sxs-lookup"><span data-stu-id="301b7-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="301b7-117">Vea la sección [controles del centro de llamadas](./about-call-center-controls.md) para obtener información sobre el uso de estas interfaces y métodos.</span><span class="sxs-lookup"><span data-stu-id="301b7-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="301b7-118">Sin embargo, TAPI 2,2 sigue siendo utilizable para conjuntos de aplicaciones de ACD completo si se desea.</span><span class="sxs-lookup"><span data-stu-id="301b7-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
