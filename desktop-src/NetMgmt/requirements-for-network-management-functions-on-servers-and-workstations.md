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
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Requisitos para las funciones de administración de redes en servidores y estaciones de trabajo

Si llama a una de las funciones de administración de red que se enumeran en este tema en un servidor o estación de trabajo, se aplican diferentes requisitos de acceso a las consultas de información y a las actualizaciones de información.

## <a name="queries"></a>Consultas

Si llama a una de las siguientes funciones para realizar una consulta en un servidor o estación de trabajo, de forma predeterminada, todos los usuarios autenticados pueden leer y enumerar la información.

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo niveles 1 y 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo niveles 2 y 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

A continuación se muestra información adicional sobre el acceso anónimo al leer y enumerar información.

**Windows Server 2003 y Windows XP:** El acceso anónimo a la información es posible si la configuración de la Directiva EveryoneIncludesAnonymous permite el acceso anónimo.

**Windows 2000:** El acceso anónimo a objetos protegibles es posible si la configuración de la Directiva RestrictAnonymous permite el acceso anónimo. Puede restringir el acceso anónimo si establece la clave siguiente en el registro en el valor 1.

**HKEY \_ \_Equipo local \\ sistema \\ CurrentControlSet \\ control \\ LSA** \\ **RestrictAnonymous** = 1

Para obtener más información, consulte el siguiente artículo de Microsoft Knowledge Base:

IDENTIFICADOR de artículo: [Q246261](https://support.microsoft.com/kb/246261)

TITLE: Cómo usar el valor del Registro RestrictAnonymous.

## <a name="updates"></a>Actualizaciones

De forma predeterminada, solo los administradores y los usuarios avanzados pueden escribir información.

Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control), [privilegios](/windows/desktop/SecAuthZ/privileges)y [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects). Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

 

 