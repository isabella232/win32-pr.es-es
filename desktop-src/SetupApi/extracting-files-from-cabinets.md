---
description: Puede extraer archivos de un archivo. cab de dos maneras. La primera y la manera más sencilla es aprovechar el procesamiento automático de los contenedores integrados en las funciones de configuración.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraer archivos de los archivadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666646"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="87b17-104">Extraer archivos de los archivadores</span><span class="sxs-lookup"><span data-stu-id="87b17-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="87b17-105">Puede extraer archivos de un archivo. cab de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="87b17-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="87b17-106">La primera y la manera más sencilla es aprovechar el procesamiento automático de los contenedores integrados en las funciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="87b17-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="87b17-107">Las funciones de instalación, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)y [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), comprueban la compresión en cada archivo.</span><span class="sxs-lookup"><span data-stu-id="87b17-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="87b17-108">Si el archivo está en un archivo. cab, las funciones buscan primero un archivo con ese nombre fuera del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="87b17-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="87b17-109">Si se encuentra, las funciones instalan el archivo externo, omitiendo el archivo dentro del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="87b17-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="87b17-110">Esto le permite actualizar un solo archivo dentro del archivo. cab sin volver a generarlo.</span><span class="sxs-lookup"><span data-stu-id="87b17-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="87b17-111">Las funciones de configuración también realizan un seguimiento de los archivos de un archivo. cab que se han recuperado, de modo que un archivo se extrae solo una vez, incluso si se instala varias veces.</span><span class="sxs-lookup"><span data-stu-id="87b17-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="87b17-112">La segunda manera de extraer archivos de un archivo. cab es mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="87b17-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="87b17-113">Esta función recorre en iteración todos los archivos de un archivo. cab y envía una notificación a una rutina de devolución de llamada para cada archivo encontrado.</span><span class="sxs-lookup"><span data-stu-id="87b17-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="87b17-114">A continuación, la rutina de devolución de llamada devuelve un valor que indica si el archivo debe extraerse u omitirse.</span><span class="sxs-lookup"><span data-stu-id="87b17-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="87b17-115">La API de instalación no proporciona una rutina de devolución de llamada predeterminada para controlar las notificaciones del archivo.</span><span class="sxs-lookup"><span data-stu-id="87b17-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="87b17-116">Si llama explícitamente a [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , debe proporcionar una rutina de devolución de llamada para procesar las notificaciones del archivo CAB que devuelve la función.</span><span class="sxs-lookup"><span data-stu-id="87b17-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



