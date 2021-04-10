---
title: Inicialización de la página
description: Inicialización de la página
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, inicializar páginas
- tiendas en línea, inicializar páginas
- tipo 2 tiendas en línea, inicializando páginas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- inicializar páginas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269077"
---
# <a name="initializing-the-page"></a><span data-ttu-id="2164f-113">Inicialización de la página</span><span class="sxs-lookup"><span data-stu-id="2164f-113">Initializing the Page</span></span>

<span data-ttu-id="2164f-114">Cuando se carga la página web, se ejecuta la función **init** .</span><span class="sxs-lookup"><span data-stu-id="2164f-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="2164f-115">Este código recupera primero los datos almacenados en una sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="2164f-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="2164f-116">Para obtener más información, consulte mantenimiento de la [información de sesión](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="2164f-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="2164f-117">Después crea el objeto **Downloadmanager** y lo almacena en la variable global denominada g \_ oManager.</span><span class="sxs-lookup"><span data-stu-id="2164f-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="2164f-118">A continuación, la función conecta el evento **OnColorChange** a la función denominada **OnAppColor** y, a continuación, llama directamente a la función para inicializar el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="2164f-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="2164f-119">Vea [buscar coincidencias con los colores de Media Player de Windows](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="2164f-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="2164f-120">Por último, la función inicia un temporizador con un intervalo de un segundo e inicializa los cuadros de lista que muestran las colecciones de descarga pendientes y los elementos de descarga.</span><span class="sxs-lookup"><span data-stu-id="2164f-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="2164f-121">Esto es importante porque puede haber sesiones en curso la última vez que se cerró la tienda en línea y es necesario volver a mostrar esta información.</span><span class="sxs-lookup"><span data-stu-id="2164f-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2164f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2164f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2164f-123">**Uso del administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="2164f-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




