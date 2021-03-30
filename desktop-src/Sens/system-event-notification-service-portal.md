---
description: Supervise las notificaciones de eventos del sistema de los programas que se ejecutan en equipos móviles para determinar el ancho de banda y la latencia de conexión de red. Escriba aplicaciones optimizadas para la informática móvil y LAN de alta latencia.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Servicio de notificación de eventos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002661"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="724bb-104">Servicio de notificación de eventos del sistema</span><span class="sxs-lookup"><span data-stu-id="724bb-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="724bb-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="724bb-105">Purpose</span></span>

<span data-ttu-id="724bb-106">Las aplicaciones diseñadas para su uso por parte de usuarios móviles requieren un conjunto único de funciones de conectividad y notificaciones.</span><span class="sxs-lookup"><span data-stu-id="724bb-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="724bb-107">En el pasado, las aplicaciones individuales eran necesarias para implementar estas características internamente.</span><span class="sxs-lookup"><span data-stu-id="724bb-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="724bb-108">El servicio de notificación de eventos del sistema (SENS) ahora proporciona estas funcionalidades en el sistema operativo, creando una interfaz de notificación y conectividad uniforme para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="724bb-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="724bb-109">El uso de los desarrolladores de SENS puede determinar el ancho de banda de conexión y la información de latencia dentro de su aplicación y optimizar el funcionamiento de la aplicación en función de esas condiciones.</span><span class="sxs-lookup"><span data-stu-id="724bb-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="724bb-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="724bb-110">Where applicable</span></span>

<span data-ttu-id="724bb-111">Las funciones de conectividad y las notificaciones de SENS son útiles para las aplicaciones escritas para equipos móviles o equipos conectados a redes de área local de latencia alta.</span><span class="sxs-lookup"><span data-stu-id="724bb-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="724bb-112">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="724bb-112">Developer audience</span></span>

<span data-ttu-id="724bb-113">Este documento está destinado a los desarrolladores de software que desarrollan aplicaciones para la informática móvil y redes de área local de latencia alta.</span><span class="sxs-lookup"><span data-stu-id="724bb-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="724bb-114">En este documento se proporciona una referencia completa de todas las partes del servicio de notificación de eventos del sistema, incluido el objeto SENS y los métodos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="724bb-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="724bb-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="724bb-115">Run-time requirements</span></span>

<span data-ttu-id="724bb-116">Requiere Microsoft Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="724bb-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="724bb-117">Para obtener información acerca de los sistemas operativos necesarios para usar una interfaz o función determinada, consulte la sección de requisitos de la documentación.</span><span class="sxs-lookup"><span data-stu-id="724bb-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="724bb-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="724bb-118">In this section</span></span>



| <span data-ttu-id="724bb-119">Tema</span><span class="sxs-lookup"><span data-stu-id="724bb-119">Topic</span></span>                                                              | <span data-ttu-id="724bb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="724bb-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="724bb-121">Información general</span><span class="sxs-lookup"><span data-stu-id="724bb-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="724bb-122">Información general sobre el servicio de notificación de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="724bb-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="724bb-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="724bb-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="724bb-124">Documentación de los métodos e interfaces del servicio de notificación de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="724bb-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="724bb-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="724bb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724bb-126">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="724bb-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
