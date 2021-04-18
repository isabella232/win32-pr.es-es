---
description: Heredar transacciones manuales
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Heredar transacciones manuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705263"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="c1c2f-103">Heredar transacciones manuales</span><span class="sxs-lookup"><span data-stu-id="c1c2f-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="c1c2f-104">Si un objeto con una transacción de transacciones manuales en su contexto crea un segundo objeto, el objeto de nivel inferior puede heredar la transacción de transacciones de transacciones (si se configura para que herede transacciones).</span><span class="sxs-lookup"><span data-stu-id="c1c2f-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="c1c2f-105">El primer objeto creado mediante la puerta de enlace de transacciones se debe configurar para "requerir" o "admitir" transacciones.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="c1c2f-106">Los objetos subsiguientes de la actividad se pueden configurar en función de los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="c1c2f-107">En el caso de las transacciones automáticas, el tiempo de ejecución de COM+ no intenta confirmar la transacción hasta que el objeto raíz indica que está preparada (llamando a [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) antes de volver de una llamada).</span><span class="sxs-lookup"><span data-stu-id="c1c2f-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="c1c2f-108">Los usuarios deben tener en cuenta que una transacción de transacciones se puede confirmar prematuramente (en el caso de que no se haya completado el trabajo de los objetos secundarios), ya que la "raíz" no se está ejecutando en el entorno de tiempo de ejecución de COM+ y la semántica de confirmación no está asociada a la duración del objeto.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="c1c2f-109">En general, el usuario debe tener cuidado de no infringir el límite de sincronización de la transacción.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="c1c2f-110">De lo contrario, se aplica la semántica de confirmación de COM+.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="c1c2f-111">COM+ no intentará confirmar una transacción mientras un objeto dentro de un límite de sincronización está llamando a.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="c1c2f-112">Además, los objetos pueden indicar su coherencia mediante [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span><span class="sxs-lookup"><span data-stu-id="c1c2f-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="c1c2f-113">Si se intenta confirmar una transacción que incluye el trabajo de un objeto que ha llamado a **DisableCommit**, se anulará la transacción.</span><span class="sxs-lookup"><span data-stu-id="c1c2f-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



