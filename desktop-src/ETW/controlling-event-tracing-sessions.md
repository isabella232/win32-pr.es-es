---
description: Las sesiones de seguimiento de eventos registran eventos de uno o más proveedores.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controlar sesiones de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984519"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="b02d9-103">Controlar sesiones de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="b02d9-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="b02d9-104">Las sesiones de seguimiento de eventos registran eventos de uno o más [proveedores](providing-events.md).</span><span class="sxs-lookup"><span data-stu-id="b02d9-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="b02d9-105">El controlador define la sesión y habilita los proveedores.</span><span class="sxs-lookup"><span data-stu-id="b02d9-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="b02d9-106">La definición de la sesión suele incluir la especificación de la sesión y el nombre del archivo de registro, el tipo de archivo de registro que se va a usar y la resolución de la marca de tiempo utilizada para registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="b02d9-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="b02d9-107">Los controladores también pueden actualizar y consultar sesiones de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b02d9-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="b02d9-108">En los temas siguientes se muestra cómo definir y actualizar una sesión y habilitar los proveedores de seguimiento de eventos:</span><span class="sxs-lookup"><span data-stu-id="b02d9-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="b02d9-109">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="b02d9-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="b02d9-110">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="b02d9-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="b02d9-111">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="b02d9-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="b02d9-112">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="b02d9-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="b02d9-113">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="b02d9-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="b02d9-114">Recuperación de datos de seguimiento de eventos adicionales</span><span class="sxs-lookup"><span data-stu-id="b02d9-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="b02d9-115">Para obtener información sobre cómo vaciar y consultar sesiones, vea [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) y [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b02d9-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="b02d9-116">Solo los usuarios que ejecutan con privilegios administrativos elevados, los usuarios del grupo usuarios del registro de rendimiento y las aplicaciones que se ejecutan como LocalSystem, LocalService o NetworkService pueden controlar las sesiones de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b02d9-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="b02d9-117">Para conceder a un usuario restringido la capacidad de controlar las sesiones de seguimiento, agréguelas al grupo usuarios del registro de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b02d9-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="b02d9-118">**Windows XP y windows 2000:** Cualquier persona puede controlar una sesión de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="b02d9-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
