---
title: Funciones de grupo local
description: Un grupo local puede contener cuentas de usuario o cuentas de grupo globales de uno o más dominios. (Los grupos globales pueden contener usuarios de un solo dominio). Un grupo local comparte privilegios y derechos comunes solo dentro de su propio dominio.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792010"
---
# <a name="local-group-functions"></a>Funciones de grupo local

Un *grupo local* puede contener cuentas de usuario o cuentas de grupo globales de uno o más dominios. (Los grupos globales pueden contener usuarios de un solo dominio). Un grupo local comparte privilegios y derechos comunes solo dentro de su propio dominio.

Las funciones de grupo local de administración de redes controlan a los miembros de los grupos locales de una forma en la que solo se puede llamar a las funciones localmente en el sistema en el que se define el grupo local. En una estación de trabajo, o en un servidor que no sea un controlador de dominio, solo puede usar un grupo local definido en ese sistema.

En Active Directory, los dominios que están en modo nativo, los grupos locales se denominan *grupos locales de dominio*. Los grupos locales de dominio están disponibles en todos los controladores de dominio, servidores miembro y estaciones de trabajo Unidas al dominio. Active Directory dominios de modo mixto se definen en el controlador de dominio principal y se replican en todos los demás controladores de dominio del dominio. Por lo tanto, un grupo local está disponible en todos los controladores de dominio del dominio en el que se creó.

Las funciones de grupo local crean o eliminan grupos locales y revisan o ajustan las pertenencias de grupos locales. Estas funciones se muestran a continuación.



| Función                                                   | Descripción                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crea un grupo local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Agrega uno o más usuarios o grupos globales a un grupo local existente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Elimina un grupo local, quitando todos los miembros existentes del grupo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Quita uno o más miembros de un grupo local existente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Devuelve información acerca de cada cuenta de grupo local en un servidor.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Devuelve información acerca de una cuenta de grupo local determinada en un servidor. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Enumera todos los miembros de un grupo local especificado.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Establece información general sobre un grupo local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Asigna miembros a un grupo local.                                       |



 

Puede Agregar un miembro a un grupo local especificando el identificador de seguridad (SID) del miembro. Para traducir el nombre de una cuenta de miembro a un SID, llame a la función [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .

Al crear un grupo local llamando a la función [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) , debe proporcionar un nombre de grupo local. Inicialmente, el grupo local no tiene miembros.

La información de la cuenta de grupo local está disponible en los siguientes niveles:

-   [**Información del LOCALGROUP \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**Información del LOCALGROUP \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**Información del LOCALGROUP \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

La información de pertenencia al grupo local está disponible en los siguientes niveles de información:

-   [**Miembros del LOCALGROUP ( \_ \_ información) \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**Miembros del LOCALGROUP \_ \_ información \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**Miembros del LOCALGROUP de \_ \_ información \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**Miembros del LOCALGROUP, \_ \_ información \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

Puede recuperar los nombres de los grupos locales a los que pertenece un usuario mediante una llamada a la función [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) , especificando el siguiente nivel de información:

[**Información de usuarios de LOCALGROUP \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Para obtener más información, vea funciones de [Grupo](group-functions.md)de administración de red.

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de grupo local de administración de redes. Para obtener más información, vea [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 