---
title: Estructuras de suplicante de EAPHost
description: Obtenga información acerca de las estructuras de la API de suplicante de EAPHost, como \_ \_ matriz de propiedades de método EAP y req \_ \_ \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7121e123fd790a54a95dafb59c080f435ca917
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421400"
---
# <a name="eaphost-supplicant-structures"></a>Estructuras de suplicante de EAPHost

Las estructuras de la API suplicante de EAPHost son las siguientes.



| Estructura                                                                        | Descripción                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_solicitud de credenciales de EAP \_**](eap-cred-req.md)                                           | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                    |
| [**respuesta de cred de EAP \_ \_**](eap-cred-resp.md)                                         | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de cambio de credenciales.                                    |
| [**\_solicitud de \_ expiración de credenciales de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                     |
| [**respuesta \_ de \_ expiración de credenciales de EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contiene las credenciales de EAP antiguas y nuevas para las operaciones de expiración de credenciales.                                    |
| [**\_solicitud de \_ Inicio de sesión de recred de EAP \_**](eap-cred-logon-req.md)                              | Contiene credenciales EAP para la autenticación de red.                                                                 |
| [**EAP de inicio de sesión de la \_ \_ \_ resp**](eap-cred-logon-resp.md)                            | Contiene credenciales EAP para la autenticación de red.                                                                 |
| [**\_datos de \_ interfaz de usuario interactiva de EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contiene información de configuración para los componentes de interfaz de usuario interactivos generados en un suplicante EAP.            |
| [**\_propiedad de método EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 o posterior: representa una propiedad de método.                                                                    |
| [**\_matriz de \_ propiedades de método EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 o posterior: contiene una matriz de estructuras de propiedades de método.                                                 |
| [**valor de la \_ propiedad de método EAP \_ \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 o posterior: contiene un valor de propiedad de método.                                                                |
| [**\_valor de propiedad de método EAP \_ \_ \_ booleano**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 o posterior: contiene un valor de propiedad de método de tipo de datos BOOL.                                                 |
| [**\_ \_ \_ valor \_ DWORD de la propiedad del método EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 o posterior: contiene un valor de propiedad de método de tipo de datos DWORD.                                                |
| [**\_cadena de \_ valor de propiedad de método EAP \_ \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 o posterior: contiene un valor de propiedad de método de tipo de datos de cadena.                                               |
| [**\_información de autenticación de EAPHOST \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Describe la información de autenticación actual en diferentes fases del proceso de autenticación de EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contiene los datos de resultado generados por EAPHost durante una sesión de autenticación que se pasa a continuación a un método EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 o posterior: contiene la información de protección de acceso a redes (NAP) de un suplicante EAP.                   |



 

 

 