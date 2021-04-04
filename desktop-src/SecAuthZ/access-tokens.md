---
description: Un token de acceso es un objeto que describe el contexto de seguridad de un proceso o subproceso.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Tokens de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910621"
---
# <a name="access-tokens"></a>Tokens de acceso

Un [*token de acceso*](/windows/desktop/SecGloss/a-gly) es un objeto que describe el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de un [*proceso*](/windows/desktop/SecGloss/p-gly) o subproceso. La información de un token incluye la identidad y los privilegios de la cuenta de usuario asociada con el proceso o subproceso. Cuando un usuario inicia sesión, el sistema comprueba la contraseña del usuario comparándola con la información almacenada en una base de datos de seguridad. Si la contraseña se [*autentica*](/windows/desktop/SecGloss/a-gly), el sistema genera un token de acceso. Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

El sistema utiliza un token de acceso para identificar al usuario cuando un subproceso interactúa con un [objeto protegible](securable-objects.md) o intenta realizar una tarea del sistema que requiere privilegios. Los tokens de acceso contienen la siguiente información:

-   El [identificador de seguridad](security-identifiers.md) (SID) de la cuenta del usuario
-   SID para los grupos de los que el usuario es miembro
-   [*SID de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que identifica la sesión de [*Inicio*](/windows/desktop/SecGloss/l-gly) de sesión actual
-   Una lista de los [privilegios](privileges.md) mantenidos por el usuario o los grupos del usuario
-   Un SID de propietario
-   El SID para el grupo primario
-   [DACL](access-control-lists.md) predeterminada que el sistema utiliza cuando el usuario crea un objeto protegible sin especificar un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) .
-   El origen del token de acceso
-   Si el token es un token de [suplantación](client-impersonation.md) o [*principal*](/windows/desktop/SecGloss/p-gly)
-   Una lista opcional de [restricción de SID](restricted-tokens.md)
-   Niveles de suplantación actuales
-   Otras estadísticas

Cada proceso tiene un [*token principal*](/windows/desktop/SecGloss/p-gly) que describe el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) de la cuenta de usuario asociada al proceso. De forma predeterminada, el sistema utiliza el token principal cuando un subproceso del proceso interactúa con un objeto protegible. Además, un subproceso puede suplantar una cuenta de cliente. La suplantación permite que el subproceso interactúe con objetos protegibles mediante el contexto de seguridad del cliente. Un subproceso que suplanta a un cliente tiene un token principal y un [*token de suplantación*](/windows/desktop/SecGloss/i-gly).

Utilice la función [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) para recuperar un identificador para el token primario de un proceso. Utilice la función [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para recuperar un identificador para el token de suplantación de un subproceso. Para obtener más información, vea [suplantación](client-impersonation.md).

Puede utilizar las siguientes funciones para manipular los tokens de acceso.



| Función                                               | Descripción                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Cambia la información de grupo en un token de acceso.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Habilita o deshabilita los privilegios en un token de acceso. No concede nuevos privilegios ni revoca los existentes.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Determina si un SID especificado está habilitado en un token de acceso especificado.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Crea un nuevo token que es una versión restringida de un token existente. El token restringido puede tener SID deshabilitados, privilegios eliminados y una lista de SID restringidos. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Crea un nuevo token de suplantación que duplica un token existente.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Crea un nuevo token primario o un token de suplantación que duplica un token existente.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Recupera información sobre un token.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Determina si un token tiene una lista de SID restrictivos.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Recupera un identificador del token de acceso principal para un proceso.                                                                                                          |
| [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Recupera un identificador del token de acceso de suplantación para un subproceso.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Asigna o quita un token de suplantación para un subproceso.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Cambia el propietario, el grupo primario o la DACL predeterminada de un token.                                                                                                               |



 

Las funciones de token de acceso usan las siguientes estructuras para describir las partes de un token de acceso.



| Estructura                                            | Descripción                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**CONTROL de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Información que identifica un token de acceso.                                                          |
| [**\_DACL predeterminada de token \_**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | DACL predeterminada que el sistema utiliza en los descriptores de seguridad de los nuevos objetos creados por un subproceso. |
| [**grupos de TOKENs \_**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Especifica los SID y los atributos de los SID de grupo en un token de acceso.                               |
| [**propietario del TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | SID del propietario predeterminado para los descriptores de seguridad de los nuevos objetos.                                    |
| [**\_grupo principal de tokens \_**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | SID de grupo principal predeterminado para los descriptores de seguridad de los nuevos objetos.                            |
| [**privilegios de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Los privilegios asociados a un token de acceso. También determina si los privilegios están habilitados.   |
| [**origen de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Origen de un token de acceso.                                                                        |
| [**estadísticas de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Estadísticas asociadas a un token de acceso.                                                           |
| [**usuario de TOKEN \_**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | SID del usuario asociado a un token de acceso.                                                  |



 

Las funciones de token de acceso usan los siguientes tipos de enumeración.



| Tipo de enumeración                                             | Especifica                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_clase de información de token \_**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifica el tipo de información que se va a establecer o recuperar de un token de acceso. |
| [**tipo de TOKEN \_**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifica un token de acceso como un token de suplantación o principal.                 |



 

 

 
