---
title: Resumen de la capacidad de configurar el montón de descriptores
description: En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105186"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="4e801-103">Resumen de la capacidad de configurar el montón de descriptores</span><span class="sxs-lookup"><span data-stu-id="4e801-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="4e801-104">En la tabla siguiente se resume la información sobre el sombreador y la compatibilidad con el montón visible de no sombreador.</span><span class="sxs-lookup"><span data-stu-id="4e801-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="4e801-105">Montón de descriptor visible del sombreador</span><span class="sxs-lookup"><span data-stu-id="4e801-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="4e801-106">Montón de descriptor visible sin sombreador</span><span class="sxs-lookup"><span data-stu-id="4e801-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e801-107">Tipos de montones admitidos</span><span class="sxs-lookup"><span data-stu-id="4e801-107">Heap Types Supported</span></span>          | <span data-ttu-id="4e801-108">CBV \_ SRV \_ UAV, muestra</span><span class="sxs-lookup"><span data-stu-id="4e801-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="4e801-109">All</span><span class="sxs-lookup"><span data-stu-id="4e801-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4e801-110">Propiedades de la página de CPU admitidas</span><span class="sxs-lookup"><span data-stu-id="4e801-110">CPU Page Properties Supported</span></span> | <span data-ttu-id="4e801-111">NO \_ disponible, combinación de escritura \_</span><span class="sxs-lookup"><span data-stu-id="4e801-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="4e801-112">ESCRITURA \_ inversa</span><span class="sxs-lookup"><span data-stu-id="4e801-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4e801-113">Administración de la residencia por aplicación</span><span class="sxs-lookup"><span data-stu-id="4e801-113">Residency Management By App</span></span>   | <span data-ttu-id="4e801-114">Sí, responsable de la aplicación</span><span class="sxs-lookup"><span data-stu-id="4e801-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="4e801-115">No es aplicable (no es visible para GPU).</span><span class="sxs-lookup"><span data-stu-id="4e801-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4e801-116">Compatibilidad con la edición de descriptores</span><span class="sxs-lookup"><span data-stu-id="4e801-116">Descriptor Edit Support</span></span>       | <span data-ttu-id="4e801-117">Solo destino de copia, a través de la actualización de la lista de comandos o la copia de la CPU si la CPU es visible.</span><span class="sxs-lookup"><span data-stu-id="4e801-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="4e801-118">Solo lectura y escritura de CPU.</span><span class="sxs-lookup"><span data-stu-id="4e801-118">CPU read and write only.</span></span> <span data-ttu-id="4e801-119">No hay acceso directo a la GPU.</span><span class="sxs-lookup"><span data-stu-id="4e801-119">No direct GPU access.</span></span> <span data-ttu-id="4e801-120">Se puede usar para la copia de CPU inmediata (como origen y destino).</span><span class="sxs-lookup"><span data-stu-id="4e801-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="4e801-121">Se puede usar como origen de actualización en una lista de comandos: esto copiará los descriptores en el almacenamiento de la lista de comandos durante el registro de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="4e801-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="4e801-122">En la ejecución, la copia almacenada se copiará en el destino, que debe ser un montón visible de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4e801-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4e801-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e801-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e801-124">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="4e801-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




