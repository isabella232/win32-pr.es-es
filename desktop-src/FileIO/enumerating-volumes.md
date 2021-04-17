---
description: Para realizar una lista completa de los volúmenes de un equipo o para manipular cada volumen a su vez, puede enumerar los volúmenes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerar volúmenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687794"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="626bc-103">Enumerar volúmenes</span><span class="sxs-lookup"><span data-stu-id="626bc-103">Enumerating Volumes</span></span>

<span data-ttu-id="626bc-104">Para realizar una lista completa de los volúmenes de un equipo o para manipular cada volumen a su vez, puede enumerar los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="626bc-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="626bc-105">Dentro de un volumen, puede [Buscar carpetas montadas](enumerating-volume-mount-points.md) u otros objetos en el volumen.</span><span class="sxs-lookup"><span data-stu-id="626bc-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="626bc-106">Tres funciones permiten a una aplicación enumerar volúmenes en un equipo:</span><span class="sxs-lookup"><span data-stu-id="626bc-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="626bc-107">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="626bc-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="626bc-108">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="626bc-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="626bc-109">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="626bc-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="626bc-110">Estas tres funciones funcionan de forma muy similar a las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="626bc-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="626bc-111">Inicia una búsqueda de volúmenes con [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="626bc-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="626bc-112">Si la búsqueda se realiza correctamente, procese los resultados según el diseño de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="626bc-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="626bc-113">A continuación, use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) en un bucle para buscar y procesar cada volumen subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="626bc-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="626bc-114">Una vez agotado el suministro de volúmenes, cierre la búsqueda con [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="626bc-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="626bc-115">No debe asumir ninguna correlación entre el orden de los volúmenes que devuelven estas funciones y el orden de los volúmenes devueltos por otras funciones o herramientas.</span><span class="sxs-lookup"><span data-stu-id="626bc-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="626bc-116">En concreto, no asuma ninguna correlación entre el orden de volumen y las letras de unidad asignadas por el BIOS (si existe) o el administrador de discos.</span><span class="sxs-lookup"><span data-stu-id="626bc-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="626bc-117">Vea [ejemplos de carpetas montadas](volume-mount-point-examples.md) para obtener un ejemplo de cómo enumerar los volúmenes de un equipo.</span><span class="sxs-lookup"><span data-stu-id="626bc-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



