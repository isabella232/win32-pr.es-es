---
description: Muchas aplicaciones registran errores y eventos en registros de errores patentados, cada uno con su propio formato e interfaz de usuario.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Registro de eventos (registro de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688296"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="89343-103">Registro de eventos (registro de eventos)</span><span class="sxs-lookup"><span data-stu-id="89343-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="89343-104">Muchas aplicaciones registran errores y eventos en registros de errores patentados, cada uno con su propio formato e interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="89343-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="89343-105">Los datos de aplicaciones diferentes no se pueden combinar fácilmente en un informe completo, lo que requiere que los administradores del sistema o los representantes de soporte técnico comprueben diversos orígenes para diagnosticar problemas.</span><span class="sxs-lookup"><span data-stu-id="89343-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="89343-106">El registro de eventos proporciona una manera centralizada y estándar para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware.</span><span class="sxs-lookup"><span data-stu-id="89343-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="89343-107">El servicio registro de eventos registra eventos de varios orígenes y los almacena en una sola colección denominada *registro de eventos*.</span><span class="sxs-lookup"><span data-stu-id="89343-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="89343-108">El Visor de eventos permite ver registros; la interfaz de programación también permite examinar los registros.</span><span class="sxs-lookup"><span data-stu-id="89343-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="89343-109">Acerca del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="89343-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="89343-110">Uso del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="89343-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="89343-111">Referencia del registro de eventos</span><span class="sxs-lookup"><span data-stu-id="89343-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="89343-112">La API de registro de eventos se diseñó para aplicaciones que se ejecutan en el sistema operativo Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="89343-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="89343-113">En Windows Vista, se ha rediseñado la infraestructura de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="89343-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="89343-114">Las aplicaciones diseñadas para ejecutarse en Windows Vista o sistemas operativos posteriores deben usar el [registro de eventos de Windows](/windows/desktop/WES/windows-event-log) para registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="89343-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
