---
title: Particiones de directorio de aplicaciones
description: En Windows Server 2003, Active Directory Domain Services admiten particiones de directorio de aplicaciones.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- AD de particiones de directorio de aplicaciones
- Particiones de directorio de aplicaciones AD, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077567"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="d1ee3-105">Particiones de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-105">Application Directory Partitions</span></span>

<span data-ttu-id="d1ee3-106">En Windows Server 2003, Active Directory Domain Services admiten particiones de directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="d1ee3-107">Una partición de directorio de aplicaciones puede contener una jerarquía de cualquier tipo de objeto, excepto las entidades de seguridad, y se puede configurar para replicar en cualquier conjunto de controladores de dominio del bosque.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="d1ee3-108">A diferencia de una partición de dominio, no se necesita una partición de directorio de aplicaciones para replicar en todos los controladores de dominio de un dominio y la partición se puede replicar en controladores de dominio en dominios diferentes del bosque.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="d1ee3-109">Para obtener más información acerca de las particiones de directorio de aplicaciones, consulte [acerca de las particiones de directorio de aplicaciones](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="d1ee3-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="d1ee3-110">Se puede crear una partición de directorio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-110">An application directory partition can be created.</span></span> <span data-ttu-id="d1ee3-111">se modificó y eliminó mediante las operaciones estándar ADSI, LDAP y [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="d1ee3-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="d1ee3-112">El contexto de seguridad necesario para crear y modificar una partición de directorio de aplicación es el mismo que para crear una partición de dominio.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="d1ee3-113">En los temas siguientes se describe cómo trabajar con particiones de directorio de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="d1ee3-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="d1ee3-114">Replicación de partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="d1ee3-115">Seguridad de partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="d1ee3-116">Crear una partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="d1ee3-117">Eliminar una partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="d1ee3-118">Enumerar particiones de directorio de aplicaciones en un bosque</span><span class="sxs-lookup"><span data-stu-id="d1ee3-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="d1ee3-119">Localizar un servidor host de partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="d1ee3-120">Agregar o eliminar una réplica de partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="d1ee3-121">Enumerar réplicas de una partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="d1ee3-122">Modificar la configuración de la partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d1ee3-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 