---
title: Consulta de usuarios
description: Para consultar a un usuario, la consulta debe contener la expresión de búsqueda \ 0034;( (usuario de objectClass) (usuario objectCategory)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- usuarios AD, consulta de usuarios
- Active Directory, uso, usuarios, consulta de usuarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789495"
---
# <a name="querying-for-users"></a><span data-ttu-id="2e5c8-105">Consulta de usuarios</span><span class="sxs-lookup"><span data-stu-id="2e5c8-105">Querying for Users</span></span>

<span data-ttu-id="2e5c8-106">Para consultar a un usuario, la consulta debe contener la expresión de búsqueda "(& (objectClass = User) (objectCategory = person))".</span><span class="sxs-lookup"><span data-stu-id="2e5c8-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="2e5c8-107">Dado que la clase Computer es una subclase de User, una consulta que solo contiene (objectClass = User) devolverá objetos de usuario y objetos de equipo.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="2e5c8-108">Además, la categoría de objeto del objeto de usuario es persona (no usuario). por lo tanto, la expresión (objectCategory = user) no devuelve ningún usuario.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="2e5c8-109">Si usa la expresión (objectCategory = person), la consulta devuelve objetos de usuario y objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="2e5c8-110">Los usuarios pueden colocarse en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="2e5c8-111">Esto significa que los usuarios pueden estar en varias ubicaciones en la jerarquía de directorios.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="2e5c8-112">Puede realizar una búsqueda en profundidad de "(objectCategory = user)" para buscar todos los usuarios de un contenedor, una unidad organizativa, un dominio, un árbol de dominio o un bosque, dependiendo del objeto al que esté enlazado el puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que está usando.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 