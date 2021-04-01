---
title: Configuración de enlace de seguridad
description: Los valores de enlace de seguridad controlan la manera en que se obtiene o se usa un token de seguridad.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Servicios Web de configuración de enlace de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797271"
---
# <a name="security-binding-settings"></a>Configuración de enlace de seguridad

Los valores de enlace de seguridad controlan la manera en que se obtiene o se usa un token de seguridad. Se representan como una colección de pares propiedad-valor, con las claves de propiedad definidas por la [**propiedad de \_ \_ enlace WS \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)de la enumeración. Cada propiedad de la colección tiene un valor predeterminado razonable. Como resultado, es posible definir y usar una descripción de seguridad sin especificar ninguna de las opciones de enlace de seguridad.


Para obtener información sobre la configuración de seguridad de todo el canal, con propiedades cuyas claves se definen mediante la enumeración de [**identificador de propiedad de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) , consulte [configuración del canal de seguridad](security-channel-settings.md).

Los siguientes elementos de API se usan con la configuración de enlace de seguridad.

| Enumeración                                                                          | Descripción                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_error de certificado WS \_**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Define los errores relacionados con la validación de certificados.                                                                                                               |
| [**\_esquema de \_ autenticación de encabezado HTTP \_ de WS \_**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Define las opciones para realizar la autenticación del cliente mediante encabezados de autenticación HTTP.                                                                       |
| [**\_destino de \_ autenticación de encabezado HTTP \_ de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Define el destino del enlace de seguridad de autenticación del encabezado HTTP.                                                                                           |
| [**\_acción de \_ token de seguridad de solicitud WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Define el conjunto de acciones que se va a usar al negociar tokens de seguridad mediante WS-Trust.                                                                              |
| [**\_nombre del \_ conjunto de algoritmos de WS Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Conjunto de algoritmos de seguridad que se usa para tareas como la firma y la encryting.                                                                                      |
| [**identificador de la propiedad de enlace de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Identifica las propiedades utilizadas para especificar la configuración de enlace de seguridad.                                                                                              |
| [**\_modo de \_ entropía de clave de WS Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Define cómo se debe contribuir la aleatoriedad a la clave emitida durante una negociación de tokens de seguridad realizada con la seguridad de modo mixto y de mensaje.                     |
| [**tipo de clave de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | El tipo de clave de un token de seguridad.                                                                                                                                 |
| [**\_modo de \_ referencia de tokens de WS Security \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | mecanismo que se va a usar para hacer referencia a un token de seguridad de firmas, elementos cifrados y tokens derivados en el contexto de los enlaces de seguridad de modo mixto y de mensaje. |
| [**versión de WS- \_ Trust \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Define la versión de especificación de WS-Trust que se va a utilizar con la seguridad de mensajes y la seguridad de modo mixto.                                                              |
| [**\_paquete de \_ \_ autenticación integrada \_ de WS Windows**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | Define el paquete SSP específico que se va a utilizar para la autenticación integrada de Windows.                                                                                |



 



| Estructura                                                               | Descripción                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**propiedad de enlace de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Especifica un valor específico de enlace de seguridad. |



 

 

 




