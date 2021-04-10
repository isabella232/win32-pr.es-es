---
description: El SDK de Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos. Sin embargo, también puede usar las herramientas existentes, incluido un editor de cuadros de diálogo.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programar un experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156308"
---
# <a name="programming-an-expert"></a><span data-ttu-id="562c8-104">Programar un experto</span><span class="sxs-lookup"><span data-stu-id="562c8-104">Programming an Expert</span></span>

<span data-ttu-id="562c8-105">El SDK de Monitor de red incluye las funciones y el código de ejemplo que necesita para crear expertos.</span><span class="sxs-lookup"><span data-stu-id="562c8-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="562c8-106">Sin embargo, también puede usar las herramientas existentes, incluido un editor de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="562c8-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="562c8-107">Requisitos mínimos para ejecutar un experto</span><span class="sxs-lookup"><span data-stu-id="562c8-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="562c8-108">En la tabla siguiente se enumeran los puntos de entrada de DLL y las funciones de experto que debe usar para crear un experto.</span><span class="sxs-lookup"><span data-stu-id="562c8-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="562c8-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="562c8-109">Name</span></span>                                                 | <span data-ttu-id="562c8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="562c8-110">Type</span></span>               | <span data-ttu-id="562c8-111">¿Necesario?</span><span class="sxs-lookup"><span data-stu-id="562c8-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="562c8-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="562c8-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="562c8-113">Función de entrada DLL</span><span class="sxs-lookup"><span data-stu-id="562c8-113">DLL entry function</span></span> | <span data-ttu-id="562c8-114">Sí</span><span class="sxs-lookup"><span data-stu-id="562c8-114">Yes</span></span>                                             |
| [<span data-ttu-id="562c8-115">**Registrar experto**</span><span class="sxs-lookup"><span data-stu-id="562c8-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="562c8-116">Función de entrada DLL</span><span class="sxs-lookup"><span data-stu-id="562c8-116">DLL entry function</span></span> | <span data-ttu-id="562c8-117">Sí</span><span class="sxs-lookup"><span data-stu-id="562c8-117">Yes</span></span>                                             |
| [<span data-ttu-id="562c8-118">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="562c8-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="562c8-119">Función de entrada DLL</span><span class="sxs-lookup"><span data-stu-id="562c8-119">DLL entry function</span></span> | <span data-ttu-id="562c8-120">Sí</span><span class="sxs-lookup"><span data-stu-id="562c8-120">Yes</span></span>                                             |
| [<span data-ttu-id="562c8-121">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="562c8-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="562c8-122">Función de entrada DLL</span><span class="sxs-lookup"><span data-stu-id="562c8-122">DLL entry function</span></span> | <span data-ttu-id="562c8-123">Solo si el experto proporciona la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="562c8-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="562c8-124">**ExpertIndicateStatus**</span><span class="sxs-lookup"><span data-stu-id="562c8-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="562c8-125">Función experta</span><span class="sxs-lookup"><span data-stu-id="562c8-125">Expert function</span></span>    | <span data-ttu-id="562c8-126">Sí</span><span class="sxs-lookup"><span data-stu-id="562c8-126">Yes</span></span>                                             |
| [<span data-ttu-id="562c8-127">**ExpertSubmitEvent**</span><span class="sxs-lookup"><span data-stu-id="562c8-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="562c8-128">Función experta</span><span class="sxs-lookup"><span data-stu-id="562c8-128">Expert function</span></span>    | <span data-ttu-id="562c8-129">Sí</span><span class="sxs-lookup"><span data-stu-id="562c8-129">Yes</span></span>                                             |



 

<span data-ttu-id="562c8-130">Revise los temas de referencia de expertos y del analizador en el Monitor de red SDK para actualizar el código fuente y, a continuación, use el código de ejemplo y los procedimientos proporcionados en estos temas:</span><span class="sxs-lookup"><span data-stu-id="562c8-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="562c8-131">Creación de un experto</span><span class="sxs-lookup"><span data-stu-id="562c8-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="562c8-132">Instalación de un experto</span><span class="sxs-lookup"><span data-stu-id="562c8-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="562c8-133">Depuración de un experto</span><span class="sxs-lookup"><span data-stu-id="562c8-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="562c8-134">Los archivos dll expertos requieren la Convención de llamada C, no la de C++, porque las funciones se llaman a través de punteros de función mediante una superposición.</span><span class="sxs-lookup"><span data-stu-id="562c8-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="562c8-135">A través de un conjunto de funciones expertas especializadas, el experto tiene acceso a los fotogramas de la captura.</span><span class="sxs-lookup"><span data-stu-id="562c8-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="562c8-136">El experto puede usar la mayoría de las API de Monitor de red para manipular los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="562c8-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="562c8-137">Cuando un experto encuentra información para enviar al usuario, empaqueta la información en una estructura de datos de eventos y la envía a Monitor de red, que muestra la información en una ventana de salida experta.</span><span class="sxs-lookup"><span data-stu-id="562c8-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="562c8-138">El experto debe actualizar periódicamente Monitor de red con información de estado de finalización de porcentaje, proporcionada por la función [**ExpertIndicateStatus**](expertindicatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="562c8-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="562c8-139">A las funciones exportadas del experto se les llama de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="562c8-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="562c8-140">Cuando Monitor de red está creando la lista de expertos que va a presentar al usuario, Monitor de red llama a la función [**registrar experto**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="562c8-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="562c8-141">Después de la llamada a **Register**, si el experto es configurable, monitor de red llama a la función [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="562c8-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="562c8-142">Cuando el usuario Monitor de red hace clic en **Ejecutar experto**, monitor de red llama a la función [**Ejecutar**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="562c8-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="562c8-143">Cuando los expertos analizan los fotogramas solicitados y encuentran un problema, usan [**ExpertSubmitEvent**](expertsubmitevent.md) para enviar un evento que contiene información sobre el problema.</span><span class="sxs-lookup"><span data-stu-id="562c8-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="562c8-144">Monitor de red distribuye el evento al Visor de eventos estándar (compartido) o (si el experto lo registra) en una Visor de eventos privada.</span><span class="sxs-lookup"><span data-stu-id="562c8-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



