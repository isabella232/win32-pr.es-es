---
title: Administración de usuarios
description: Obtenga información sobre la administración de usuarios. Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, administrar usuarios
- usuarios de AD
- usuarios ad , administrar usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8154dc9d062b86d10b0df6418b5b4cbb79b44d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395320"
---
# <a name="managing-users"></a><span data-ttu-id="c8b88-107">Administración de usuarios</span><span class="sxs-lookup"><span data-stu-id="c8b88-107">Managing Users</span></span>

<span data-ttu-id="c8b88-108">Las cuentas de usuario se crean y almacenan como objetos en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c8b88-108">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="c8b88-109">Estos objetos de usuario representan usuarios y equipos.</span><span class="sxs-lookup"><span data-stu-id="c8b88-109">These user objects represent users and computers.</span></span> <span data-ttu-id="c8b88-110">En esta sección se define qué son los usuarios y cómo se usan, y se explica cómo administrar los usuarios mediante programación en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c8b88-110">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="c8b88-111">En esta sección se de tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8b88-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="c8b88-112">Usuarios de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c8b88-112">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="c8b88-113">Entidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="c8b88-113">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="c8b88-114">¿Qué es un usuario?</span><span class="sxs-lookup"><span data-stu-id="c8b88-114">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="c8b88-115">Código de ejemplo para enlazar al contenedor users</span><span class="sxs-lookup"><span data-stu-id="c8b88-115">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="c8b88-116">Atributos de objeto de usuario</span><span class="sxs-lookup"><span data-stu-id="c8b88-116">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="c8b88-117">Creación de un usuario</span><span class="sxs-lookup"><span data-stu-id="c8b88-117">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="c8b88-118">Eliminar un usuario.</span><span class="sxs-lookup"><span data-stu-id="c8b88-118">Deleting a user.</span></span> <span data-ttu-id="c8b88-119">Un usuario se elimina en la misma forma que cualquier otro objeto de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c8b88-119">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="c8b88-120">Para obtener más información sobre cómo eliminar objetos, vea [Crear y eliminar objetos en Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="c8b88-120">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="c8b88-121">Enumeración de usuarios</span><span class="sxs-lookup"><span data-stu-id="c8b88-121">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="c8b88-122">Consulta de usuarios</span><span class="sxs-lookup"><span data-stu-id="c8b88-122">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="c8b88-123">Mover usuarios.</span><span class="sxs-lookup"><span data-stu-id="c8b88-123">Moving users.</span></span> <span data-ttu-id="c8b88-124">Un usuario se mueve en el mismo estado que cualquier otro Active Directory objeto.</span><span class="sxs-lookup"><span data-stu-id="c8b88-124">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="c8b88-125">Para obtener más información sobre cómo mover Active Directory objetos, vea [Mover objetos](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c8b88-125">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="c8b88-126">Administración de usuarios en servidores miembros y Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8b88-126">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




