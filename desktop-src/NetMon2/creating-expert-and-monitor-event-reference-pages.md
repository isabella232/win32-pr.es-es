---
description: En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (O ERP e) y cómo implementarlas en un experto o en un monitor. Para obtener información sobre O ERP e y cómo usarlos con Monitor de red, consulte la página de referencia de eventos.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Creación de páginas de referencia de eventos Expert y monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652659"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="7cac9-104">Creación de páginas de referencia de eventos Expert y monitor</span><span class="sxs-lookup"><span data-stu-id="7cac9-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="7cac9-105">En esta sección se describe cómo planear, desarrollar y probar páginas de referencia de eventos (O ERP e) y cómo implementarlas en un experto o en un monitor.</span><span class="sxs-lookup"><span data-stu-id="7cac9-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="7cac9-106">Para obtener información sobre O ERP e y cómo usarlos con Monitor de red, consulte la [Página de referencia de eventos](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="7cac9-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="7cac9-107">Para desarrollar un nuevo ERP, el primer paso consiste en determinar los eventos que requieren O ERP e individuales para el [experto](experts.md) o el [monitor](monitors.md)personalizado.</span><span class="sxs-lookup"><span data-stu-id="7cac9-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="7cac9-108">Debe crear O ERP e independientes para cada evento que desee mostrar en el Visor de eventos de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="7cac9-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="7cac9-109">Por ejemplo, supongamos que:</span><span class="sxs-lookup"><span data-stu-id="7cac9-109">For example, suppose that:</span></span>

-   <span data-ttu-id="7cac9-110">Desarrolla un monitor denominado monitor de juegos y supervisor de existencias.</span><span class="sxs-lookup"><span data-stu-id="7cac9-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="7cac9-111">El monitor se encuentra en un archivo denominado Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="7cac9-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="7cac9-112">El monitor genera dos eventos, juegos en ejecución y mis acciones de Internet.</span><span class="sxs-lookup"><span data-stu-id="7cac9-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="7cac9-113">Planea desarrollar dos O ERP e, Gamemon1.htm y Gamemon2.htm.</span><span class="sxs-lookup"><span data-stu-id="7cac9-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="7cac9-114">No es necesario tener una correspondencia uno a uno de O ERP e para supervisar o realizar eventos expertos.</span><span class="sxs-lookup"><span data-stu-id="7cac9-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="7cac9-115">Una vez que haya establecido una lista de O ERP e únicos, siga estos pasos para crear cada ERP.</span><span class="sxs-lookup"><span data-stu-id="7cac9-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="7cac9-116">[Escriba el documento de origen HTML](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="7cac9-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="7cac9-117">Guarde el archivo de código fuente HTML [y asígnele un nombre](naming-an-event-reference-page.md) como archivo. htm.</span><span class="sxs-lookup"><span data-stu-id="7cac9-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="7cac9-118">[Pruebe el ERP](testing-an-event-reference-page.md) con el experto o el monitor completado.</span><span class="sxs-lookup"><span data-stu-id="7cac9-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



