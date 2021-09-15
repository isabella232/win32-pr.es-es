---
title: Configuración de enlace de seguridad
description: La configuración de enlace de seguridad controla la forma en que se obtiene o se usa un token de seguridad.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Enlace de seguridad Configuración web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574229"
---
# <a name="security-binding-settings"></a>Configuración de enlace de seguridad

La configuración de enlace de seguridad controla la forma en que se obtiene o se usa un token de seguridad. Se representan como una colección de pares propiedad-valor, con las claves de propiedad definidas por la enumeración [**WS \_ SECURITY BINDING \_ \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property). Cada propiedad de la colección tiene un valor predeterminado razonable. Como resultado, es posible definir y usar una descripción de seguridad sin especificar ninguna de las opciones de enlace de seguridad.


Para obtener información sobre la configuración de seguridad de todo el canal, con propiedades cuyas claves se definen mediante la enumeración [**\_ WS SECURITY \_ PROPERTY \_ ID,**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) vea [Security Channel Configuración](security-channel-settings.md).

Los siguientes elementos de API se usan con la configuración de enlace de seguridad.

| Enumeración                                                                          | Descripción                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ERROR DEL \_ CERTIFICADO WS \_**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Define errores relacionados con la validación de certificados.                                                                                                               |
| [**ESQUEMA DE \_ AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ DE \_ WS**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Define las opciones para realizar la autenticación de cliente mediante encabezados de autenticación HTTP.                                                                       |
| [**DESTINO DE \_ AUTENTICACIÓN DE ENCABEZADO HTTP \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Define el destino del enlace de seguridad de autenticación de encabezado HTTP.                                                                                           |
| [**ACCIÓN DEL \_ TOKEN DE SEGURIDAD DE \_ \_ WS \_ REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Define el conjunto de acciones que se usarán al negociar tokens de seguridad mediante WS-Trust.                                                                              |
| [**NOMBRE DEL CONJUNTO \_ DE \_ ALGORITMOS \_ DE SEGURIDAD \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Conjunto de algoritmos de seguridad que se usan para tareas como la firma y la firma.                                                                                      |
| [**IDENTIFICADOR DE PROPIEDAD \_ DE ENLACE DE \_ \_ SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Identifica las propiedades utilizadas para especificar la configuración del enlace de seguridad.                                                                                              |
| [**MODO DE \_ \_ ENTROPÍA DE CLAVE \_ DE SEGURIDAD \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Define cómo debe contribuir la aleatoriedad a la clave emitida durante una negociación de token de seguridad realizada con seguridad de mensaje y modo mixto.                     |
| [**TIPO DE \_ CLAVE DE \_ SEGURIDAD WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | Tipo de clave de un token de seguridad.                                                                                                                                 |
| [**MODO DE REFERENCIA \_ DEL TOKEN DE SEGURIDAD \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | mecanismo que se usa para hacer referencia a un token de seguridad de firmas, elementos cifrados y tokens derivados en el contexto de los enlaces de seguridad de modo mixto y mensaje. |
| [**VERSIÓN DE WS \_ TRUST \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Define la WS-Trust de especificación que se va a usar con seguridad de mensajes y seguridad en modo mixto.                                                              |
| [**PAQUETE DE \_ \_ AUTENTICACIÓN \_ INTEGRADO DE \_ WS WINDOWS**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | Define el paquete SSP específico que se va a usar para Windows autenticación integrada.                                                                                |



 



| Estructura                                                               | Descripción                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**WS \_ SECURITY \_ BINDING \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Especifica una configuración específica del enlace de seguridad. |



 

 

 




