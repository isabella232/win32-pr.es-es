---
description: La versión 3,1 de TAPI es una API basada en COM que combina la telefonía clásica y la IP. Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada (RTC) pública a conferencias de IP Multimedia multidifusión con calidad de servicio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Información general de TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687489"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="1814e-104">Información general de TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1814e-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="1814e-105">La versión 3,1 de TAPI es una API basada en COM que combina la telefonía clásica y la IP.</span><span class="sxs-lookup"><span data-stu-id="1814e-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="1814e-106">Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada (RTC) pública a conferencias de IP Multimedia multidifusión con calidad de servicio (QOS).</span><span class="sxs-lookup"><span data-stu-id="1814e-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="1814e-107">Para obtener más información acerca de las capacidades de telefonía IP de TAPI 3,1, consulte las notas del producto "telefonía IP con TAPI 3", que encontrará en el sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1814e-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="1814e-108">Hay cuatro componentes principales de TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="1814e-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="1814e-109">API DE COM</span><span class="sxs-lookup"><span data-stu-id="1814e-109">COM API</span></span>
-   <span data-ttu-id="1814e-110">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="1814e-110">TAPI Server</span></span>
-   <span data-ttu-id="1814e-111">Proveedores de servicios de telefonía (profesionales)</span><span class="sxs-lookup"><span data-stu-id="1814e-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="1814e-112">Proveedores de flujo de medios (MSP)</span><span class="sxs-lookup"><span data-stu-id="1814e-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="1814e-113">En el siguiente diagrama se ilustra la arquitectura de TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="1814e-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![arquitectura de TAPI 3](images/callarc-gif-1.png)

<span data-ttu-id="1814e-115">La API se implementa como un conjunto de objetos del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="1814e-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="1814e-116">Mover TAPI al modelo COM orientado a objetos permite a los desarrolladores escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic o C/C++.</span><span class="sxs-lookup"><span data-stu-id="1814e-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="1814e-117">El uso de COM permite actualizar componentes de las características de TAPI.</span><span class="sxs-lookup"><span data-stu-id="1814e-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="1814e-118">El proceso de servidor TAPI (TAPISRV) abstrae la interfaz del proveedor de servicios TAPI (TSPI) de TAPI 3. x y TAPI 2. x, lo que permite usar los proveedores de servicios de telefonía TAPI 2. x con TAPI 3. x, manteniendo el estado interno de TAPI.</span><span class="sxs-lookup"><span data-stu-id="1814e-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="1814e-119">TAPISRV se implementa como un proceso de servicio en SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="1814e-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="1814e-120">Los [proveedores de servicios](./tapi-service-providers.md) comportan mecanismos de transporte multimedia específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1814e-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="1814e-121">Normalmente existen en pares: un proveedor de servicios de telefonía (TSP) para el control de llamadas y un proveedor de servicios multimedia (MSP) para el control multimedia.</span><span class="sxs-lookup"><span data-stu-id="1814e-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="1814e-122">Los [proveedores de servicios de telefonía](./telephony-service-providers-start-page.md) (profesionales) son responsables de resolver el modelo de llamadas independiente del Protocolo de TAPI en mecanismos de control de llamadas específicos del protocolo.</span><span class="sxs-lookup"><span data-stu-id="1814e-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="1814e-123">TAPI 3,1 proporciona compatibilidad con versiones anteriores de TAPI 2,1 profesionales.</span><span class="sxs-lookup"><span data-stu-id="1814e-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="1814e-124">Dos proveedores de servicios de telefonía IP (y sus MSP asociados) se distribuyen de forma predeterminada con TAPI 3,1: el TSP H. 323 y el TSP de conferencias de multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="1814e-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="1814e-125">Los [proveedores de servicios multimedia](media-service-providers-start-page.md) (MSP) proporcionan una forma uniforme de acceder a los flujos multimedia en una llamada, lo que admite la API de DirectShow<sup>TM</sup> como controlador de flujo de medios principal.</span><span class="sxs-lookup"><span data-stu-id="1814e-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="1814e-126">Los MSP de TAPI implementan interfaces de DirectShow para un TSP determinado y son necesarios para cualquier servicio de telefonía que haga uso de la transmisión por secuencias de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1814e-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="1814e-127">La aplicación controla las secuencias genéricas.</span><span class="sxs-lookup"><span data-stu-id="1814e-127">Generic streams are handled by the application.</span></span>

 

 
