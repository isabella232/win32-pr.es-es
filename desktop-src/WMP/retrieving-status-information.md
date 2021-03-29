---
title: Recuperando información de estado
description: Recuperando información de estado
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, recuperar el estado
- tiendas en línea, recuperar estado
- tipo 2 tiendas en línea, recuperando estado
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- recuperando estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778258"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="cf8d3-113">Recuperando información de estado</span><span class="sxs-lookup"><span data-stu-id="cf8d3-113">Retrieving Status Information</span></span>

<span data-ttu-id="cf8d3-114">La información de estado se actualiza mediante el temporizador creado en la función **init** .</span><span class="sxs-lookup"><span data-stu-id="cf8d3-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="cf8d3-115">Todo el estado se actualiza con el mismo temporizador.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-115">All status is updated using the same timer.</span></span> <span data-ttu-id="cf8d3-116">El nombre de la función para el evento del temporizador es **Altimer**.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="cf8d3-117">**Altimer** determina la información que se va a mostrar en función de la selección del usuario, que se almacena en la variable global denominada g \_ oCurrentDLItem.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="cf8d3-118">La función comprueba primero si los valores de tamaño o progreso son válidos y crea una cadena para cada caso.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="cf8d3-119">Si un valor es válido, la cadena representa el recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="cf8d3-120">Si el valor no es válido, como-1, la cadena proporciona un mensaje para informar al usuario de que la información aún no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="cf8d3-121">Después, un bloque **Switch** determina si la descarga del elemento seleccionado se ha completado o cancelado.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="cf8d3-122">Si alguna de las mayúsculas y minúsculas es true, el valor de las variables size o Progress se actualiza en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="cf8d3-123">Por último, la información de estado se muestra en el elemento DIV denominado dlstate.</span><span class="sxs-lookup"><span data-stu-id="cf8d3-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf8d3-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf8d3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf8d3-125">**Uso del administrador de descargas**</span><span class="sxs-lookup"><span data-stu-id="cf8d3-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




