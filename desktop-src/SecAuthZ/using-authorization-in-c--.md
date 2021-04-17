---
description: Use la API de administrador de autorización para controlar el acceso a los recursos de la aplicación.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Usar la autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668047"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="2ed05-103">Usar la autorización en C++</span><span class="sxs-lookup"><span data-stu-id="2ed05-103">Using Authorization in C++</span></span>

<span data-ttu-id="2ed05-104">Puede usar la API de administrador de autorización para controlar el acceso a los recursos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ed05-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="2ed05-105">Si tiene una solución de control de acceso en función de [*las listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) y desea evitar la conversión de esta solución para usar administrador de autorización, puede seguir usando ACL para controlar el acceso a los recursos.</span><span class="sxs-lookup"><span data-stu-id="2ed05-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="2ed05-106">Para obtener información sobre cómo controlar el acceso a los recursos mediante ACL, vea [definir permisos con ACL en c++](defining-permissions-with-acls-in-c--.md), [establecer un contexto de cliente a partir de un SID en c++](establishing-a-client-context-from-a-sid-in-c--.md)y [comprobar el acceso de cliente con ACL en c++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="2ed05-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="2ed05-107">En el caso de las grandes empresas, existe un equilibrio entre la sobrecarga administrativa y el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2ed05-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="2ed05-108">A medida que aumenta el número de recursos y usuarios protegidos, la administración de las ACL es más complicada.</span><span class="sxs-lookup"><span data-stu-id="2ed05-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="2ed05-109">El rendimiento no se ve afectado porque toda la información necesaria sobre los derechos de acceso se distribuye a los recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="2ed05-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="2ed05-110">El rendimiento de administrador de autorización se ve afectado por el escalado.</span><span class="sxs-lookup"><span data-stu-id="2ed05-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="2ed05-111">Para obtener información acerca de otras tareas de autorización, consulte [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="2ed05-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="2ed05-112">Tema</span><span class="sxs-lookup"><span data-stu-id="2ed05-112">Topic</span></span>                                                                                                                | <span data-ttu-id="2ed05-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ed05-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed05-114">Definir permisos en C++</span><span class="sxs-lookup"><span data-stu-id="2ed05-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="2ed05-115">Defina qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización.</span><span class="sxs-lookup"><span data-stu-id="2ed05-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="2ed05-116">Comprobar el acceso del cliente a un recurso solicitado en C++</span><span class="sxs-lookup"><span data-stu-id="2ed05-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="2ed05-117">Compruebe si el cliente tiene acceso a una o varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="2ed05-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="2ed05-118">Delegación de la definición de permisos en C++</span><span class="sxs-lookup"><span data-stu-id="2ed05-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="2ed05-119">Delegue la administración de almacenes de directivas de autorización que se almacenan en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ed05-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
