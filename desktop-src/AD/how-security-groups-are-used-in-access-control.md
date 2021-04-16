---
title: Cómo se usan los grupos de seguridad en Access Control
description: El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o el grupo se utiliza por motivos de seguridad.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Cómo se usan los grupos de seguridad en Access Control
- control de acceso, grupos de seguridad usados en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656230"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="7855e-105">Cómo se usan los grupos de seguridad en Access Control</span><span class="sxs-lookup"><span data-stu-id="7855e-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="7855e-106">El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o el grupo se utiliza por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7855e-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="7855e-107">El nombre del usuario o grupo no se utiliza como identificador único en el sistema.</span><span class="sxs-lookup"><span data-stu-id="7855e-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="7855e-108">El SID se almacena en el atributo **objectSid** de objetos de usuario y objetos de grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7855e-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="7855e-109">El servidor de Active Directory genera el **objectSid** cuando se crea el usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="7855e-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="7855e-110">El sistema garantiza que los SID son únicos en todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="7855e-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="7855e-111">Tenga en cuenta que **objectGuid** es el identificador único de un usuario, grupo o cualquier otro objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="7855e-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="7855e-112">El SID cambia si un usuario o grupo se mueve a otro dominio; **objectGuid** sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="7855e-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="7855e-113">Cuando a un usuario o grupo se le concede permiso para tener acceso a un recurso, como una impresora o un recurso compartido de archivos, se agrega el SID del usuario o grupo a la entrada de control de acceso (ACE) que define el permiso concedido en la lista de control de acceso discrecional (DACL) del recurso.</span><span class="sxs-lookup"><span data-stu-id="7855e-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="7855e-114">En Active Directory Domain Services, cada objeto tiene un atributo **nTSecurityDescriptor** que almacena una DACL que define el acceso a ese objeto o atributos concretos en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="7855e-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="7855e-115">Para obtener más información sobre cómo establecer el control de acceso en los objetos de Active Directory Domain Services, vea [controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="7855e-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="7855e-116">Cuando un usuario inicia sesión en un dominio de Windows 2000, el sistema operativo genera un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="7855e-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="7855e-117">Este token de acceso se usa para determinar a qué recursos puede tener acceso el usuario.</span><span class="sxs-lookup"><span data-stu-id="7855e-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="7855e-118">El token de acceso de usuario incluye los datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7855e-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="7855e-119">SID de usuario.</span><span class="sxs-lookup"><span data-stu-id="7855e-119">User SID.</span></span>
-   <span data-ttu-id="7855e-120">SID de todos los grupos de seguridad globales y universales de los que es miembro el usuario.</span><span class="sxs-lookup"><span data-stu-id="7855e-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="7855e-121">SID de todos los grupos de seguridad globales y universales anidados.</span><span class="sxs-lookup"><span data-stu-id="7855e-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="7855e-122">Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.</span><span class="sxs-lookup"><span data-stu-id="7855e-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="7855e-123">Cuando el usuario intenta obtener acceso a los recursos de un equipo, el servicio a través del cual el usuario tiene acceso al recurso suplantará al usuario mediante la creación de un nuevo token de acceso basado en el token de acceso creado en el momento de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="7855e-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="7855e-124">Este nuevo token de acceso también contendrá los siguientes SID:</span><span class="sxs-lookup"><span data-stu-id="7855e-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="7855e-125">SID para todos los grupos locales de dominio del dominio de destino de los que el usuario es miembro.</span><span class="sxs-lookup"><span data-stu-id="7855e-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="7855e-126">SID para todos los grupos locales de la máquina del equipo de destino de los que el usuario es miembro.</span><span class="sxs-lookup"><span data-stu-id="7855e-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="7855e-127">El servicio usa este nuevo token de acceso para evaluar el acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="7855e-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="7855e-128">Si aparece un SID en el token de acceso en cualquier ACE de la DACL, el servicio concede al usuario los permisos especificados en esas ACE.</span><span class="sxs-lookup"><span data-stu-id="7855e-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 




