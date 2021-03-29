---
description: En una comprobación de acceso, el sistema compara la información de seguridad del token de acceso de subprocesos con la información de seguridad del descriptor de seguridad de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interacción entre subprocesos y objetos protegibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912426"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="2962f-103">Interacción entre subprocesos y objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="2962f-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="2962f-104">Cuando un subproceso intenta utilizar un [objeto protegible](securable-objects.md), el sistema realiza una comprobación de acceso antes de permitir que el subproceso continúe.</span><span class="sxs-lookup"><span data-stu-id="2962f-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="2962f-105">En una comprobación de acceso, el sistema compara la información de seguridad en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del subproceso con la información de seguridad del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto.</span><span class="sxs-lookup"><span data-stu-id="2962f-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="2962f-106">El token de acceso contiene los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que identifican al usuario asociado al subproceso.</span><span class="sxs-lookup"><span data-stu-id="2962f-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="2962f-107">El descriptor de seguridad identifica el propietario del objeto y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL).</span><span class="sxs-lookup"><span data-stu-id="2962f-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="2962f-108">La DACL contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE), cada una de las cuales especifica los derechos de acceso permitidos o denegados a un usuario o grupo específico.</span><span class="sxs-lookup"><span data-stu-id="2962f-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="2962f-109">El sistema comprueba la DACL del objeto, buscando las ACE que se aplican a los SID de usuario y de grupo del token de acceso del subproceso.</span><span class="sxs-lookup"><span data-stu-id="2962f-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="2962f-110">El sistema comprueba cada ACE hasta que se haya concedido o denegado el acceso o hasta que no haya más ACE para comprobar.</span><span class="sxs-lookup"><span data-stu-id="2962f-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="2962f-111">Es posible que una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) tenga varias ACE que se aplican a los SID del token.</span><span class="sxs-lookup"><span data-stu-id="2962f-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="2962f-112">Y, si esto ocurre, se acumulan los derechos de acceso concedidos por cada ACE.</span><span class="sxs-lookup"><span data-stu-id="2962f-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="2962f-113">Por ejemplo, si una ACE concede acceso de lectura a un grupo y otra ACE concede acceso de escritura a un usuario que sea miembro del grupo, el usuario puede tener acceso de lectura y escritura al objeto.</span><span class="sxs-lookup"><span data-stu-id="2962f-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="2962f-114">En la ilustración siguiente se muestra la relación entre estos bloques de información de seguridad:</span><span class="sxs-lookup"><span data-stu-id="2962f-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![relaciones entre procesos, ACE y DACL](images/cssec-02.png)

 

 
