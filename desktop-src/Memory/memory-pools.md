---
description: 'El administrador de memoria crea los siguientes grupos de memoria que el sistema utiliza para asignar memoria: bloque no paginado y grupo paginado.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Grupos de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678529"
---
# <a name="memory-pools"></a><span data-ttu-id="d52df-103">Grupos de memoria</span><span class="sxs-lookup"><span data-stu-id="d52df-103">Memory Pools</span></span>

<span data-ttu-id="d52df-104">El administrador de memoria crea los siguientes grupos de memoria que el sistema utiliza para asignar memoria: bloque no paginado y grupo paginado.</span><span class="sxs-lookup"><span data-stu-id="d52df-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="d52df-105">Ambos grupos de memoria se encuentran en la región del espacio de direcciones que se reserva para el sistema y se asignan en el espacio de direcciones virtuales de cada proceso.</span><span class="sxs-lookup"><span data-stu-id="d52df-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="d52df-106">El bloque no paginado consta de direcciones de memoria virtual que se garantiza que residen en la memoria física siempre que se asignen los objetos de kernel correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d52df-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="d52df-107">El bloque paginado se compone de la memoria virtual que se puede paginar dentro y fuera del sistema.</span><span class="sxs-lookup"><span data-stu-id="d52df-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="d52df-108">Para mejorar el rendimiento, los sistemas con un solo procesador tienen tres grupos paginados y los sistemas multiprocesador tienen cinco grupos paginados.</span><span class="sxs-lookup"><span data-stu-id="d52df-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="d52df-109">Los identificadores de los [objetos de kernel](../sysinfo/kernel-objects.md) se almacenan en el grupo paginado, por lo que el número de identificadores que se pueden crear se basa en la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="d52df-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="d52df-110">El sistema registra los límites y los valores actuales de su bloque no paginado, el grupo paginado y el uso del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="d52df-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="d52df-111">Para obtener más información, vea [información sobre el rendimiento](memory-performance-information.md)de la memoria.</span><span class="sxs-lookup"><span data-stu-id="d52df-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
