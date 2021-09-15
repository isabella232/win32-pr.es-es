---
title: Credenciales de seguridad
description: Las credenciales de seguridad son un elemento de evidencia que posee una parte comunicante que se puede usar para crear u obtener un token de seguridad.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servicios web de credenciales de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467026"
---
# <a name="security-credentials"></a>Credenciales de seguridad

Las credenciales de seguridad son un elemento de evidencia que posee una parte comunicante que se puede usar para crear u obtener un token de seguridad. Por lo tanto, las credenciales suelen ser de mayor duración que los tokens de seguridad y un token de seguridad se puede ver como la expresión en tiempo de ejecución de las credenciales de seguridad. Un ejemplo de credenciales incluye un certificado de máquina (que se puede convertir en un token de seguridad X.509 en tiempo de ejecución) o un par de nombre de usuario y contraseña para un dominio (que se puede usar para obtener un token de seguridad de Kerberos).


Las credenciales se especifican como parte de los enlaces [de seguridad](security-bindings.md).

Los siguientes elementos de API se usan con credenciales de seguridad.

| Devolución de llamada                                                                  | Descripción                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Proporciona un certificado al entorno de ejecución de seguridad.          |
| [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Valida un par de nombre de usuario y contraseña en el lado receptor. |



 



| Enumeración                                                                                           | Descripción                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**WS \_ CERT \_ CREDENTIAL \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Tipo de la credencial de certificado.                       |
| [**TIPO DE \_ CREDENCIAL \_ DE NOMBRE DE USUARIO DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Tipo de la credencial de nombre de usuario y contraseña.                 |
| [**TIPO DE \_ CREDENCIAL \_ \_ DE AUTENTICACIÓN INTEGRADA \_ DE \_ WS WINDOWS**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Tipo de la credencial Windows autenticación integrada. |



 



| Estructura                                                                                                   | Descripción                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**WS \_ CERT \_ CREDENTIAL**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Tipo base abstracto para todos los tipos de credenciales de certificado.                                                          |
| [**\_CREDENCIAL DE CERTIFICADO PERSONALIZADO \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Tipo para especificar una credencial de certificado que se va a proporcionar mediante una devolución de llamada a la aplicación.             |
| [**\_CREDENCIAL DE \_ AUTENTICACIÓN INTEGRADA DE WINDOWS \_ \_ \_ PREDETERMINADA DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Escriba para proporcionar una credencial Windows autenticación integrada basada en el token de subproceso actual.                  |
| [**\_CREDENCIAL DE \_ AUTENTICACIÓN INTEGRADA DE WINDOWS \_ \_ OPACA \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Escriba para proporcionar una credencial Windows autenticación integrada.                                                    |
| [**CREDENCIAL DE \_ NOMBRE DE USUARIO DE \_ \_ WS STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Tipo para proporcionar un par de nombre de usuario y contraseña como cadenas.                                                           |
| [**\_CREDENCIAL DE \_ AUTENTICACIÓN INTEGRADA DE WINDOWS \_ \_ DE \_ WS STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Escriba para proporcionar una credencial Windows nombre de usuario, contraseña y cadenas de dominio.                                        |
| [**WS \_ SUBJECT \_ NAME \_ CERT \_ CREDENTIAL**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Tipo para especificar una credencial de certificado mediante el nombre del firmante del certificado, la ubicación del almacén y el nombre del almacén. |
| [**\_CREDENCIAL DE CERTIFICADO DE HUELLA DIGITAL \_ \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Tipo para especificar una credencial de certificado mediante la huella digital del certificado, la ubicación del almacén y el nombre del almacén.   |
| [**CREDENCIAL \_ DE NOMBRE DE USUARIO DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Tipo base abstracto para todas las credenciales de nombre de usuario y contraseña.                                                         |
| [**CREDENCIAL DE \_ \_ \_ AUTENTICACIÓN INTEGRADA DE WS WINDOWS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | Tipo base abstracto para todos los tipos de credenciales usados con Windows autenticación integrada.                          |



 

 

 




