---
title: Requisitos para las funciones de administración de redes en servidores y estaciones de trabajo
description: Si llama a una de las funciones de administración de red que se enumeran en este tema en un servidor o estación de trabajo, se aplican diferentes requisitos de acceso a las consultas de información y a las actualizaciones de información.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904778"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="0bc5e-103">Requisitos para las funciones de administración de redes en servidores y estaciones de trabajo</span><span class="sxs-lookup"><span data-stu-id="0bc5e-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="0bc5e-104">Si llama a una de las funciones de administración de red que se enumeran en este tema en un servidor o estación de trabajo, se aplican diferentes requisitos de acceso a las consultas de información y a las actualizaciones de información.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="0bc5e-105">Consultas</span><span class="sxs-lookup"><span data-stu-id="0bc5e-105">Queries</span></span>

<span data-ttu-id="0bc5e-106">Si llama a una de las siguientes funciones para realizar una consulta en un servidor o estación de trabajo, de forma predeterminada, todos los usuarios autenticados pueden leer y enumerar la información.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="0bc5e-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="0bc5e-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="0bc5e-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="0bc5e-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="0bc5e-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo niveles 1 y 2)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="0bc5e-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo niveles 2 y 502)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="0bc5e-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="0bc5e-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="0bc5e-114">A continuación se muestra información adicional sobre el acceso anónimo al leer y enumerar información.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="0bc5e-115">**Windows Server 2003 y Windows XP:** El acceso anónimo a la información es posible si la configuración de la Directiva EveryoneIncludesAnonymous permite el acceso anónimo.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="0bc5e-116">**Windows 2000:** El acceso anónimo a objetos protegibles es posible si la configuración de la Directiva RestrictAnonymous permite el acceso anónimo.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="0bc5e-117">Puede restringir el acceso anónimo si establece la clave siguiente en el registro en el valor 1.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="0bc5e-118">**HKEY \_ \_Equipo local \\ sistema \\ CurrentControlSet \\ control \\ LSA** \\ **RestrictAnonymous** = 1</span><span class="sxs-lookup"><span data-stu-id="0bc5e-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="0bc5e-119">Para obtener más información, consulte el siguiente artículo de Microsoft Knowledge Base:</span><span class="sxs-lookup"><span data-stu-id="0bc5e-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="0bc5e-120">IDENTIFICADOR de artículo: [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="0bc5e-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="0bc5e-121">TITLE: Cómo usar el valor del Registro RestrictAnonymous.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="0bc5e-122">Actualizaciones</span><span class="sxs-lookup"><span data-stu-id="0bc5e-122">Updates</span></span>

<span data-ttu-id="0bc5e-123">De forma predeterminada, solo los administradores y los usuarios avanzados pueden escribir información.</span><span class="sxs-lookup"><span data-stu-id="0bc5e-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="0bc5e-124">Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control), [privilegios](/windows/desktop/SecAuthZ/privileges)y [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="0bc5e-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="0bc5e-125">Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="0bc5e-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 