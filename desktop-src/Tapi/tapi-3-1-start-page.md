---
description: La interfaz de programación de aplicaciones de telefonía (TAPI) versión 3,1 de Microsoft es una API basada en el modelo de objetos componentes (COM) que combina la telefonía clásica y la IP.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Interfaz de programación de aplicaciones de telefonía versión 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678202"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="6719c-103">Interfaz de programación de aplicaciones de telefonía versión 3,1</span><span class="sxs-lookup"><span data-stu-id="6719c-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="6719c-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="6719c-104">Purpose</span></span>

<span data-ttu-id="6719c-105">La interfaz de programación de aplicaciones de telefonía (TAPI) versión 3,1 de Microsoft es una API basada en el modelo de objetos componentes (COM) que combina la telefonía clásica y la IP.</span><span class="sxs-lookup"><span data-stu-id="6719c-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6719c-106">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="6719c-106">Where applicable</span></span>

<span data-ttu-id="6719c-107">Las posibles aplicaciones TAPI incluyen:</span><span class="sxs-lookup"><span data-stu-id="6719c-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="6719c-108">Conferencias IP Multimedia multidifusión con calidad de servicio (QOS)</span><span class="sxs-lookup"><span data-stu-id="6719c-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="6719c-109">Llamadas de voz a través de Internet mediante el protocolo H. 323</span><span class="sxs-lookup"><span data-stu-id="6719c-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="6719c-110">Aplicaciones del centro de llamadas capaces de realizar un seguimiento de varios agentes</span><span class="sxs-lookup"><span data-stu-id="6719c-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="6719c-111">Llamadas de voz básicas en la red telefónica conmutada (RTC) pública</span><span class="sxs-lookup"><span data-stu-id="6719c-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="6719c-112">Control de PBX</span><span class="sxs-lookup"><span data-stu-id="6719c-112">PBX control</span></span>
-   <span data-ttu-id="6719c-113">Sistemas de respuesta interactiva de voz (IVR)</span><span class="sxs-lookup"><span data-stu-id="6719c-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="6719c-114">Buzón de voz</span><span class="sxs-lookup"><span data-stu-id="6719c-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6719c-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="6719c-115">Developer audience</span></span>

<span data-ttu-id="6719c-116">Puede escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic y C/C++.</span><span class="sxs-lookup"><span data-stu-id="6719c-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="6719c-117">Es necesario estar familiarizado con COM.</span><span class="sxs-lookup"><span data-stu-id="6719c-117">Familiarity with COM is required.</span></span> <span data-ttu-id="6719c-118">La experiencia de desarrollo con las telecomunicaciones y otras aplicaciones de telefonía es útil, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="6719c-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6719c-119">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="6719c-119">Run-time requirements</span></span>

<span data-ttu-id="6719c-120">La versión 3,1 de TAPI permite el desarrollo de aplicaciones de comunicaciones para los sistemas operativos Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6719c-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6719c-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6719c-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="6719c-122">Tema</span><span class="sxs-lookup"><span data-stu-id="6719c-122">Topic</span></span></th><th><span data-ttu-id="6719c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6719c-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="6719c-124"><a href="tapi-3-1-overview.md">Información general</a></span><span class="sxs-lookup"><span data-stu-id="6719c-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="6719c-125">Información general acerca de la arquitectura y los componentes de TAPI.</span><span class="sxs-lookup"><span data-stu-id="6719c-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="6719c-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="6719c-126">Reference</span></span><br/></td><td><span data-ttu-id="6719c-127">Documentación de:</span><span class="sxs-lookup"><span data-stu-id="6719c-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="6719c-128"><a href="call-and-media-controls-reference.md">Referencia de controles de llamada y multimedia</a></span><span class="sxs-lookup"><span data-stu-id="6719c-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="6719c-129"><a href="call-center-controls-reference.md">Referencia de controles del centro de llamadas</a></span><span class="sxs-lookup"><span data-stu-id="6719c-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="6719c-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Referencia de Rendezvous</a></span><span class="sxs-lookup"><span data-stu-id="6719c-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="6719c-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6719c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6719c-132">Introducción a la telefonía de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6719c-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="6719c-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6719c-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="6719c-134">Proveedores de servicios TAPI</span><span class="sxs-lookup"><span data-stu-id="6719c-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

