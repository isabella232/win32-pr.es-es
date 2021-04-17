---
description: Un identificador de seguridad (SID) es un valor único de longitud variable que se usa para identificar un administrador de confianza.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificadores de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368b2484cd8766aa7fa74c24679e82b10854e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652449"
---
# <a name="security-identifiers"></a>Identificadores de seguridad

Un [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) es un valor único de longitud variable que se usa para identificar un [Administrador de confianza](trustees.md). Cada cuenta tiene un SID único emitido por una autoridad, como un controlador de dominio de Windows, y almacenado en una base de datos de seguridad. Cada vez que un usuario inicia sesión, el sistema recupera el SID del usuario de la base de datos y lo coloca en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) para dicho usuario. El sistema utiliza el SID en el token de acceso para identificar al usuario en todas las interacciones posteriores con la seguridad de Windows. Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede usar de nuevo para identificar a otro usuario o grupo.

La seguridad de Windows usa SID en los siguientes elementos de seguridad:

-   En los [descriptores de seguridad](security-descriptors.md) para identificar el propietario de un objeto y el grupo principal
-   En [entradas de control de acceso](access-control-entries.md), para identificar el administrador de confianza para el que se permite, deniega o audita el acceso
-   En los [tokens de acceso](access-tokens.md), para identificar al usuario y a los grupos a los que pertenece el usuario

Además de los SID específicos de dominio que se crean de forma única y que se asignan a usuarios y grupos específicos, existen [SID conocidos](well-known-sids.md) que identifican grupos genéricos y usuarios genéricos. Por ejemplo, los SID conocidos, todos y todo el mundo, identifican un grupo que incluye a todos los usuarios.

La mayoría de las aplicaciones nunca necesitan trabajar con SID. Dado que los nombres de [SID conocidos](well-known-sids.md) pueden variar, debe usar las funciones para generar el SID a partir de constantes predefinidas en lugar de usar el nombre del SID conocido. Por ejemplo, la versión en Inglés de Estados Unidos del sistema operativo Windows tiene un SID conocido denominado "administradores integrados \\ " que puede tener un nombre diferente en las versiones internacionales del sistema. Para obtener un ejemplo que crea un SID conocido, vea [Buscar un SID en un token de acceso en C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Si necesita trabajar con SID, no los manipule directamente. En su lugar, utilice las siguientes funciones.



| Función                                                       | Descripción                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Asigna e inicializa un SID con el número de subautores especificado.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Convierte un SID en un formato de cadena adecuado para la presentación, el almacenamiento o el transporte.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Convierte un SID de formato de cadena en un SID válido y funcional.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia un SID de origen en un búfer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Comprueba la igualdad de dos valores de prefijo de SID. Un prefijo SID es todo el SID, excepto el último valor de subautoridad.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Comprueba la igualdad de dos SID. Deben coincidir exactamente para que se consideren iguales.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera un SID previamente asignado mediante la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera la longitud de un SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera un puntero a la autoridad del identificador de un SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera el tamaño del búfer necesario para almacenar un SID con un número de subautores especificado.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera un puntero a un subautor especificado en un SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera el número de subautores en un SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inicializa una estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) .                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Comprueba la validez de un SID comprobando que el número de revisión está dentro de un intervalo conocido y que el número de subautores es menor que el máximo. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera el SID correspondiente a un nombre de cuenta especificado.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera el nombre de cuenta que corresponde a un SID especificado.                                                                                           |



 

 

 
