---
title: Funciones de usuario
description: Las funciones de usuario de administración de red controlan la cuenta de un usuario en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. A continuación se enumeran las funciones de usuario.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a3349673d09e42fbfe7a5dc949d1bcff53b828
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676467"
---
# <a name="user-functions"></a>Funciones de usuario

Las funciones de usuario de administración de red controlan la cuenta de un usuario en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. A continuación se enumeran las funciones de usuario.



| Función                                               | Descripción                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Agrega una cuenta de usuario y asigna una contraseña y un nivel de privilegios.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Cambia la contraseña de un usuario para un dominio o servidor de red especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Elimina una cuenta de usuario del servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Muestra todas las cuentas de usuario en un servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Devuelve una lista de nombres de grupos globales a los que pertenece un usuario.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Devuelve información acerca de una cuenta de usuario determinada en un servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Devuelve una lista de nombres de grupos locales a los que pertenece un usuario.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Establece la pertenencia a grupos globales para una cuenta de usuario especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Establece la contraseña y otros elementos de una cuenta de usuario.             |



 

Cada usuario o aplicación que tiene acceso a los recursos de red debe tener una cuenta en la base de datos de seguridad. Los servicios de directorio usan esta cuenta para comprobar que el usuario o la aplicación tienen permiso para conectarse a un recurso. Cuando un usuario o una aplicación solicita acceso a un recurso, el sistema de seguridad de Windows comprueba si existe una cuenta de usuario o de grupo adecuada para permitir el acceso.

Una vez que se quita una cuenta de usuario mediante una llamada a la función [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) , el usuario ya no puede tener acceso al servidor excepto mediante la cuenta invitado.

Dado que la contraseña de un usuario es confidencial, no la devuelve la función [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) o la función [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) . La contraseña se asigna inicialmente cuando se llama a [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

La información de la cuenta de usuario está disponible en los siguientes niveles:

-   [**Información de usuario \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**Información de usuario \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**Información de usuario \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**Información de usuario \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**Información de usuario \_ \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**Información de usuario \_ \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**Información de usuario \_ \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**Información de usuario \_ \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**Información de usuario \_ \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**Información de usuario \_ \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**Información de usuario \_ \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Además, los siguientes niveles de información son válidos cuando se llama a la función [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) :

-   [**Información de usuario \_ \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**Información de usuario \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**Información de usuario \_ \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**Información de usuario \_ \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**Información de usuario \_ \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**Información de usuario \_ \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**Información de usuario \_ \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**Información de usuario \_ \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**Información de usuario \_ \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**Información de usuario \_ \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**Información de usuario \_ \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**Información de usuario \_ \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**Información de usuario \_ \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**Información de usuario \_ \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**Información de usuario \_ \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**Información de usuario \_ \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Las siguientes funciones permiten a las aplicaciones comprobar el cumplimiento de contraseñas.



| Función                                                               | Descripción                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria asignada por la función [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) . |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Comprueba que las contraseñas cumplan los requisitos de complejidad, antigüedad, longitud mínima y reutilización del historial.            |



 

Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz de servicio Active Directory (ADSI) para lograr la misma funcionalidad que puede lograr mediante una llamada a las funciones de usuario de administración de redes. Para obtener más información, vea [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) y [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 