---
description: Varios procesos pueden tener identificadores para el mismo objeto de evento, exclusión mutua, semáforo o temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronización entre procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667976"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="e73d1-103">Sincronización entre procesos</span><span class="sxs-lookup"><span data-stu-id="e73d1-103">Interprocess Synchronization</span></span>

<span data-ttu-id="e73d1-104">Varios procesos pueden tener identificadores para el mismo objeto de evento, exclusión mutua, semáforo o temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos.</span><span class="sxs-lookup"><span data-stu-id="e73d1-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="e73d1-105">El proceso que crea un objeto puede usar el identificador devuelto por la función de creación ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore (**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span><span class="sxs-lookup"><span data-stu-id="e73d1-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="e73d1-106">Otros procesos pueden abrir un identificador para el objeto utilizando su nombre o a través de la herencia o la duplicación.</span><span class="sxs-lookup"><span data-stu-id="e73d1-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="e73d1-107">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e73d1-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e73d1-108">Nombres de objeto</span><span class="sxs-lookup"><span data-stu-id="e73d1-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="e73d1-109">Herencia de objetos</span><span class="sxs-lookup"><span data-stu-id="e73d1-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="e73d1-110">Duplicación de objetos</span><span class="sxs-lookup"><span data-stu-id="e73d1-110">Object Duplication</span></span>](object-duplication.md)

 

 
