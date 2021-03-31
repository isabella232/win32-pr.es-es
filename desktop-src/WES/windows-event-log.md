---
title: Registro de errores de Windows
description: La API del registro de eventos de Windows define el esquema que se utiliza para escribir un manifiesto de instrumentación.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904811"
---
# <a name="windows-event-log"></a><span data-ttu-id="9e03f-103">Registro de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="9e03f-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="9e03f-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="9e03f-104">Purpose</span></span>

<span data-ttu-id="9e03f-105">La API del registro de eventos de Windows define el esquema que se utiliza para escribir un manifiesto de instrumentación.</span><span class="sxs-lookup"><span data-stu-id="9e03f-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="9e03f-106">Un manifiesto de instrumentación identifica el proveedor de eventos y los eventos que registra.</span><span class="sxs-lookup"><span data-stu-id="9e03f-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="9e03f-107">La API también incluye las funciones que un consumidor de eventos, como el [visor de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), usaría para leer y representar los eventos.</span><span class="sxs-lookup"><span data-stu-id="9e03f-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="9e03f-108">Para escribir los eventos definidos en el manifiesto, use las funciones incluidas en la API de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="9e03f-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="9e03f-109">El registro de eventos de Windows sustituye a la API de [registro de eventos](/windows/desktop/EventLog/event-logging) a partir del sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e03f-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9e03f-110">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="9e03f-110">Developer audience</span></span>

<span data-ttu-id="9e03f-111">El registro de eventos de Windows está diseñado para programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="9e03f-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9e03f-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="9e03f-112">Run-time requirements</span></span>

<span data-ttu-id="9e03f-113">El registro de eventos de Windows se incluye en el sistema operativo a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9e03f-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="9e03f-114">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="9e03f-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="9e03f-115">Para ver el historial de versiones completo, vea [novedades](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="9e03f-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e03f-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9e03f-116">In this section</span></span>


| <span data-ttu-id="9e03f-117">Tema</span><span class="sxs-lookup"><span data-stu-id="9e03f-117">Topic</span></span>                                                        | <span data-ttu-id="9e03f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e03f-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e03f-119">Uso del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="9e03f-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="9e03f-120">Guía de procedimientos que muestra cómo usar la API del registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e03f-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="9e03f-121">Referencia del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="9e03f-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="9e03f-122">Los tipos de datos, las funciones, las enumeraciones, las estructuras, las constantes y los esquemas que incluye la API.</span><span class="sxs-lookup"><span data-stu-id="9e03f-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|