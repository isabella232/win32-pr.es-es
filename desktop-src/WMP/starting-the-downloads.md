---
title: Iniciar las descargas
description: Iniciar las descargas
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, iniciar descargas
- tiendas en línea, iniciar descargas
- tipo 2 tiendas en línea, iniciar descargas
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- iniciar descargas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419085"
---
# <a name="starting-the-downloads"></a><span data-ttu-id="197f1-113">Iniciar las descargas</span><span class="sxs-lookup"><span data-stu-id="197f1-113">Starting the Downloads</span></span>

<span data-ttu-id="197f1-114">La descarga se inicia cuando el usuario hace clic en **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="197f1-114">The downloading starts when the user clicks **Download**.</span></span> <span data-ttu-id="197f1-115">Este botón se denomina btnDownload en el código y la función de controlador de eventos para el evento **onclick** se denomina "aldescargar".</span><span class="sxs-lookup"><span data-stu-id="197f1-115">This button is named btnDownload in the code and the event handler function for the **onClick** event is named "OnDownload".</span></span>

<span data-ttu-id="197f1-116">"Undownload" crea primero un nuevo objeto **DownloadCollection** vacío y lo asigna a una variable local.</span><span class="sxs-lookup"><span data-stu-id="197f1-116">"OnDownload" first creates a new empty **DownloadCollection** object and assigns it to a local variable.</span></span>


```C++
oDLC = g_oManager.createDownloadCollection();

```



<span data-ttu-id="197f1-117">A continuación, la función inicia cada uno de los cinco elementos que se descargan y almacena el objeto **DownloadItem** devuelto en una matriz.</span><span class="sxs-lookup"><span data-stu-id="197f1-117">Next, the function starts each of the five items downloading and stores the returned **DownloadItem** object in an array.</span></span>


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



<span data-ttu-id="197f1-118">A continuación, el código actualiza los elementos de la interfaz de usuario con la información sobre la colección de descarga y sus elementos de descarga.</span><span class="sxs-lookup"><span data-stu-id="197f1-118">The code then updates the user interface elements with the information about the download collection and its download items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="197f1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="197f1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="197f1-120">**Uso del administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="197f1-120">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




