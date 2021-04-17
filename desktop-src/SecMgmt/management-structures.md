---
description: Enumera las estructuras utilizadas con las API de administración de seguridad.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Estructuras de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668317"
---
# <a name="security-management-structures"></a>Estructuras de administración de seguridad

Esta sección contiene páginas de referencia para los siguientes grupos de estructuras:

-   [Estructuras de administración de directivas de LSA](#lsa-policy-management-structures)
-   [Estructuras de datos adjuntos](#attachment-structures)
-   [Estructuras más seguras](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Estructuras de administración de directivas de LSA

Las siguientes estructuras las utilizan las funciones de administración de directivas de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA).



| Estructura                                                                       | Descripción                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_información de autenticación de LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Contiene información de autenticación para un dominio de confianza.                                                                                     |
| [**\_información de enumeración de LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Contiene un puntero a un [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**\_atributos de objeto LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Especifica los atributos de una conexión al objeto de [**Directiva**](policy-object.md) .                                                       |
| [**lista de dominios a los \_ que se hace referencia LSA \_ \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Contiene información acerca de los dominios a los que se hace referencia en una operación de búsqueda.                                                                      |
| [**\_nombre traducido de LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Contiene información acerca de la cuenta identificada por un SID.                                                                                   |
| [**\_SID traducido de LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Contiene información acerca del SID que identifica una cuenta.                                                                                |
| [**\_SID2 traducido de LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Contiene información acerca del SID que identifica una cuenta.                                                                                |
| [**\_información de confianza de LSA \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifica un dominio.                                                                                                                          |
| [**\_cadena Unicode \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Contiene una cadena y su información de longitud.                                                                                                 |
| [**\_información de \_ dominio de cuenta de directiva \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Se utiliza para establecer y consultar el nombre y el SID del dominio de la cuenta del sistema.                                                                        |
| [**\_información de \_ eventos de auditoría de directiva \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Se usa para establecer y consultar las reglas de auditoría del sistema.                                                                                            |
| [**\_información del \_ dominio \_ DNS de la Directiva**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Se utiliza para establecer y consultar información del sistema de nombres de dominio (DNS) sobre el dominio principal asociado a un objeto de [**Directiva**](policy-object.md) . |
| [**DIRECTIVA \_ LSA \_ de \_ rol de servidor \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Se usa para establecer y consultar el rol de un servidor LSA.                                                                                              |
| [**\_información de modificación de directiva \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Se utiliza para consultar información acerca de la hora de creación y la última modificación de la base de datos LSA.                                                  |
| [**DIRECTIVA \_ PD \_ información de cuenta \_**](policy-pd-account-info.md)                     | Obsoleto. Las estaciones de trabajo usan el nombre de la estación de trabajo seguido de un $ como nombre de cuenta.                                                          |
| [**\_información del \_ dominio \_ principal de la Directiva**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Obsoleto. En su lugar, use **PolicyDnsDomainInformation** y la estructura de [**\_ \_ \_ información de dominio DNS**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) de la Directiva.           |
| [**\_información de \_ autenticación de dominio de confianza \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Se usa para recuperar información de autenticación para un dominio de confianza.                                                                             |
| [**\_ \_ información completa del dominio de confianza \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Se usa para recuperar información completa sobre un dominio de confianza.                                                                                 |
| [**\_ \_ información básica de dominios de confianza \_**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Información sobre un dominio de confianza. Esta estructura es idéntica a [**la \_ \_ información de confianza de LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**información de dominio de confianza \_ \_ \_ ex**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Se utiliza para recuperar información extendida sobre un dominio de confianza.                                                                                 |
| [**\_información del \_ nombre de dominio de confianza \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Se usa para consultar o establecer el nombre de un dominio de confianza.                                                                                            |
| [**\_información de contraseña de confianza \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Se usa para consultar o establecer la contraseña de un dominio de confianza.                                                                                       |
| [**\_información de \_ desplazamiento de POSIX de confianza \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Se utiliza para consultar o establecer el valor utilizado para generar identificadores de usuario y de grupo de POSIX.                                                             |



 

Los tipos de estructura siguientes están obsoletos o se reservan para uso futuro:

-   **\_información de \_ \_ consulta completa de auditoría \_ de Directiva**
-   **\_información de \_ \_ conjunto completo de auditoría \_ de Directiva**
-   **\_información de \_ registro de auditoría de directiva \_**
-   **\_información de \_ cuota \_ predeterminada de Directiva**
-   **\_información de \_ origen de réplica de directiva \_**
-   **\_información de los controladores de confianza \_**

## <a name="attachment-structures"></a>Estructuras de datos adjuntos

Los archivos dll de datos adjuntos de configuración de seguridad usan las siguientes estructuras y sus funciones auxiliares. Estas estructuras se definen en scesvc. h.



| Estructura                                                        | Descripción                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_información de configuración de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Contiene información de configuración de un servicio.                                                                                               |
| [**\_línea de configuración de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Contiene información sobre una línea de datos de configuración.                                                                                        |
| [**\_información de análisis de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Contiene la información de análisis.                                                                                                              |
| [**\_línea de análisis de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Contiene la clave, el valor y la longitud del valor de una línea específica especificada por una estructura de [**\_ \_ información de análisis de SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) . |
| [**información de devolución de llamada de SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Contiene un identificador de base de datos opaco y punteros de función de devolución de llamada para consultar, establecer y liberar información.                                          |



 

## <a name="safer-structures"></a>Estructuras más seguras

Las siguientes estructuras y tipos enumerados se usan de un tipo más seguro. Se definen en WinSafer. h.



| Estructura                                                                | Descripción                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_propiedades de código más seguras \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Contiene información de imagen de código y los criterios que se van a comprobar en la imagen de código. Una matriz de estas estructuras se pasa a la función [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) .                                                                  |
| [**\_encabezado de identificación más seguro \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Estructura de encabezado para la [**\_ \_ identificación de ruta de seguridad más segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), [**\_ \_ identificación de hash segura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)y estructuras de [**\_ \_ identificación de URLZONE más seguras**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) . |
| [**\_identificación de ruta de seguridad más segura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Contiene el nombre de la ruta de acceso de una imagen de código que se va a comprobar.                                                                                                                                                                                                      |
| [**\_identificación de hash más segura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifica un hash de la imagen de código que se va a comprobar.                                                                                                                                                                                                      |
| [**\_identificación de URLZONE más segura \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Identifica la zona URL de origen de la imagen de código que se va a comprobar.                                                                                                                                                                                      |



 

 

 
