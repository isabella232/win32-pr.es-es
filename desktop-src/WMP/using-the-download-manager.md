---
title: Uso del administrador de descargas
description: Uso del administrador de descargas
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419153"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="1c6ea-109">Uso del administrador de descargas</span><span class="sxs-lookup"><span data-stu-id="1c6ea-109">Using the Download Manager</span></span>

<span data-ttu-id="1c6ea-110">El SDK de Windows Media Player incluye una página web de ejemplo que muestra cómo usar el administrador de descargas para descargar archivos en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="1c6ea-111">Puede encontrar el ejemplo en la carpeta denominada página web en la que instaló el SDK.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="1c6ea-112">El nombre del archivo es sample. asp.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="1c6ea-113">El ejemplo proporciona la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="1c6ea-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="1c6ea-114">Crea el objeto **Downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="1c6ea-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="1c6ea-115">Crea un objeto **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="1c6ea-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="1c6ea-116">Comienza a descargar cinco archivos cuando el usuario hace clic en **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="1c6ea-117">En el ejemplo se proporcionan rutas de acceso de archivo predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="1c6ea-118">Debe reemplazar estas rutas de acceso predeterminadas por las ubicaciones de los archivos de su propio servidor.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="1c6ea-119">Puede cambiar las rutas de acceso cambiando los valores asignados a la matriz global denominada g \_ sFiles.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="1c6ea-120">Muestra información de estado de una descarga cuando el usuario la selecciona.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="1c6ea-121">Proporciona controles para pausar, reanudar, cancelar y quitar un elemento de descarga.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="1c6ea-122">Mantiene información acerca de las colecciones de descarga entre sesiones mediante cookies.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="1c6ea-123">Esto es importante porque el usuario puede cerrar el reproductor en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="1c6ea-124">Además, si el usuario cambia los paneles de tareas en el reproductor, finaliza la sesión de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="1c6ea-125">Usa la descarga en tiempo real de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="1c6ea-126">Puede cambiar el comportamiento a la descarga en segundo plano cambiando el valor de la variable denominada g \_ sDLType.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="1c6ea-127">La descarga en segundo plano está disponible para su uso con el sistema operativo Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="1c6ea-128">Sincroniza el color de fondo con el color del reproductor.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="1c6ea-129">Puede usar esta característica para que la tienda en línea cambie de apariencia cuando el usuario decida cambiar el color del reproductor.</span><span class="sxs-lookup"><span data-stu-id="1c6ea-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="1c6ea-130">En las secciones siguientes se proporciona más información:</span><span class="sxs-lookup"><span data-stu-id="1c6ea-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="1c6ea-131">Inicialización de la página</span><span class="sxs-lookup"><span data-stu-id="1c6ea-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="1c6ea-132">Iniciar las descargas</span><span class="sxs-lookup"><span data-stu-id="1c6ea-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="1c6ea-133">Recuperando información de estado</span><span class="sxs-lookup"><span data-stu-id="1c6ea-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="1c6ea-134">Mantenimiento de la información de sesión</span><span class="sxs-lookup"><span data-stu-id="1c6ea-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="1c6ea-135">Depurar la página</span><span class="sxs-lookup"><span data-stu-id="1c6ea-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="1c6ea-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c6ea-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6ea-137">**Guía de programación para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="1c6ea-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




