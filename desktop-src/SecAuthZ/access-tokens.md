---
description: Un token de acceso es un objeto que describe el contexto de seguridad de un proceso o subproceso.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Tokens de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073744"
---
# <a name="access-tokens"></a>Tokens de acceso

Un [*token de*](/windows/desktop/SecGloss/a-gly) acceso es un objeto que describe el contexto de [*seguridad*](/windows/desktop/SecGloss/s-gly) de un [*proceso*](/windows/desktop/SecGloss/p-gly) o subproceso. La información de un token incluye la identidad y los privilegios de la cuenta de usuario asociada al proceso o subproceso. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándolo con la información almacenada en una base de datos de seguridad. Si se autentica la [*contraseña,*](/windows/desktop/SecGloss/a-gly)el sistema genera un token de acceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

El sistema usa un token de acceso para identificar al usuario cuando un subproceso interactúa con un objeto [protegible](securable-objects.md) o intenta realizar una tarea del sistema que requiere privilegios. Los tokens de acceso contienen la siguiente información:

-   Identificador [de seguridad](security-identifiers.md) (SID) de la cuenta del usuario
-   SID para los grupos de los que el usuario es miembro
-   SID [*de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que identifica la sesión de inicio de sesión [*actual*](/windows/desktop/SecGloss/l-gly)
-   Una lista de los [privilegios que](privileges.md) tiene el usuario o los grupos del usuario.
-   SID de propietario
-   SID del grupo principal
-   La [DACL predeterminada](access-control-lists.md) que usa el sistema cuando el usuario crea un objeto protegible sin especificar un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)
-   Origen del token de acceso
-   Si el token es un [*token principal*](/windows/desktop/SecGloss/p-gly) o [de suplantación](client-impersonation.md)
-   Lista opcional de [SID restricting](restricted-tokens.md)
-   Niveles de suplantación actuales
-   Otras estadísticas

Cada proceso tiene un [*token principal*](/windows/desktop/SecGloss/p-gly) que describe el contexto [*de*](/windows/desktop/SecGloss/s-gly) seguridad de la cuenta de usuario asociada al proceso. De forma predeterminada, el sistema usa el token principal cuando un subproceso del proceso interactúa con un objeto protegible. Además, un subproceso puede suplantar una cuenta de cliente. La suplantación permite que el subproceso interactúe con objetos protegibles mediante el contexto de seguridad del cliente. Un subproceso que suplanta a un cliente tiene un token principal y un [*token de suplantación.*](/windows/desktop/SecGloss/i-gly)

Use la [**función OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para recuperar un identificador para el token principal de un proceso. Use la [**función OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para recuperar un identificador para el token de suplantación de un subproceso. Para obtener más información, vea [Suplantación.](client-impersonation.md)

Puede usar las siguientes funciones para manipular los tokens de acceso.



| Función                                               | Descripción                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Cambia la información del grupo en un token de acceso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Habilita o deshabilita los privilegios en un token de acceso. No concede nuevos privilegios ni revoca los existentes.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina si un SID especificado está habilitado en un token de acceso especificado.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Crea un nuevo token que es una versión restringida de un token existente. El token restringido puede tener SID deshabilitados, privilegios eliminados y una lista de SID restringidos. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Crea un nuevo token de suplantación que duplica un token existente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Crea un nuevo token principal o token de suplantación que duplica un token existente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera información sobre un token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina si un token tiene una lista de SID de restricción.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera un identificador del token de acceso principal para un proceso.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera un identificador del token de acceso de suplantación para un subproceso.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Asigna o quita un token de suplantación para un subproceso.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Cambia el propietario, el grupo principal o la DACL predeterminada de un token.                                                                                                               |



 

Las funciones de token de acceso usan las estructuras siguientes para describir las partes de un token de acceso.



| Estructura                                            | Descripción                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**CONTROL DE \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Información que identifica un token de acceso.                                                          |
| [**DACL \_ PREDETERMINADA \_ DEL TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | La DACL predeterminada que el sistema usa en los descriptores de seguridad de los nuevos objetos creados por un subproceso. |
| [**GRUPOS DE \_ TOKENS**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Especifica los SID y atributos de los SID de grupo en un token de acceso.                               |
| [**PROPIETARIO DEL \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | SID de propietario predeterminado para los descriptores de seguridad de objetos nuevos.                                    |
| [**GRUPO \_ PRINCIPAL DE \_ TOKENS**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | SID de grupo principal predeterminado para los descriptores de seguridad de nuevos objetos.                            |
| [**PRIVILEGIOS \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Privilegios asociados a un token de acceso. También determina si los privilegios están habilitados.   |
| [**ORIGEN DEL \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Origen de un token de acceso.                                                                        |
| [**ESTADÍSTICAS \_ DE TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Estadísticas asociadas a un token de acceso.                                                           |
| [**USUARIO DE \_ TOKEN**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | SID del usuario asociado a un token de acceso.                                                  |



 

Las funciones de token de acceso usan los siguientes tipos de enumeración.



| Tipo de enumeración                                             | Especifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**CLASE DE \_ INFORMACIÓN DE \_ TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica el tipo de información que se establece o recupera de un token de acceso. |
| [**TIPO DE \_ TOKEN**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica un token de acceso como un token principal o de suplantación.                 |



 

 

 
