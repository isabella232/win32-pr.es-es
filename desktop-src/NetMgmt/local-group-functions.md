---
title: Funciones de grupo local
description: Un grupo local puede contener cuentas de usuario o cuentas de grupo global de uno o varios dominios. (Los grupos globales pueden contener usuarios de un solo dominio). Un grupo local comparte privilegios y derechos comunes solo dentro de su propio dominio.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d6521d067aada7d8c2d30ab4cdade8a41d6efa07e27a45098c21659ce88bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912065"
---
# <a name="local-group-functions"></a>Funciones de grupo local

Un *grupo local puede* contener cuentas de usuario o cuentas de grupo global de uno o varios dominios. (Los grupos globales pueden contener usuarios de un solo dominio). Un grupo local comparte privilegios y derechos comunes solo dentro de su propio dominio.

Las funciones de grupo local de administración de redes controlan los miembros de los grupos locales de forma que las funciones solo se puedan llamar localmente en el sistema en el que se define el grupo local. En una estación de trabajo o en un servidor que no es un controlador de dominio, solo puede usar un grupo local definido en ese sistema.

En Active Directory, los dominios que están en modo nativo, los grupos locales se denominan *grupos locales de dominio.* Los grupos locales de dominio están disponibles en todos los controladores de dominio, servidores miembros y estaciones de trabajo unidos al dominio. Active Directory de modo mixto se definen en el controlador de dominio principal y se replican en todos los demás controladores de dominio del dominio. Por lo tanto, un grupo local está disponible en todos los controladores de dominio dentro del dominio en el que se creó.

Las funciones de grupo local crean o eliminan grupos locales, y revisan o ajustan las pertenencias de los grupos locales. Estas funciones se enumeran a continuación.



| Función                                                   | Descripción                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crea un grupo local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Agrega uno o varios usuarios o grupos globales a un grupo local existente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Elimina un grupo local y quita todos los miembros existentes del grupo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Quita uno o varios miembros de un grupo local existente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Devuelve información sobre cada cuenta de grupo local de un servidor.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Devuelve información sobre una cuenta de grupo local determinada en un servidor. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Enumera todos los miembros de un grupo local especificado.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Establece información general sobre un grupo local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Asigna miembros a un grupo local.                                       |



 

Puede agregar un miembro a un grupo local especificando el identificador de seguridad (SID) del miembro. Para traducir un nombre de cuenta de miembro a un SID, llame a la [**función LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea)

Al crear un grupo local mediante una llamada a la [**función NetLocalGroupAdd,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) debe proporcionar un nombre de grupo local. Inicialmente, el grupo local no tiene miembros.

La información de la cuenta de grupo local está disponible en los niveles siguientes:

-   [**LOCALGROUP \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**LOCALGROUP \_ INFO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**LOCALGROUP \_ INFO \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

La información de pertenencia a grupos locales está disponible en los siguientes niveles de información:

-   [**LOCALGROUP \_ MEMBERS \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**INFORMACIÓN \_ 1 DE \_ LOS MIEMBROS DEL GRUPO \_ LOCAL**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**LOCALGROUP \_ MEMBERS \_ INFO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**LOCALGROUP \_ MEMBERS \_ INFO \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

Puede recuperar los nombres de los grupos locales a los que pertenece un usuario llamando a la función [**NetUserGetLocalGroups,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) especificando el siguiente nivel de información:

[**LOCALGROUP \_ USERS \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Para obtener más información, vea Funciones de grupo de [administración de red](group-functions.md).

Si está programando para Active Directory, es posible que pueda llamar a determinados métodos de interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr llamando a las funciones de grupo local de administración de redes. Para obtener más información, [**vea IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 