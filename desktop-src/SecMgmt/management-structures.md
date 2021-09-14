---
description: Enumera las estructuras usadas con las API de administración de seguridad.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Estructuras de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073617"
---
# <a name="security-management-structures"></a>Estructuras de administración de seguridad

Esta sección contiene páginas de referencia para los siguientes grupos de estructuras:

-   [Estructuras de administración de directivas LSA](#lsa-policy-management-structures)
-   [Estructuras de datos adjuntos](#attachment-structures)
-   [Estructuras más seguras](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Estructuras de administración de directivas LSA

Las funciones de administración de directivas de la Autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) usan las siguientes estructuras.



| Estructura                                                                       | Descripción                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN DE \_ AUTENTICACIÓN DE LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Contiene información de autenticación para un dominio de confianza.                                                                                     |
| [**INFORMACIÓN DE ENUMERACIÓN \_ LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Contiene un puntero a un [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**ATRIBUTOS DE OBJETO LSA \_ \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Especifica los atributos de una conexión al [**objeto Policy.**](policy-object.md)                                                       |
| [**LISTA DE DOMINIOS \_ A LOS QUE SE HACE REFERENCIA LSA \_ \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Contiene información sobre los dominios a los que se hace referencia en una operación de búsqueda.                                                                      |
| [**NOMBRE TRADUCIDO DE LSA \_ \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Contiene información sobre la cuenta identificada por un SID.                                                                                   |
| [**SID TRADUCIDO \_ LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Contiene información sobre el SID que identifica una cuenta.                                                                                |
| [**\_SID2 TRADUCIDO DE LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Contiene información sobre el SID que identifica una cuenta.                                                                                |
| [**INFORMACIÓN DE CONFIANZA DE LSA \_ \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifica un dominio.                                                                                                                          |
| [**CADENA UNICODE LSA \_ \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Contiene una cadena y su información de longitud.                                                                                                 |
| [**INFORMACIÓN DE \_ DOMINIO DE LA CUENTA DE \_ \_ DIRECTIVA**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Se usa para establecer y consultar el nombre y el SID del dominio de cuenta del sistema.                                                                        |
| [**INFORMACIÓN DE \_ EVENTOS DE AUDITORÍA DE \_ \_ DIRECTIVAS**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Se usa para establecer y consultar las reglas de auditoría del sistema.                                                                                            |
| [**INFORMACIÓN DE \_ DOMINIO DNS \_ DE \_ DIRECTIVA**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Se usa para establecer y consultar información del Sistema de nombres de dominio (DNS) sobre el dominio principal asociado a un [**objeto Policy.**](policy-object.md) |
| [**INFORMACIÓN DEL \_ ROL DE SERVIDOR LSA \_ DE \_ \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Se usa para establecer y consultar el rol de un servidor LSA.                                                                                              |
| [**INFORMACIÓN DE \_ MODIFICACIÓN DE \_ DIRECTIVAS**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Se usa para consultar información sobre la hora de creación y la última modificación de la base de datos LSA.                                                  |
| [**INFORMACIÓN DE \_ LA CUENTA DE MANTENIMIENTO DE \_ \_ DIRECTIVAS**](policy-pd-account-info.md)                     | Obsoleto. Las estaciones de trabajo usan el nombre de la estación de trabajo seguido de $ como nombre de cuenta.                                                          |
| [**INFORMACIÓN DE \_ DOMINIO \_ PRINCIPAL DE \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Obsoleto. En **su lugar, use PolicyDnsDomainInformation y** la estructura POLICY DNS DOMAIN [**\_ \_ \_ INFO.**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)           |
| [**INFORMACIÓN \_ DE \_ AUTENTICACIÓN DE DOMINIO DE \_ CONFIANZA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Se usa para recuperar información de autenticación para un dominio de confianza.                                                                             |
| [**INFORMACIÓN \_ COMPLETA DE DOMINIO DE \_ \_ CONFIANZA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Se usa para recuperar información completa sobre un dominio de confianza.                                                                                 |
| [**INFORMACIÓN \_ DE DOMINIO DE CONFIANZA \_ \_ BÁSICA**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Información sobre un dominio de confianza. Esta estructura es idéntica a [**LSA \_ TRUST \_ INFORMATION**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**INFORMACIÓN \_ DE DOMINIO DE \_ \_ CONFIANZA, POR EJEMPLO,**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Se usa para recuperar información extendida sobre un dominio de confianza.                                                                                 |
| [**INFORMACIÓN DE \_ NOMBRE DE DOMINIO DE \_ \_ CONFIANZA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Se usa para consultar o establecer el nombre de un dominio de confianza.                                                                                            |
| [**INFORMACIÓN DE \_ CONTRASEÑA \_ DE CONFIANZA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Se usa para consultar o establecer la contraseña de un dominio de confianza.                                                                                       |
| [**INFORMACIÓN DE \_ DESPLAZAMIENTO \_ POSIX \_ DE CONFIANZA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Se usa para consultar o establecer el valor utilizado para generar identificadores de usuario y grupo de Posix.                                                             |



 

Los siguientes tipos de estructura están obsoletos o están reservados para su uso futuro:

-   **INFORMACIÓN DE \_ CONSULTA COMPLETA DE AUDITORÍA DE \_ \_ \_ DIRECTIVAS**
-   **INFORMACIÓN DE \_ CONJUNTO COMPLETO DE AUDITORÍA DE \_ \_ \_ DIRECTIVAS**
-   **INFORMACIÓN DEL \_ REGISTRO DE AUDITORÍA DE \_ \_ DIRECTIVAS**
-   **INFORMACIÓN DE \_ CUOTA PREDETERMINADA \_ DE \_ DIRECTIVA**
-   **INFORMACIÓN DE \_ ORIGEN DE RÉPLICA DE \_ \_ DIRECTIVA**
-   **INFORMACIÓN DE \_ CONTROLADORES DE \_ CONFIANZA**

## <a name="attachment-structures"></a>Estructuras de datos adjuntos

Las siguientes estructuras las usan los archivos DLL de datos adjuntos de configuración de seguridad y sus funciones compatibles. Estas estructuras se definen en Scesvc.h.



| Estructura                                                        | Descripción                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN DE CONFIGURACIÓN DE SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Contiene información de configuración para un servicio.                                                                                               |
| [**LÍNEA DE CONFIGURACIÓN \_ DE SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Contiene información sobre una línea de datos de configuración.                                                                                        |
| [**INFORMACIÓN DE ANÁLISIS DE SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Contiene la información de análisis.                                                                                                              |
| [**LÍNEA DE ANÁLISIS \_ DE SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Contiene la clave, el valor y la longitud del valor de una línea específica especificada por una [**estructura DE INFORMACIÓN DE ANÁLISIS \_ \_ DE SCESVC.**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) |
| [**INFORMACIÓN DE DEVOLUCIÓN DE LLAMADA SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Contiene un identificador de base de datos opaco y punteros de función de devolución de llamada para consultar, establecer y liberar información.                                          |



 

## <a name="safer-structures"></a>Estructuras más seguras

Las siguientes estructuras y tipos enumerados se usan en Safer. Se definen en WinSafer.h.



| Estructura                                                                | Descripción                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PROPIEDADES DE \_ CÓDIGO MÁS \_ SEGURAS**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Contiene información de imagen de código y criterios que se comprobarán en la imagen de código. Se pasa una matriz de estas estructuras a [**la función SaferIdentifyLevel.**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                                                                  |
| [**ENCABEZADO DE \_ IDENTIFICACIÓN \_ MÁS SEGURO**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Estructura de encabezado para [**las estructuras SAFER \_ PATHNAME \_ IDENTIFICATION**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), [**SAFER HASH \_ \_ IDENTIFICATION**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)y [**SAFER \_ URLZONE \_ IDENTIFICATION.**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) |
| [**IDENTIFICACIÓN DE \_ PATHNAME MÁS \_ SEGURA**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Contiene el nombre de ruta de acceso de una imagen de código que se va a comprobar.                                                                                                                                                                                                      |
| [**IDENTIFICACIÓN \_ DE HASH MÁS \_ SEGURA**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifica un hash de la imagen de código que se va a comprobar.                                                                                                                                                                                                      |
| [**IDENTIFICACIÓN \_ DE URLZONE MÁS \_ SEGURA**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Identifica la zona de dirección URL de origen de la imagen de código que se va a comprobar.                                                                                                                                                                                      |



 

 

 
