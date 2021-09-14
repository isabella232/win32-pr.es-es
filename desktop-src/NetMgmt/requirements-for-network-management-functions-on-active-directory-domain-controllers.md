---
title: Requisitos para las funciones de administración de redes en Dominio de Active Directory controladores
description: Si llama a una de las funciones de administración de red enumeradas en este tema en un controlador de dominio que ejecuta Active Directory, se permite o deniega el acceso a un objeto protegible en función de la lista de control de acceso (ACL) del objeto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169350"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisitos para las funciones de administración de redes en Dominio de Active Directory controladores

Si llama [a](/windows/desktop/SecAuthZ/securable-objects) una de las funciones de administración de red enumeradas en este tema en un controlador de dominio que ejecuta Active Directory, se permite o se deniega el acceso a un objeto protegible en función de la lista de [control](/windows/desktop/SecAuthZ/access-control-lists) de acceso (ACL) del objeto. (Las ACL se especifican en el directorio).

Se aplican distintos requisitos de acceso a las consultas de información y a las actualizaciones de información.

## <a name="queries"></a>Consultas

En el caso de las consultas, la ACL predeterminada permite que todos los usuarios y miembros autenticados del grupo "Acceso compatible con versiones[anteriores Windows 2000"](/windows/desktop/SecAuthZ/allowing-anonymous-access)lean y enumeren la información. Las funciones enumeradas a continuación se ven afectadas:

-   [**NetGroupEnum,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum) [**NetGroupGetInfo,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo) [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo niveles 1 y 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo niveles 2 y 502)
-   [**NetUserEnum,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) [**NetUserGetGroups,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups) [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

El acceso anónimo a la información de grupo requiere que el usuario Anónimo se agregó explícitamente al grupo "Acceso compatible Windows 2000". Esto se debe a que los tokens anónimos no incluyen el SID del grupo Todos.

**Windows 2000:** De forma predeterminada, el grupo "Acceso compatible Windows 2000" incluye Todos como miembro. Esto permite el acceso anónimo (inicio de sesión anónimo) a la información si el sistema permite el acceso anónimo. Los administradores pueden quitar Todos del grupo "Acceso compatible Windows 2000" en cualquier momento. Quitar Todos del grupo restringe el acceso a la información solo a los usuarios autenticados. Para obtener más información sobre el acceso anónimo, vea [Identificadores de seguridad](/windows/desktop/SecAuthZ/security-identifiers) y [SID conocidos](/windows/desktop/SecAuthZ/well-known-sids).

Puede invalidar el valor predeterminado del sistema estableciendo la siguiente clave en el Registro en el valor 1:

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa** \\ **EveryoneIncludesAnonymous** = 1

Vea [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) y [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) para obtener información adicional sobre el acceso anónimo a la información de grupo al llamar a estas dos funciones.

## <a name="updates"></a>Actualizaciones

En el caso de las actualizaciones, la ACL predeterminada solo permite que los administradores de dominio y los operadores de cuenta escriban información. Una excepción es que los usuarios pueden cambiar su propia contraseña y establecer el campo de comentario \* \_ usri \_ usr. Otra excepción es que los operadores de cuenta no pueden modificar las cuentas de administración. Las funciones enumeradas a continuación se ven afectadas:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

Normalmente, los llamadores deben tener acceso de escritura a todo el objeto para que las llamadas a [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) y [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) se realizarán correctamente. Para un control de acceso más preciso, debe considerar el uso de ADSI. Para obtener más información sobre ADSI, [vea Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Para obtener más información sobre cómo controlar el acceso a objetos protegibles, [vea Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges)y [Securable Objects](/windows/desktop/SecAuthZ/securable-objects). Para obtener más información sobre cómo llamar a funciones que requieren privilegios de administrador, vea [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).

 

 