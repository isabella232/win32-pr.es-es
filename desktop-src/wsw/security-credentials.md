---
title: Credenciales de seguridad
description: Las credenciales de seguridad son un fragmento de evidencia que posee una entidad de comunicación que se puede usar para crear u obtener un token de seguridad.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servicios Web de credenciales de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105705078"
---
# <a name="security-credentials"></a>Credenciales de seguridad

Las credenciales de seguridad son un fragmento de evidencia que posee una entidad de comunicación que se puede usar para crear u obtener un token de seguridad. Por lo tanto, las credenciales suelen durar más que los tokens de seguridad, y un token de seguridad se puede ver como la manifestación en tiempo de ejecución de las credenciales de seguridad. Un ejemplo de credenciales incluye un certificado de equipo (que se puede convertir en un token de seguridad X. 509 en tiempo de ejecución) o un par de nombre de usuario/contraseña para un dominio (que se puede usar para obtener un token de seguridad de Kerberos).


Las credenciales se especifican como parte de los [enlaces de seguridad](security-bindings.md).

Los siguientes elementos de API se usan con las credenciales de seguridad.

| Devolución de llamada                                                                  | Descripción                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**devolución de llamada de WS \_ Get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Proporciona un certificado para el tiempo de ejecución de seguridad.          |
| [**devolución de llamada de validación de contraseña de WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Valida un par de nombre de usuario y contraseña en el lado receptor. |



 



| Enumeración                                                                                           | Descripción                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**\_tipo de \_ credencial de certificado WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | El tipo de la credencial de certificado.                       |
| [**tipo de credencial de WS \_ username \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Tipo de la credencial de nombre de usuario/contraseña.                 |
| [**\_tipo de \_ \_ credencial de autenticación integrada \_ \_ de WS Windows**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | El tipo de credencial de autenticación integrada de Windows. |



 



| Estructura                                                                                                   | Descripción                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_credencial de certificado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | El tipo base abstracto para todos los tipos de credenciales de certificado.                                                          |
| [**\_credencial de \_ certificado \_ personalizado de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Tipo para especificar una credencial de certificado que se va a proporcionar mediante una devolución de llamada a la aplicación.             |
| [**\_credencial de \_ \_ autenticación integrada \_ de \_ Windows de WS predeterminada**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Tipo para proporcionar una credencial de autenticación integrada de Windows basada en el token de subproceso actual.                  |
| [**\_credencial de \_ autenticación de Windows \_ integrada \_ \_ de WS opaco**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Escriba para proporcionar una credencial de autenticación integrada de Windows.                                                    |
| [**\_credencial de \_ nombre de usuario de WS String \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Tipo para proporcionar un par de nombre de usuario y contraseña como cadenas.                                                           |
| [**\_credencial de \_ \_ autenticación integrada \_ de Windows de cadena WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Escriba para proporcionar una credencial de Windows como nombre de usuario, contraseña y cadenas de dominio.                                        |
| [**\_credencial de \_ certificado de nombre de firmante de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | El tipo para especificar una credencial de certificado con el nombre de sujeto del certificado, la ubicación del almacén y el nombre de almacén. |
| [**\_credencial de certificado de huella digital de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Tipo para especificar una credencial de certificado utilizando la huella digital del certificado, la ubicación del almacén y el nombre de almacén.   |
| [**credencial de WS \_ username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | El tipo base abstracto para todas las credenciales de nombre de usuario y contraseña.                                                         |
| [**\_credencial de \_ \_ autenticación integrada \_ de WS Windows**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | El tipo base abstracto para todos los tipos de credenciales que se usan con la autenticación integrada de Windows.                          |



 

 

 




