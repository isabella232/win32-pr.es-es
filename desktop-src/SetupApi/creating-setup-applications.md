---
description: Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación. Llame a las funciones de configuración desde la aplicación de instalación para realizar muchas operaciones de instalación.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Crear aplicaciones de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667884"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="832d1-104">Crear aplicaciones de instalación</span><span class="sxs-lookup"><span data-stu-id="832d1-104">Creating Setup Applications</span></span>

<span data-ttu-id="832d1-105">Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="832d1-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="832d1-106">Llame a las funciones de configuración desde la aplicación de instalación para realizar muchas operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="832d1-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="832d1-107">En los pasos siguientes se describe una manera de usar las funciones de configuración de para crear una aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="832d1-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="832d1-108">Puede usar este ejemplo como punto de partida o desarrollar su propio algoritmo de instalación.</span><span class="sxs-lookup"><span data-stu-id="832d1-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="832d1-109">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="832d1-109">**Initialization**</span></span>

-   [<span data-ttu-id="832d1-110">Abra el archivo INF y, si procede, anexe otros archivos INF.</span><span class="sxs-lookup"><span data-stu-id="832d1-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="832d1-111">Extraiga la información del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="832d1-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="832d1-112">Recopile información de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="832d1-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="832d1-113">Cree una cola.</span><span class="sxs-lookup"><span data-stu-id="832d1-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="832d1-114">**Archivos de instalación**</span><span class="sxs-lookup"><span data-stu-id="832d1-114">**Install files**</span></span>

-   [<span data-ttu-id="832d1-115">Confirme la cola y especifique una rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="832d1-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="832d1-116">Actualice la información del registro.</span><span class="sxs-lookup"><span data-stu-id="832d1-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="832d1-117">**Limpieza**</span><span class="sxs-lookup"><span data-stu-id="832d1-117">**Clean up**</span></span>

-   [<span data-ttu-id="832d1-118">Cierre la cola de archivos y el archivo INF.</span><span class="sxs-lookup"><span data-stu-id="832d1-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="832d1-119">Libere cualquier otro recurso del sistema y finalice el programa.</span><span class="sxs-lookup"><span data-stu-id="832d1-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



