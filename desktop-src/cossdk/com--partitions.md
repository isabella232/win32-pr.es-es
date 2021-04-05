---
description: Puede usar el servicio particiones COM+ para instalar diferentes versiones de una aplicación COM+ en un equipo y ejecutarlas simultáneamente.
ms.assetid: fd22a64c-f2d8-48af-86e1-985e21b0f8fa
title: Particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd4e1efdd42ac407d8937c4090c59e65472ed69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907096"
---
# <a name="com-partitions"></a><span data-ttu-id="208d1-103">Particiones COM+</span><span class="sxs-lookup"><span data-stu-id="208d1-103">COM+ Partitions</span></span>

<span data-ttu-id="208d1-104">Puede usar el servicio particiones COM+ para instalar diferentes versiones de una aplicación COM+ en un equipo y ejecutarlas simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="208d1-104">You can use the COM+ partitions service to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="208d1-105">**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible.</span><span class="sxs-lookup"><span data-stu-id="208d1-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="208d1-106">La partición global es la única partición de COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="208d1-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="208d1-107">\* \* Windows 2000: \* \* el servicio de particiones COM+ no está disponible en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="208d1-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

<span data-ttu-id="208d1-108">En los temas siguientes se proporciona información acerca del servicio de particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="208d1-108">The following topics provide information about the COM+ partitions service.</span></span>



| <span data-ttu-id="208d1-109">Tema</span><span class="sxs-lookup"><span data-stu-id="208d1-109">Topic</span></span>                                                               | <span data-ttu-id="208d1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="208d1-110">Description</span></span>                                                                 |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="208d1-111">Conceptos de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="208d1-111">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)<br/> | <span data-ttu-id="208d1-112">Proporciona información general sobre el uso de particiones de COM+.</span><span class="sxs-lookup"><span data-stu-id="208d1-112">Provides an overview of using COM+ partitions.</span></span><br/>                   |
| [<span data-ttu-id="208d1-113">Tareas de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="208d1-113">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)<br/>       | <span data-ttu-id="208d1-114">Proporciona instrucciones para crear y administrar particiones COM+.</span><span class="sxs-lookup"><span data-stu-id="208d1-114">Provides instructions for creating and managing COM+ partitions.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="208d1-115">El servicio de particiones COM+ no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="208d1-115">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="208d1-116">Para usar el servicio de particiones de COM+, debe habilitarlo mediante la herramienta de administración de servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a true.</span><span class="sxs-lookup"><span data-stu-id="208d1-116">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

 

 




