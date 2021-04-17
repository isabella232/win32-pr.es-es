---
description: El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones desde el control de dispositivos, liberando a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marzo en lógico.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modelo de programación de telefonía de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686478"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="6a742-103">Modelo de programación de telefonía de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6a742-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="6a742-104">El modelo de programación de telefonía de Microsoft abstrae el control de comunicaciones desde el control de dispositivos, liberando a las aplicaciones de usuario final y a los fabricantes de dispositivos de la necesidad de marzo en lógico.</span><span class="sxs-lookup"><span data-stu-id="6a742-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="6a742-105">Con este modelo, una aplicación de servidor o de usuario final no necesita información detallada sobre el control de dispositivo y no es necesario que el dispositivo esté adaptado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6a742-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="6a742-106">Las aplicaciones y los dispositivos pueden someterse a la innovación y al cambio sin necesidad de representar a los clientes.</span><span class="sxs-lookup"><span data-stu-id="6a742-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="6a742-107">En el diagrama siguiente se muestra cómo se realiza esta abstracción.</span><span class="sxs-lookup"><span data-stu-id="6a742-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![Cómo abstrae TAPI el control de comunicaciones del control de dispositivo](images/tapicomp.png)

<span data-ttu-id="6a742-109">Estos componentes se pueden ver como repositorios de conocimientos especializados.</span><span class="sxs-lookup"><span data-stu-id="6a742-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="6a742-110">La aplicación de interfaz de programación de aplicaciones de telefonía (TAPI) conoce las necesidades de los usuarios, la DLL de TAPI y TAPISRV comprenden la telefonía general y los proveedores de servicios (TSP y MSP) saben el control detallado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a742-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="6a742-111">Los escritores de aplicaciones y los fabricantes de dispositivos solo necesitan conocimientos generales de los requisitos de los demás.</span><span class="sxs-lookup"><span data-stu-id="6a742-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="6a742-112">Una aplicación carga el archivo DLL de TAPI en su espacio de proceso y usa TAPI para comunicar las necesidades.</span><span class="sxs-lookup"><span data-stu-id="6a742-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="6a742-113">TAPI establece comunicaciones de vínculo RPC con el servidor TAPI.</span><span class="sxs-lookup"><span data-stu-id="6a742-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="6a742-114">Además, TAPI 3. x crea un objeto MSP y se comunica con él mediante un conjunto definido de comandos, la interfaz del proveedor de servicios multimedia (MSPI).</span><span class="sxs-lookup"><span data-stu-id="6a742-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="6a742-115">Cuando una aplicación llama a una operación de TAPI, la biblioteca de vínculos dinámicos TAPI valida y calcula las referencias de los parámetros y, a continuación, reenvía la información a TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="6a742-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="6a742-116">TAPISRV realiza un seguimiento de los recursos de comunicaciones disponibles en el equipo local e interactúa con los proveedores de servicios de telefonía (profesionales) mediante la interfaz del proveedor de servicios de telefonía (TSPI).</span><span class="sxs-lookup"><span data-stu-id="6a742-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="6a742-117">Las comunicaciones entre un TSP y un MSP tienen lugar mediante una conexión virtual que pasa a través de la DLL de TAPI y TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="6a742-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="6a742-118">El par TSP/MSP proporciona información sobre el estado y las capacidades del dispositivo e implementa los comandos específicos necesarios para una respuesta deseada.</span><span class="sxs-lookup"><span data-stu-id="6a742-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="6a742-119">El resultado de utilizar este modelo de programación es que las aplicaciones pueden omitir o ajustarse a los cambios del dispositivo y los nuevos dispositivos pueden ser útiles al instante en lugar de esperar a que se produzcan cambios en el código base.</span><span class="sxs-lookup"><span data-stu-id="6a742-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="6a742-120">La cuota de mercado potencial se expande para los escritores de aplicaciones y los fabricantes de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6a742-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="6a742-121">En los temas siguientes se describen los componentes de telefonía de Microsoft con más detalle:</span><span class="sxs-lookup"><span data-stu-id="6a742-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="6a742-122">Aplicaciones TAPI</span><span class="sxs-lookup"><span data-stu-id="6a742-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="6a742-123">DLL DE TAPI</span><span class="sxs-lookup"><span data-stu-id="6a742-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="6a742-124">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="6a742-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="6a742-125">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="6a742-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="6a742-126">Modelo sincrónico/asincrónico</span><span class="sxs-lookup"><span data-stu-id="6a742-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="6a742-127">Estructuras de datos TAPI</span><span class="sxs-lookup"><span data-stu-id="6a742-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="6a742-128">Niveles de servicio de TAPI</span><span class="sxs-lookup"><span data-stu-id="6a742-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



