---
title: Requisitos para las funciones de administración de redes en controladores de Dominio de Active Directory
description: Si llama a una de las funciones de administración de red que se enumeran en este tema en un controlador de dominio que ejecuta Active Directory, se permite o se deniega el acceso a un objeto protegible en función de la lista de control de acceso (ACL) para el objeto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904661"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisitos para las funciones de administración de redes en controladores de Dominio de Active Directory

Si llama a una de las funciones de administración de red que se enumeran en este tema en un controlador de dominio que ejecuta Active Directory, se permite o se deniega el acceso a un [objeto protegible](/windows/desktop/SecAuthZ/securable-objects) en función de la [lista de control de acceso](/windows/desktop/SecAuthZ/access-control-lists) (ACL) para el objeto. (Las ACL se especifican en el directorio).

Los diferentes requisitos de acceso se aplican a las consultas de información y a las actualizaciones de información.

## <a name="queries"></a>Consultas

En el caso de las consultas, la ACL predeterminada permite a todos los usuarios autenticados y a los miembros del grupo "[acceso compatible con versiones anteriores a Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)" leer y enumerar la información. Las funciones que se enumeran a continuación se ven afectadas:

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (solo niveles 1 y 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (solo niveles 2 y 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

El acceso anónimo a la información de grupo requiere que el usuario anónimo se agregue explícitamente al grupo "acceso compatible con versiones anteriores a Windows 2000". Esto se debe a que los tokens anónimos no incluyen el SID del grupo todos.

**Windows 2000:** De forma predeterminada, el grupo "acceso compatible con versiones anteriores de 2000 Windows" incluye a todos los usuarios como miembros. Esto habilita el acceso anónimo (inicio de sesión anónimo) a la información si el sistema permite el acceso anónimo. Los administradores pueden quitar todos los miembros del grupo "acceso compatible con versiones anteriores a Windows 2000" en cualquier momento. Al quitar todos los miembros del grupo, solo se restringe el acceso a la información a los usuarios autenticados. Para obtener más información sobre el acceso anónimo, vea [identificadores de seguridad](/windows/desktop/SecAuthZ/security-identifiers) y [SID conocidos](/windows/desktop/SecAuthZ/well-known-sids).

Puede invalidar el valor predeterminado del sistema estableciendo la siguiente clave en el registro en el valor 1:

**HKEY \_ \_Sistema del equipo local ( \\ \\ control CurrentControlSet) \\ \\ LSA** \\ **EveryoneIncludesAnonymous** = 1

Vea [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) y [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) para obtener información adicional sobre el acceso anónimo a la información de grupo cuando se llama a estas dos funciones.

## <a name="updates"></a>Actualizaciones

En el caso de las actualizaciones, la ACL predeterminada solo permite que los administradores de dominio y los operadores de cuentas escriban información. Una excepción es que los usuarios pueden cambiar su propia contraseña y establecer el \* \_ campo de comentario Usri usr \_ . Otra excepción es que los operadores de cuentas no pueden modificar las cuentas de administración. Las funciones que se enumeran a continuación se ven afectadas:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

Normalmente, los autores de la llamada deben tener acceso de escritura a todo el objeto para que las llamadas a [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) y [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) se realicen correctamente. Para un control de acceso más preciso, considere la posibilidad de usar ADSI. Para obtener más información acerca de ADSI, consulte [Active Directory interfaces de servicio](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control), [privilegios](/windows/desktop/SecAuthZ/privileges)y [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects). Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

 

 