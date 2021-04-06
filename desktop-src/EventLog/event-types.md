---
description: Hay cinco tipos de eventos que se pueden registrar. Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908862"
---
# <a name="event-types"></a><span data-ttu-id="c96a0-104">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="c96a0-104">Event Types</span></span>

<span data-ttu-id="c96a0-105">Hay cinco tipos de eventos que se pueden registrar.</span><span class="sxs-lookup"><span data-stu-id="c96a0-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="c96a0-106">Todos ellos tienen datos comunes bien definidos y, opcionalmente, pueden incluir datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="c96a0-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="c96a0-107">La aplicación indica el tipo de evento cuando informa de un evento.</span><span class="sxs-lookup"><span data-stu-id="c96a0-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="c96a0-108">Cada evento debe ser de un tipo único.</span><span class="sxs-lookup"><span data-stu-id="c96a0-108">Each event must be of a single type.</span></span> <span data-ttu-id="c96a0-109">En el Visor de eventos se muestra un icono diferente para cada tipo en la vista de lista del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="c96a0-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="c96a0-110">En la tabla siguiente se describen los cinco tipos de eventos que se usan en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="c96a0-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="c96a0-111">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="c96a0-111">Event type</span></span>        | <span data-ttu-id="c96a0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c96a0-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96a0-113">**Error**</span><span class="sxs-lookup"><span data-stu-id="c96a0-113">**Error**</span></span>         | <span data-ttu-id="c96a0-114">Evento que indica un problema importante, como la pérdida de datos o la pérdida de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="c96a0-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="c96a0-115">Por ejemplo, si un servicio no se carga durante el inicio, se registra un evento de error.</span><span class="sxs-lookup"><span data-stu-id="c96a0-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="c96a0-116">**Warning (ADVERTENCIA)**</span><span class="sxs-lookup"><span data-stu-id="c96a0-116">**Warning**</span></span>       | <span data-ttu-id="c96a0-117">Un evento que no es necesariamente significativo, pero puede indicar un posible problema futuro.</span><span class="sxs-lookup"><span data-stu-id="c96a0-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="c96a0-118">Por ejemplo, si el espacio en disco es bajo, se registra un evento de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c96a0-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="c96a0-119">Si una aplicación puede recuperarse de un evento sin pérdida de funcionalidad o datos, generalmente puede clasificar el evento como un evento de advertencia.</span><span class="sxs-lookup"><span data-stu-id="c96a0-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="c96a0-120">**Información**</span><span class="sxs-lookup"><span data-stu-id="c96a0-120">**Information**</span></span>   | <span data-ttu-id="c96a0-121">Evento que describe el funcionamiento correcto de una aplicación, un controlador o un servicio.</span><span class="sxs-lookup"><span data-stu-id="c96a0-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="c96a0-122">Por ejemplo, cuando un controlador de red se carga correctamente, puede ser adecuado registrar un evento de información.</span><span class="sxs-lookup"><span data-stu-id="c96a0-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="c96a0-123">Tenga en cuenta que, por lo general, no es apropiado que una aplicación de escritorio registre un evento cada vez que se inicie.</span><span class="sxs-lookup"><span data-stu-id="c96a0-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="c96a0-124">**Auditoría de aciertos**</span><span class="sxs-lookup"><span data-stu-id="c96a0-124">**Success Audit**</span></span> | <span data-ttu-id="c96a0-125">Evento que registra un intento de acceso de seguridad auditado que se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c96a0-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="c96a0-126">Por ejemplo, el intento de inicio de sesión correcto de un usuario en el sistema se registra como un evento de auditoría correcta.</span><span class="sxs-lookup"><span data-stu-id="c96a0-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="c96a0-127">**Auditoría de errores**</span><span class="sxs-lookup"><span data-stu-id="c96a0-127">**Failure Audit**</span></span> | <span data-ttu-id="c96a0-128">Evento que registra un intento de acceso de seguridad auditado que produce un error.</span><span class="sxs-lookup"><span data-stu-id="c96a0-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="c96a0-129">Por ejemplo, si un usuario intenta obtener acceso a una unidad de red y se produce un error, el intento se registra como un evento de auditoría de errores.</span><span class="sxs-lookup"><span data-stu-id="c96a0-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="c96a0-130">Se puede realizar un seguimiento de las actividades seleccionadas de los usuarios mediante la auditoría de eventos de seguridad y la colocación de entradas en el registro de seguridad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="c96a0-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



