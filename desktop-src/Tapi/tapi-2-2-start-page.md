---
description: La versión 2,2 (TAPI/C) de la interfaz de programación de aplicaciones de telefonía (TAPI) de Microsoft admite la implementación de aplicaciones de comunicaciones que abarcan desde el control básico de módem hasta centros de llamadas con varios agentes y conmutadores.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Interfaz de programación de aplicaciones de telefonía versión 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277136"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="3fbef-103">Interfaz de programación de aplicaciones de telefonía versión 2,2</span><span class="sxs-lookup"><span data-stu-id="3fbef-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="3fbef-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="3fbef-104">Purpose</span></span>

<span data-ttu-id="3fbef-105">La versión 2,2 (TAPI/C) de la interfaz de programación de aplicaciones de telefonía (TAPI) de Microsoft admite la implementación de aplicaciones de comunicaciones que abarcan desde el control básico de módem hasta centros de llamadas con varios agentes y conmutadores.</span><span class="sxs-lookup"><span data-stu-id="3fbef-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3fbef-106">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="3fbef-106">Where applicable</span></span>

<span data-ttu-id="3fbef-107">Las posibles aplicaciones TAPI 2,2 incluyen:</span><span class="sxs-lookup"><span data-stu-id="3fbef-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="3fbef-108">Llamadas de voz básicas en la red telefónica conmutada (RTC) pública</span><span class="sxs-lookup"><span data-stu-id="3fbef-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="3fbef-109">Aplicaciones del centro de llamadas para realizar un seguimiento de varios agentes</span><span class="sxs-lookup"><span data-stu-id="3fbef-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="3fbef-110">Control de módem</span><span class="sxs-lookup"><span data-stu-id="3fbef-110">Modem control</span></span>
-   <span data-ttu-id="3fbef-111">Control de PBX</span><span class="sxs-lookup"><span data-stu-id="3fbef-111">PBX control</span></span>
-   <span data-ttu-id="3fbef-112">Sistemas de respuesta interactiva de voz (IVR)</span><span class="sxs-lookup"><span data-stu-id="3fbef-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="3fbef-113">Buzón de voz</span><span class="sxs-lookup"><span data-stu-id="3fbef-113">Voice mail</span></span>
-   <span data-ttu-id="3fbef-114">Control de dispositivo de teléfono detallado</span><span class="sxs-lookup"><span data-stu-id="3fbef-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3fbef-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="3fbef-115">Developer audience</span></span>

<span data-ttu-id="3fbef-116">TAPI/C está diseñado para que lo usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="3fbef-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="3fbef-117">La experiencia de desarrollo con las telecomunicaciones y otras aplicaciones de telefonía es útil, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="3fbef-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3fbef-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="3fbef-118">Run-time requirements</span></span>

<span data-ttu-id="3fbef-119">La versión 2,2 de TAPI permite el desarrollo de aplicaciones de comunicaciones para los sistemas operativos Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98 y Windows 95.</span><span class="sxs-lookup"><span data-stu-id="3fbef-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="3fbef-120">Para obtener más información acerca de los sistemas operativos que admiten una función determinada, consulte la sección de requisitos de la documentación de esa función.</span><span class="sxs-lookup"><span data-stu-id="3fbef-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3fbef-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3fbef-121">In this section</span></span>



| <span data-ttu-id="3fbef-122">Tema</span><span class="sxs-lookup"><span data-stu-id="3fbef-122">Topic</span></span>                                          | <span data-ttu-id="3fbef-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fbef-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fbef-124">Información general</span><span class="sxs-lookup"><span data-stu-id="3fbef-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="3fbef-125">Información general acerca de la arquitectura y los componentes de TAPI.</span><span class="sxs-lookup"><span data-stu-id="3fbef-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="3fbef-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="3fbef-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="3fbef-127">Documentación de funciones, estructuras, mensajes, constantes y clases de dispositivos disponibles en TAPI 2,2.</span><span class="sxs-lookup"><span data-stu-id="3fbef-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3fbef-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fbef-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fbef-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3fbef-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="3fbef-130">Proveedores de servicios TAPI</span><span class="sxs-lookup"><span data-stu-id="3fbef-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

