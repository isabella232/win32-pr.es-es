---
description: Modo de reproducción no representativo de VMR (asignador personalizado)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modo de reproducción no representativo de VMR (asignador personalizado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815246"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="e10c1-103">Modo de reproducción no representativo de VMR (asignador personalizado)</span><span class="sxs-lookup"><span data-stu-id="e10c1-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="e10c1-104">En el modo de reproducción sin representación, VMR no realiza la representación.</span><span class="sxs-lookup"><span data-stu-id="e10c1-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="e10c1-105">En su lugar, utiliza un asignador personalizado proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e10c1-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="e10c1-106">Este modo es útil para juegos y otros tipos de aplicaciones que tienen efectos de vídeo sofisticados.</span><span class="sxs-lookup"><span data-stu-id="e10c1-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="e10c1-107">El modo de reproducción sin representación permite que las aplicaciones creen y controlen su propia superficie de DirectDraw (VMR-7) o la superficie de Direct3D (VMR-9), y para tener acceso a los bits de vídeo en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="e10c1-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="e10c1-108">En el modo sin procesar, VMR-9 no carga automáticamente su componente de mezclador.</span><span class="sxs-lookup"><span data-stu-id="e10c1-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="e10c1-109">En el modo de reproducción sin procesar, la aplicación realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="e10c1-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="e10c1-110">Administra la ventana de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e10c1-110">Manages the playback window.</span></span>
-   <span data-ttu-id="e10c1-111">Asigna el objeto DirectDraw o Direct3D y el búfer de fotogramas final.</span><span class="sxs-lookup"><span data-stu-id="e10c1-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="e10c1-112">Notifica al resto del sistema de reproducción del objeto que se está usando.</span><span class="sxs-lookup"><span data-stu-id="e10c1-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="e10c1-113">Presenta el búfer de fotogramas en el momento correcto.</span><span class="sxs-lookup"><span data-stu-id="e10c1-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="e10c1-114">Controla todos los cambios en el modo de resolución, supervisa los cambios y las pérdidas superficiales.</span><span class="sxs-lookup"><span data-stu-id="e10c1-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="e10c1-115">Debe informar al resto del sistema de reproducción de estos eventos.</span><span class="sxs-lookup"><span data-stu-id="e10c1-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="e10c1-116">La VMR hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e10c1-116">The VMR does the following:</span></span>

-   <span data-ttu-id="e10c1-117">Controla todo el control de tiempo relacionado con la presentación del fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e10c1-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="e10c1-118">Proporciona información de control de calidad a la aplicación y al resto del sistema de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e10c1-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="e10c1-119">Presenta una interfaz coherente con los componentes de nivel superior del sistema de reproducción, que no son conscientes de que la aplicación proporciona la asignación de búfer de fotogramas y realiza la representación.</span><span class="sxs-lookup"><span data-stu-id="e10c1-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="e10c1-120">Proporciona cualquier combinación de secuencias de vídeo que puede ser necesaria antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="e10c1-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="e10c1-121">Dado que el mezclador realiza el desentrelazado, el asignador-presentador siempre recibe fotogramas desentrelazados.</span><span class="sxs-lookup"><span data-stu-id="e10c1-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="e10c1-122">Para obtener más información, consulte [configuración de preferencias de desentrelazado](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="e10c1-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="e10c1-123">Para obtener más información acerca de cómo proporcionar un asignador personalizado, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e10c1-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="e10c1-124">Proporcionar un Allocator-Presenter personalizado para VMR-7</span><span class="sxs-lookup"><span data-stu-id="e10c1-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="e10c1-125">Suministro de un Allocator-Presenter personalizado para VMR-9</span><span class="sxs-lookup"><span data-stu-id="e10c1-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="e10c1-126">Sincronizar la VMR con la frecuencia de actualización del monitor</span><span class="sxs-lookup"><span data-stu-id="e10c1-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



