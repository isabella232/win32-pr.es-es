---
description: Enumera las enumeraciones usadas en las API de autenticación.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumeraciones de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc42553074b79726c9d1b70bfc6292f4acf44df225fa1f86c7f7a28289ec8ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101325"
---
# <a name="authentication-enumerations"></a>Enumeraciones de autenticación

Las enumeraciones de autenticación se clasifican según el uso como se muestra a continuación:

-   [Enumeraciones de administración de credenciales](#credentials-management-enumerations)
-   [Enumeraciones LSA](#lsa-enumerations)
-   [Enumeraciones de proveedor de red](#network-provider-enumerations)
-   [Enumeraciones del proveedor de compatibilidad con seguridad de credenciales (CredSSP)](#credential-security-support-provider-credssp-enumerations)
-   [Otras enumeraciones](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumeraciones de administración de credenciales

Administración de credenciales usa las enumeraciones siguientes.



| Enumeración                                            | Descripción                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ SERIALIZACIÓN \_ CRED**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contiene los tipos de credenciales que [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) puede serializar o desmarshaled [**por CredUnmarshalCredential.**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)<br/> |
| [**TIPO DE \_ PROTECCIÓN \_ CRED**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Especifica el contexto de seguridad en el que se cifran las credenciales cuando se usa la [**función CredProtect.**](/windows/desktop/api/WinCred/nf-wincred-credprotecta)<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumeraciones LSA

LSA usa las enumeraciones siguientes.



| Enumeración                                                                                   | Descripción                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ ENVÍO DE INICIO DE SESIÓN DE \_ \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Muestra el tipo de inicio de sesión que se solicita.<br/>                                                                                                                                                                                                                  |
| [**TIPO DE BÚFER \_ DE \_ PERFIL \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Muestra el tipo de perfil de inicio de sesión devuelto.<br/>                                                                                                                                                                                                                 |
| [**TIPO DE MENSAJE \_ DE PROTOCOLO \_ \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Enumera los tipos de mensajes que se pueden enviar al paquete de autenticación [*Kerberos*](/windows/desktop/SecGloss/k-gly) llamando a [**LsaCallAuthenticationPackage.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage)<br/> |
| [**TIPO DE REGISTRO \_ DE COLISIÓN \_ DE CONFIANZA \_ DE \_ BOSQUE \_ LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Define los tipos de colisión que pueden producirse entre los registros de confianza del bosque LSA.<br/>                                                                                                                                                                           |
| [**TIPO DE REGISTRO \_ DE CONFIANZA DE BOSQUE \_ LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Define el tipo de un registro de confianza de bosque LSA.<br/>                                                                                                                                                                                                           |
| [**TIPO DE INFORMACIÓN \_ DEL TOKEN \_ \_ LSA**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Especifica los niveles de información que se pueden incluir en un token de inicio de sesión.<br/>                                                                                                                                                                                |
| [**TIPO DE ENVÍO DE INICIO DE SESIÓN DE MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Enumera el tipo de inicio de sesión que se solicita.<br/>                                                                                                                                                                                                                  |
| [**TIPO DE BÚFER DE PERFIL MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Muestra el tipo de perfil de inicio de sesión devuelto.<br/>                                                                                                                                                                                                                 |
| [**TIPO DE MENSAJE DE PROTOCOLO MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Enumera los tipos de mensajes que se pueden enviar al paquete de autenticación [MSV1 \_ 0](msv1-0-authentication-package.md) llamando a [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**CLASE DE \_ INFORMACIÓN DE DOMINIO DE \_ \_ DIRECTIVA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Define el tipo de información de dominio de directiva.<br/>                                                                                                                                                                                                            |
| [**TIPO DE \_ INICIO DE SESIÓN DE \_ SEGURIDAD**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica el tipo de inicio de sesión solicitado por un proceso de inicio de sesión.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumeraciones de proveedor de red

El proveedor de red usa las enumeraciones siguientes.



| Enumeración                                                                       | Descripción                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SECPKG \_ EXTENDED \_ INFORMATION \_ CLASS**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo de enumeración que especifica el tipo de información que se debe establecer u obtener para un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**SECPKG \_ NAME \_ TYPE**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valor de enumeración que especifica el tipo de nombre especificado para una cuenta.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumeraciones del proveedor de compatibilidad con seguridad de credenciales (CredSSP)

CredSSP usa las enumeraciones siguientes.



| Enumeración                                          | Descripción                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**CREDSPP \_ SUBMIT \_ TYPE**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Especifica el tipo de credenciales especificadas por una [**estructura CRED DE \_ CREDSSP.**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred)<br/> |



 

## <a name="other-enumerations"></a>Otras enumeraciones

Estas son las otras enumeraciones usadas por la autenticación.



| Enumeración                                                   | Descripción                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE \_ IDENTIDAD**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Especifica el tipo de identidades que se deben enumerar.<br/>                                                                                                                                                                  |
| [**TIPO DE ENVÍO DE \_ INICIO DE \_ SESIÓN DE PKU2U \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica el tipo de mensaje de inicio de sesión pasado en una [**estructura PKU2U \_ CERTIFICATE \_ S4U \_ LOGON.**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon)<br/>                                                                                |
| [**ESTADO DE \_ SECPKG ATTR \_ \_ LCT**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica si el token de la llamada más reciente a la [**función InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) es el último token del cliente.<br/>                               |
| [**SECPKG \_ CRED \_ (CLASE)**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica el tipo de credencial utilizada en un contexto de cliente. La [**enumeración SECPKG \_ CRED \_ CLASS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) se usa en la [**estructura SecPkgContext \_ CredInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo)<br/> |



 

 

