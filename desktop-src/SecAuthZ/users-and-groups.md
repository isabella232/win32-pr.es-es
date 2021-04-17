---
description: Explica la definición de usuarios y grupos en la API de administrador de autorización.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuarios y grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653069"
---
# <a name="users-and-groups"></a><span data-ttu-id="7a70b-103">Usuarios y grupos</span><span class="sxs-lookup"><span data-stu-id="7a70b-103">Users and Groups</span></span>

<span data-ttu-id="7a70b-104">En Administrador de autorización, los destinatarios de la Directiva de autorización se representan mediante los siguientes grupos:</span><span class="sxs-lookup"><span data-stu-id="7a70b-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="7a70b-105">Usuarios y grupos de Windows</span><span class="sxs-lookup"><span data-stu-id="7a70b-105">Windows Users and Groups</span></span>

    <span data-ttu-id="7a70b-106">Estos grupos incluyen usuarios, equipos y grupos integrados para entidades de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7a70b-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="7a70b-107">Grupos de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="7a70b-107">LDAP Query Groups</span></span>

    <span data-ttu-id="7a70b-108">La pertenencia a estos grupos se calcula dinámicamente según sea necesario desde las consultas de Protocolo ligero de acceso a directorios (LDAP).</span><span class="sxs-lookup"><span data-stu-id="7a70b-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="7a70b-109">Un grupo de consulta LDAP es un tipo de grupo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a70b-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="7a70b-110">Grupos de aplicaciones básicos</span><span class="sxs-lookup"><span data-stu-id="7a70b-110">Basic Application Groups</span></span>

    <span data-ttu-id="7a70b-111">Estos grupos se componen de grupos de consulta LDAP, usuarios y grupos de Windows y otros grupos de aplicaciones básicos.</span><span class="sxs-lookup"><span data-stu-id="7a70b-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="7a70b-112">Usuarios y grupos de Windows</span><span class="sxs-lookup"><span data-stu-id="7a70b-112">Windows Users and Groups</span></span>

<span data-ttu-id="7a70b-113">Son los mismos que los usuarios y grupos que se usan en todo el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="7a70b-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="7a70b-114">Grupos de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="7a70b-114">LDAP Query Groups</span></span>

<span data-ttu-id="7a70b-115">En Administrador de autorización, puede usar consultas LDAP para hacer coincidir los atributos del usuario con los del objeto del usuario en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a70b-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="7a70b-116">Por ejemplo, la siguiente consulta busca todos los usuarios excepto Andy.</span><span class="sxs-lookup"><span data-stu-id="7a70b-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="7a70b-117">La siguiente consulta busca todos los miembros del alias alguien en www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="7a70b-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="7a70b-118">Grupos de aplicaciones básicos</span><span class="sxs-lookup"><span data-stu-id="7a70b-118">Basic Application Groups</span></span>

<span data-ttu-id="7a70b-119">En la API de administrador de autorización, un grupo de aplicaciones se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="7a70b-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="7a70b-120">Un grupo de aplicación básico es un tipo de grupo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a70b-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="7a70b-121">Para definir la pertenencia a grupos de aplicaciones básica, defina quién es miembro y defina quién no es miembro.</span><span class="sxs-lookup"><span data-stu-id="7a70b-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="7a70b-122">Ambos pasos se realizan de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="7a70b-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="7a70b-123">Especifique cero o más usuarios y grupos de Windows, grupos de aplicaciones básicos definidos previamente o grupos de consultas LDAP.</span><span class="sxs-lookup"><span data-stu-id="7a70b-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="7a70b-124">La pertenencia del grupo de aplicación básico se calcula quitando los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="7a70b-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="7a70b-125">Administrador de autorización lo hace automáticamente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7a70b-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="7a70b-126">La no afiliación de un grupo de aplicación básico tiene prioridad sobre la pertenencia.</span><span class="sxs-lookup"><span data-stu-id="7a70b-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="7a70b-127">No se permiten definiciones de pertenencia circulares; dan como resultado el siguiente mensaje de error: "no se puede Agregar GroupName.</span><span class="sxs-lookup"><span data-stu-id="7a70b-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="7a70b-128">Se produjo el siguiente problema: se ha detectado un bucle ".</span><span class="sxs-lookup"><span data-stu-id="7a70b-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a70b-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a70b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a70b-130">Definir grupos de usuarios en C++</span><span class="sxs-lookup"><span data-stu-id="7a70b-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



