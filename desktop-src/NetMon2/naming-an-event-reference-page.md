---
description: Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe asignarle el nombre antes de que Monitor de red pueda mostrarlo en el Visor de eventos.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Asignar un nombre a una página de referencia de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669996"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="f1420-103">Asignar un nombre a una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="f1420-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="f1420-104">Después de crear un documento HTML de origen de la página de referencia de eventos (ERP), debe asignarle el nombre antes de que Monitor de red pueda mostrarlo en el Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f1420-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="f1420-105">Monitor de nombres y archivos ERP expertos con este formato:</span><span class="sxs-lookup"><span data-stu-id="f1420-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="f1420-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span><span class="sxs-lookup"><span data-stu-id="f1420-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="f1420-107">Nombre de archivo DLL, sin incluir la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f1420-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="f1420-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="f1420-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="f1420-109">Identificador de evento del ERP experto.</span><span class="sxs-lookup"><span data-stu-id="f1420-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="f1420-110">El identificador de evento también se encuentra en el miembro **EventIdent** de la estructura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="f1420-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="f1420-111">Para obtener más información acerca de la creación de un ERP, consulte los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1420-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="f1420-112">Creación de páginas de referencia de eventos Expert y monitor</span><span class="sxs-lookup"><span data-stu-id="f1420-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="f1420-113">Escribir una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="f1420-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="f1420-114">Probar una página de referencia de eventos</span><span class="sxs-lookup"><span data-stu-id="f1420-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



