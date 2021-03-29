---
description: Enumera las enumeraciones usadas en las API de autenticación.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumeraciones de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809350"
---
# <a name="authentication-enumerations"></a>Enumeraciones de autenticación

Las enumeraciones de autenticación se clasifican según el uso de la manera siguiente:

-   [Enumeraciones de administración de credenciales](#credentials-management-enumerations)
-   [Enumeraciones de LSA](#lsa-enumerations)
-   [Enumeraciones de proveedor de red](#network-provider-enumerations)
-   [Enumeraciones del proveedor de compatibilidad para seguridad de credenciales (CredSSP)](#credential-security-support-provider-credssp-enumerations)
-   [Otras enumeraciones](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumeraciones de administración de credenciales

La administración de credenciales utiliza las enumeraciones siguientes.



| Enumeración                                            | Descripción                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de serialización CRED \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contiene los tipos de credenciales cuyas referencias se pueden calcular por [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) o cuyas referencias no se calculan mediante [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).<br/> |
| [**\_tipo de protección CRED \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Especifica el contexto de seguridad en el que las credenciales se cifran cuando se usa la función [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) .<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumeraciones de LSA

LSA usa las enumeraciones siguientes.



| Enumeración                                                                                   | Descripción                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de envío de inicio de sesión de KERB \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Muestra el tipo de inicio de sesión que se solicita.<br/>                                                                                                                                                                                                                  |
| [**\_tipo de \_ búfer de Perfil de Kerb \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Muestra el tipo de Perfil de inicio de sesión devuelto.<br/>                                                                                                                                                                                                                 |
| [**\_tipo de \_ mensaje de protocolo Kerb \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Enumera los tipos de mensajes que se pueden enviar al paquete de autenticación de [*Kerberos*](/windows/desktop/SecGloss/k-gly) mediante una llamada a [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**\_tipo de \_ registro de colisión de confianza de bosque LSA \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Define los tipos de colisión que pueden producirse entre los registros de confianza de bosque de LSA.<br/>                                                                                                                                                                           |
| [**\_tipo de \_ registro de confianza de bosque LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Define el tipo de un registro de confianza de bosque LSA.<br/>                                                                                                                                                                                                           |
| [**\_tipo de \_ información de token LSA \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Especifica los niveles de información que se pueden incluir en un token de inicio de sesión.<br/>                                                                                                                                                                                |
| [**Tipo de envío de inicio de sesión de MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Muestra el tipo de inicio de sesión que se solicita.<br/>                                                                                                                                                                                                                  |
| [**\_Tipo de \_ búfer de perfil \_ \_ de MSV1 0**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Muestra el tipo de Perfil de inicio de sesión devuelto.<br/>                                                                                                                                                                                                                 |
| [**\_Tipo de \_ mensaje de protocolo MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Enumera los tipos de mensajes que se pueden enviar al [paquete de \_ autenticación MSV1 0](msv1-0-authentication-package.md) llamando a [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**\_clase de \_ información de dominio de directiva \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Define el tipo de información de dominio de directiva.<br/>                                                                                                                                                                                                            |
| [**tipo de inicio de sesión de seguridad \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica el tipo de inicio de sesión solicitado por un proceso de inicio de sesión.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumeraciones de proveedor de red

El proveedor de red utiliza las enumeraciones siguientes.



| Enumeración                                                                       | Descripción                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_clase de \_ información AMPLIAda SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo de enumeración que especifica el tipo de información que se va a establecer u obtener para un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**\_tipo de nombre SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valor de enumeración que especifica el tipo de nombre especificado para una cuenta.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumeraciones del proveedor de compatibilidad para seguridad de credenciales (CredSSP)

CredSSP usa las enumeraciones siguientes.



| Enumeración                                          | Descripción                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_tipo de envío de CREDSPP \_**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Especifica el tipo de credenciales especificado por una estructura [**\_ CRED de CREDSSP**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) .<br/> |



 

## <a name="other-enumerations"></a>Otras enumeraciones

Estas son las otras enumeraciones usadas por la autenticación de.



| Enumeración                                                   | Descripción                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo de identidad \_**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Especifica el tipo de identidades que se va a enumerar.<br/>                                                                                                                                                                  |
| [**Tipo de envío de inicio de sesión de PKU2U \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica el tipo de mensaje de inicio de sesión pasado en una estructura de [**\_ Inicio de \_ \_ sesión S4U del certificado PKU2U**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) .<br/>                                                                                |
| [**SECPKG \_ ATTR \_ LCT \_ status**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica si el token de la llamada más reciente a la función [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) es el último token del cliente.<br/>                               |
| [**SECPKG \_ CRED ( \_ clase)**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica el tipo de credencial que se usa en un contexto de cliente. La enumeración de la [**\_ \_ clase SECPKG CRED**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) se usa en la estructura [**\_ CredInfo de SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) .<br/> |



 

 

