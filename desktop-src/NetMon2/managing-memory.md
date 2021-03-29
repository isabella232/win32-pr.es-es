---
description: Si se produce un error en el experto durante el tiempo de ejecución, si utiliza Monitor de red funciones para la administración de memoria, Monitor de red liberará memoria asignada.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Administrar memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001235"
---
# <a name="managing-memory"></a><span data-ttu-id="9f6b6-103">Administrar memoria</span><span class="sxs-lookup"><span data-stu-id="9f6b6-103">Managing Memory</span></span>

<span data-ttu-id="9f6b6-104">Si se produce un error en el experto durante el tiempo de ejecución, si utiliza Monitor de red funciones para la administración de memoria, Monitor de red liberará memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="9f6b6-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="9f6b6-105">Sin embargo, cuando se escribe un experto, podría ser necesario adquirir recursos del sistema e información de la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="9f6b6-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="9f6b6-106">Por ejemplo, el experto de combinación de protocolos de Monitor de red adquiere un identificador de archivo para crear una nueva captura.</span><span class="sxs-lookup"><span data-stu-id="9f6b6-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="9f6b6-107">Cada experto debe crear su propio control **try/catch** para que el experto pueda liberar los recursos adquiridos.</span><span class="sxs-lookup"><span data-stu-id="9f6b6-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="9f6b6-108">Cuando se asigna la memoria, use las siguientes funciones de memoria existentes:</span><span class="sxs-lookup"><span data-stu-id="9f6b6-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="9f6b6-109">**ExpertAllocMemory**</span><span class="sxs-lookup"><span data-stu-id="9f6b6-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="9f6b6-110">**ExpertReallocMemory**</span><span class="sxs-lookup"><span data-stu-id="9f6b6-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



