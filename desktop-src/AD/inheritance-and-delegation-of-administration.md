---
title: Herencia y delegación de la administración
description: Describe AD DS compatibilidad con la herencia de permisos en el árbol de objetos y también la herencia específica del objeto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- herencia y delegación de administración Active Directory
- Active Directory de Active Directory, herencia de permisos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268278"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="3be4e-105">Herencia y delegación de la administración</span><span class="sxs-lookup"><span data-stu-id="3be4e-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="3be4e-106">Active Directory Domain Services admite la herencia de permisos en el árbol de objetos para permitir que las tareas de administración se realicen en niveles superiores del árbol.</span><span class="sxs-lookup"><span data-stu-id="3be4e-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="3be4e-107">Esto permite a los administradores configurar permisos heredables en objetos cercanos a la raíz, como el dominio y las unidades organizativas, y tener esos permisos distribuidos a diversos objetos del árbol.</span><span class="sxs-lookup"><span data-stu-id="3be4e-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="3be4e-108">La herencia se puede establecer por ACE.</span><span class="sxs-lookup"><span data-stu-id="3be4e-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="3be4e-109">En la tabla siguiente se enumeran las marcas que se pueden especificar en **AceFlags** para controlar la herencia de la ACE.</span><span class="sxs-lookup"><span data-stu-id="3be4e-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="3be4e-110">Marca</span><span class="sxs-lookup"><span data-stu-id="3be4e-110">Flag</span></span>                                                     | <span data-ttu-id="3be4e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be4e-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be4e-112">**\_ACE de \_ herencia de ACEFLAG de ADS \_**</span><span class="sxs-lookup"><span data-stu-id="3be4e-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="3be4e-113">Hace que la ACE se herede en el árbol.</span><span class="sxs-lookup"><span data-stu-id="3be4e-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="3be4e-114">**ACEFLAG de anuncios \_ \_ no \_ propagar la \_ ACE de herencia \_**</span><span class="sxs-lookup"><span data-stu-id="3be4e-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="3be4e-115">Hace que la ACE se herede solo en un nivel del árbol.</span><span class="sxs-lookup"><span data-stu-id="3be4e-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="3be4e-116">**ACEFLAG de anuncios \_ \_ solo heredan \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="3be4e-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="3be4e-117">Hace que la ACE se omita en el objeto en el que se especifica, solo se puede heredar y ser efectiva en la que se ha heredado.</span><span class="sxs-lookup"><span data-stu-id="3be4e-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="3be4e-118">Además de establecer la herencia, Active Directory Domain Services admite la herencia específica del objeto.</span><span class="sxs-lookup"><span data-stu-id="3be4e-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="3be4e-119">Esto permite que las ACE heredables se hereden en el árbol, pero solo se aplican a un tipo específico de objeto.</span><span class="sxs-lookup"><span data-stu-id="3be4e-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="3be4e-120">Esto es muy útil para delegar la administración.</span><span class="sxs-lookup"><span data-stu-id="3be4e-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="3be4e-121">Por ejemplo, se puede usar para establecer una ACE heredable específica de un objeto en una unidad organizativa que permita que un grupo tenga control total sobre todos los objetos de usuario en la unidad organizativa, pero nada más.</span><span class="sxs-lookup"><span data-stu-id="3be4e-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="3be4e-122">Por lo tanto, la administración de los usuarios de esa unidad organizativa se delega a los usuarios de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="3be4e-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="3be4e-123">Delegación de la administración de servicios con grupos de seguridad</span><span class="sxs-lookup"><span data-stu-id="3be4e-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="3be4e-124">Use grupos de seguridad para definir y delegar roles administrativos asociados con el servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3be4e-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="3be4e-125">Por ejemplo, el servicio puede estar asociado a un grupo administradores de servicios.</span><span class="sxs-lookup"><span data-stu-id="3be4e-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="3be4e-126">Los usuarios que se identifican como administradores de servicio se agregarán al grupo administradores de el servicio.</span><span class="sxs-lookup"><span data-stu-id="3be4e-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="3be4e-127">El programa de instalación de en el servicio puede establecer ACL en el directorio para permitir que los administradores de el servicio tengan suficientes permisos para leer o escribir atributos relacionados con el servicio, o para crear objetos específicos de este servicio, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3be4e-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="3be4e-128">Roles en grupos de seguridad para equipos que ejecutan el servicio</span><span class="sxs-lookup"><span data-stu-id="3be4e-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="3be4e-129">Use grupos de seguridad para definir el conjunto de equipos a los que se concede acceso a los objetos del servicio en el directorio.</span><span class="sxs-lookup"><span data-stu-id="3be4e-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="3be4e-130">Por ejemplo, el servicio puede estar asociado a un grupo de servidores de servicio.</span><span class="sxs-lookup"><span data-stu-id="3be4e-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="3be4e-131">Todos los equipos que ejecutan el servidor de servicio se agregan al grupo de servidores de servicio y a este grupo se le puede conceder acceso a partes del directorio en el que los servidores de servicio necesitan leer o escribir datos.</span><span class="sxs-lookup"><span data-stu-id="3be4e-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="3be4e-132">El programa de instalación de en el servicio puede establecer ACL en el directorio para habilitar los servidores de servicio de los permisos suficientes para leer y escribir los atributos relacionados con el servicio, o para crear objetos específicos del servicio, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3be4e-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 





