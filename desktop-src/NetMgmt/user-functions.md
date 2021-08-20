---
title: Funciones de usuario
description: Las funciones de usuario de administración de red controlan la cuenta de un usuario en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. Las funciones de usuario se enumeran a continuación.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796821"
---
# <a name="user-functions"></a>Funciones de usuario

Las funciones de usuario de administración de red controlan la cuenta de un usuario en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. Las funciones de usuario se enumeran a continuación.



| Función                                               | Descripción                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Agrega una cuenta de usuario y asigna un nivel de contraseña y privilegios.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Cambia la contraseña de un usuario para un dominio o servidor de red especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Elimina una cuenta de usuario del servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Enumera todas las cuentas de usuario de un servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Devuelve una lista de nombres de grupo globales a los que pertenece un usuario.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Devuelve información sobre una cuenta de usuario determinada en un servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Devuelve una lista de nombres de grupo local a los que pertenece un usuario.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Establece las pertenencias a grupos globales para una cuenta de usuario especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Establece la contraseña y otros elementos de una cuenta de usuario.             |



 

Cada usuario o aplicación que accede a los recursos de red debe tener una cuenta en la base de datos de seguridad. Los servicios de directorio usan esta cuenta para comprobar que el usuario o la aplicación tienen permiso para conectarse a un recurso. Cuando un usuario o una aplicación solicitan acceso a un recurso, el sistema de seguridad de Windows comprueba si hay una cuenta de usuario o cuenta de grupo adecuada para permitir el acceso.

Una vez que quite una cuenta de usuario mediante una llamada a la función [**NetUserDel,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) el usuario ya no podrá acceder al servidor excepto mediante la cuenta de invitado.

Dado que la contraseña de un usuario es confidencial, la función [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) o la [**función NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) no la devuelven. La contraseña se asigna inicialmente cuando se llama a [**NetUserAdd.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)

La información de la cuenta de usuario está disponible en los niveles siguientes:

-   [**USER \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**USER \_ INFO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**USER \_ INFO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**INFORMACIÓN \_ DEL \_ USUARIO 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**INFORMACIÓN \_ DE USUARIO \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**USER \_ INFO \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**USER \_ INFO \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**USER \_ INFO \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**USER \_ INFO \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**USER \_ INFO \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**USER \_ INFO \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Además, los siguientes niveles de información son válidos cuando se llama a la [**función NetUserSetInfo:**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

-   [**USER \_ INFO \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**USER \_ INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**USER \_ INFO \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**USER \_ INFO \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**INFORMACIÓN \_ DE \_ USUARIO 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**USER \_ INFO \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**USER \_ INFO \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**USER \_ INFO \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**USER \_ INFO \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**USER \_ INFO \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**USER \_ INFO \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**USER \_ INFO \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**USER \_ INFO \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**INFORMACIÓN \_ DE \_ USUARIO 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**INFORMACIÓN \_ DE \_ USUARIO 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**INFORMACIÓN \_ DE \_ USUARIO 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Las siguientes funciones permiten a las aplicaciones comprobar el cumplimiento de contraseñas.



| Función                                                               | Descripción                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria asignada por la [**función NetValidatePasswordPolicy.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Comprueba que las contraseñas cumplen los requisitos de complejidad, edad, longitud mínima y reutilización del historial.            |



 

Si está programando para Active Directory, puede llamar a determinados métodos de la interfaz de servicio (ADSI) de Active Directory para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de usuario de administración de red. Para obtener más información, [**vea IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) and [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 