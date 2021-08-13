---
description: Un identificador de seguridad (SID) es un valor único de longitud variable que se usa para identificar a un administrador de confianza.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificadores de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6acaaeacfbc77b2dc814062c4254c5f08e58869e0b6d8b2fbb64e8511dc31e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413495"
---
# <a name="security-identifiers"></a>Identificadores de seguridad

Un [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) es un valor único de longitud variable que se usa para identificar a un administrador de [confianza.](trustees.md) Cada cuenta tiene un SID único emitido por una autoridad, como un controlador Windows dominio, y almacenado en una base de datos de seguridad. Cada vez que un usuario inicia sesión, el sistema recupera el SID de ese usuario de la base de datos y lo coloca en el [*token*](/windows/desktop/SecGloss/a-gly) de acceso para ese usuario. El sistema usa el SID en el token de acceso para identificar al usuario en todas las interacciones posteriores con Windows seguridad. Cuando se ha usado un SID como identificador único de un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.

Windows seguridad usa SID en los siguientes elementos de seguridad:

-   En [descriptores de seguridad](security-descriptors.md) para identificar el propietario de un objeto y un grupo principal
-   En [las entradas de control de](access-control-entries.md)acceso , para identificar al administrador de confianza para el que se permite, deniega o audita el acceso.
-   En [los tokens de](access-tokens.md)acceso , para identificar el usuario y los grupos a los que pertenece el usuario

Además de los SID específicos de dominio creados de forma única asignados a usuarios y grupos [específicos,](well-known-sids.md) hay SID conocidos que identifican grupos genéricos y usuarios genéricos. Por ejemplo, los conocidos SID, Todos y Mundo, identifican un grupo que incluye a todos los usuarios.

La mayoría de las aplicaciones nunca necesitan trabajar con SID. Dado que los nombres de los [SID](well-known-sids.md) conocidos pueden variar, debe usar las funciones para compilar el SID a partir de constantes predefinidas en lugar de usar el nombre del SID conocido. Por ejemplo, la versión en inglés de Ee. UU. del sistema operativo Windows tiene un SID conocido denominado "Administradores BUILTIN" que podría tener un nombre diferente en las versiones internacionales del \\ sistema. Para obtener un ejemplo que compila un SID conocido, vea Buscar un SID en un [token de acceso en C++.](searching-for-a-sid-in-an-access-token-in-c--.md)

Si necesita trabajar con SID, no los manipule directamente. En su lugar, use las siguientes funciones.



| Función                                                       | Descripción                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Asigna e inicializa un SID con el número especificado de subautoridades.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Convierte un SID en un formato de cadena adecuado para su presentación, almacenamiento o transporte.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Convierte un SID con formato de cadena en un SID funcional válido.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia un SID de origen en un búfer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Comprueba la igualdad de dos valores de prefijo SID. Un prefijo SID es todo el SID, excepto el último valor de subautoridad.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Comprueba la igualdad de dos SID. Deben coincidir exactamente para que se consideren iguales.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera un SID asignado previamente mediante la [**función AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera la longitud de un SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera un puntero a la autoridad de identificador de un SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera el tamaño del búfer necesario para almacenar un SID con un número especificado de subautoridades.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera un puntero a una subautoridad especificada en un SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera el número de subautoridades de un SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inicializa una estructura [**SID.**](/windows/desktop/api/Winnt/ns-winnt-sid)                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Comprueba la validez de un SID comprobando que el número de revisión está dentro de un intervalo conocido y que el número de subautoridades es menor que el máximo. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera el SID que corresponde a un nombre de cuenta especificado.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera el nombre de cuenta que corresponde a un SID especificado.                                                                                           |



 

 

 
