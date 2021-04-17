---
description: Las funciones de configuración controlan internamente los contenedores. Para enumerar y extraer explícitamente los archivos de un archivo. cab, puede llamar a la función SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Uso de archivos. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668289"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="b26a7-104">Uso de archivos. cab</span><span class="sxs-lookup"><span data-stu-id="b26a7-104">Using Cabinet Files</span></span>

<span data-ttu-id="b26a7-105">Las funciones de configuración controlan internamente los contenedores.</span><span class="sxs-lookup"><span data-stu-id="b26a7-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="b26a7-106">Para enumerar y extraer explícitamente los archivos de un archivo. cab, puede llamar a la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="b26a7-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="b26a7-107">En el siguiente tema se describe el procesamiento del archivo. cab interno de las funciones de instalación y cómo usar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="b26a7-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="b26a7-108">También se describen las notificaciones enviadas por **SetupIterateCabinet** y el formato requerido de una rutina de devolución de llamada de archivador para procesar esas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b26a7-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="b26a7-109">Extraer archivos de los archivadores</span><span class="sxs-lookup"><span data-stu-id="b26a7-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="b26a7-110">Crear una rutina de devolución de llamada de archivador</span><span class="sxs-lookup"><span data-stu-id="b26a7-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



