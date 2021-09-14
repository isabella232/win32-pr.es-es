---
title: Estructuras suplicantes de EAPHost
description: Obtenga información sobre las estructuras de API de suplicación de EAPHost, como EAP \_ CRED \_ REQ y EAP \_ METHOD PROPERTY \_ \_ ARRAY.
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7121e123fd790a54a95dafb59c080f435ca917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252956"
---
# <a name="eaphost-supplicant-structures"></a>Estructuras suplicantes de EAPHost

Las estructuras de API de suplicación de EAPHost son las siguientes.



| Estructura                                                                        | Descripción                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**EAP \_ CRED \_ REQ**](eap-cred-req.md)                                           | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                    |
| [**EAP \_ CRED \_ RESP**](eap-cred-resp.md)                                         | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                    |
| [**SOLICITUD \_ DE SOLICITUD DE \_ EXPIRACIÓN \_ CRED DE EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales                                     |
| [**EAP \_ CRED \_ EXPIRY \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contiene las credenciales eap antiguas y nuevas para las operaciones de expiración de credenciales.                                    |
| [**EAP \_ CRED \_ LOGON \_ REQ**](eap-cred-logon-req.md)                              | Contiene credenciales de EAP para la autenticación de red.                                                                 |
| [**EAP \_ CRED \_ LOGON \_ RESP**](eap-cred-logon-resp.md)                            | Contiene credenciales de EAP para la autenticación de red.                                                                 |
| [**DATOS DE \_ LA INTERFAZ DE USUARIO INTERACTIVA \_ DE EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contiene información de configuración para los componentes interactivos de la interfaz de usuario que se genera en un suplicante eap.            |
| [**EAP \_ METHOD \_ PROPERTY**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 o posterior: representa una propiedad de método.                                                                    |
| [**MATRIZ DE \_ PROPIEDADES DEL \_ MÉTODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 o posterior: contiene una matriz de estructuras de propiedades de método.                                                 |
| [**VALOR DE \_ PROPIEDAD DEL \_ MÉTODO \_ EAP**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 o posterior: contiene un valor de propiedad de método.                                                                |
| [**VALOR DE PROPIEDAD DEL MÉTODO EAP \_ \_ \_ \_ BOOL**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 o posterior: contiene un valor de propiedad de método de tipo de datos BOOL.                                                 |
| [**VALOR \_ \_ DWORD DE \_ LA PROPIEDAD DEL MÉTODO \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 o posterior: contiene un valor de propiedad del método de tipo de datos DWORD.                                                |
| [**CADENA DE \_ VALOR DE PROPIEDAD DEL MÉTODO \_ \_ \_ EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 o posterior: contiene un valor de propiedad de método de tipo de datos de cadena.                                               |
| [**INFORMACIÓN DE \_ AUTENTICACIÓN DE \_ EAPHOST**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Describe la información de autenticación actual en las distintas fases del proceso de autenticación eap.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contiene los datos de resultado generados por EAPHost durante una sesión de autenticación que luego se pasa a un método EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 o posterior: contiene la información de Protección de acceso a redes (NAP) en un suplicante eap.                   |



 

 

 