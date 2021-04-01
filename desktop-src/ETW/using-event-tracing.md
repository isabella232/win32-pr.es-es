---
description: En los temas siguientes se describe cómo usar la API ETW para el seguimiento de eventos.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Usar el seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275671"
---
# <a name="using-event-tracing"></a><span data-ttu-id="39103-103">Usar el seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="39103-103">Using Event Tracing</span></span>

<span data-ttu-id="39103-104">En los temas siguientes se describe cómo usar la API ETW para el seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="39103-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="39103-105">Tema</span><span class="sxs-lookup"><span data-stu-id="39103-105">Topic</span></span>                                                                          | <span data-ttu-id="39103-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="39103-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39103-107">Controlar sesiones de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="39103-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="39103-108">Describe cómo administrar sesiones de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="39103-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="39103-109">Proporcionar eventos</span><span class="sxs-lookup"><span data-stu-id="39103-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="39103-110">Describe cómo registrar y instrumentar un proveedor de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="39103-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="39103-111">Consumir eventos</span><span class="sxs-lookup"><span data-stu-id="39103-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="39103-112">Describe cómo implementar funciones de devolución de llamada utilizadas para consumir y procesar eventos de un archivo de registro de seguimiento o en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="39103-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="39103-113">Preprocesador de seguimiento de software de Windows</span><span class="sxs-lookup"><span data-stu-id="39103-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="39103-114">Proporciona un mecanismo eficaz para registrar y consumir eventos que se producen durante la ejecución de una aplicación o un controlador.</span><span class="sxs-lookup"><span data-stu-id="39103-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="39103-115">Incluya el archivo de encabezado Wmistr. h antes de incluir el archivo de encabezado Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="39103-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



