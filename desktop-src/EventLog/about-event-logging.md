---
description: Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar la causa del error, intentar recuperar los datos perdidos y evitar que el error se repita.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Acerca del registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082233"
---
# <a name="about-event-logging"></a><span data-ttu-id="ab5c8-103">Acerca del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="ab5c8-103">About Event Logging</span></span>

<span data-ttu-id="ab5c8-104">Cuando se produce un error, el administrador del sistema o el representante de soporte técnico deben determinar la causa del error, intentar recuperar los datos perdidos y evitar que el error se repita.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="ab5c8-105">Resulta útil si las aplicaciones, el sistema operativo y otros servicios del sistema registran eventos importantes, como condiciones de memoria insuficiente o intentos excesivos de obtener acceso a un disco.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="ab5c8-106">A continuación, el administrador del sistema puede utilizar el registro de eventos para determinar qué condiciones produjeron el error e identificar el contexto en el que se produjo.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="ab5c8-107">Al ver periódicamente el registro de eventos, es posible que el administrador del sistema pueda identificar problemas (por ejemplo, un disco duro con errores) antes de que causen daños.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="ab5c8-108">La API de registro de eventos se diseñó para aplicaciones que se ejecutan en el sistema operativo Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="ab5c8-109">En Windows Vista, se ha rediseñado la infraestructura de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="ab5c8-110">Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores ahora deben usar el [registro de eventos de Windows](/windows/desktop/WES/windows-event-log) para registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="ab5c8-111">En esta sección se describe la interfaz de programación para escribir y consumir eventos mediante el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="ab5c8-112">Tipos de evento</span><span class="sxs-lookup"><span data-stu-id="ab5c8-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="ab5c8-113">Instrucciones de registro</span><span class="sxs-lookup"><span data-stu-id="ab5c8-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="ab5c8-114">Elementos de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="ab5c8-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="ab5c8-115">Operaciones de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="ab5c8-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="ab5c8-116">Modelo de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="ab5c8-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="ab5c8-117">Seguridad del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="ab5c8-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="ab5c8-118">Las aplicaciones que publican eventos de más de 64 kilobytes en un equipo con Windows Server 2003, Windows XP o Windows 2000 no podrán publicar eventos en un equipo con Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="ab5c8-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
