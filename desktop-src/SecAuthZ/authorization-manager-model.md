---
description: El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones. Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modelo de administrador de autorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361721"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="e656a-104">Modelo de administrador de autorización</span><span class="sxs-lookup"><span data-stu-id="e656a-104">Authorization Manager Model</span></span>

<span data-ttu-id="e656a-105">El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e656a-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="e656a-106">Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e656a-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="e656a-107">Las aplicaciones del administrador de autorización almacenan la directiva de autorización en forma de almacenes de autorización que se guardan en Active Directory o archivos XML y aplican la directiva de autorización en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e656a-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="e656a-108">Las aplicaciones llaman a un método de comprobación de acceso en tiempo de ejecución que comprueba el acceso a la información de la Directiva en el almacén de autorización.</span><span class="sxs-lookup"><span data-stu-id="e656a-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="e656a-109">La Directiva de autorización incluye las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="e656a-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="e656a-110">Almacenes de directivas, aplicaciones y ámbitos</span><span class="sxs-lookup"><span data-stu-id="e656a-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="e656a-111">Usuarios y grupos</span><span class="sxs-lookup"><span data-stu-id="e656a-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="e656a-112">Operaciones y tareas</span><span class="sxs-lookup"><span data-stu-id="e656a-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="e656a-113">Roles</span><span class="sxs-lookup"><span data-stu-id="e656a-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="e656a-114">Reglas de negocio</span><span class="sxs-lookup"><span data-stu-id="e656a-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="e656a-115">Colecciones</span><span class="sxs-lookup"><span data-stu-id="e656a-115">Collections</span></span>](collections.md)

 

 



