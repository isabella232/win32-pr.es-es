---
title: Identidad de extremo
description: Los tipos definidos en esta sección se usan para definir la identidad de seguridad de una dirección de punto de conexión.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Servicios web de identidad de punto de conexión para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262015"
---
# <a name="endpoint-identity"></a>Identidad de extremo

Los tipos definidos en esta sección se usan para definir la identidad de seguridad de una dirección de punto de conexión.

Los siguientes elementos de API forman parte de la sangría del punto de conexión:



| Enumeración                                                       | Descripción                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DE IDENTIDAD \_ DEL PUNTO DE CONEXIÓN \_ \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | Tipo de la identidad del punto de conexión, que se usa como selector para los subtipos de [**WS \_ ENDPOINT \_ IDENTITY.**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity) |



 



| Estructura                                                               | Descripción                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WS \_ CERT \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | Tipo de identidad de punto de conexión de certificado.                                                 |
| [**WS \_ DNS \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | Tipo para especificar una identidad de punto de conexión representada por un nombre DNS.                      |
| [**WS \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | Tipo base para todas las identidades de punto de conexión.                                                   |
| [**WS \_ RSA \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | Escriba la identidad del punto de conexión RSA.                                                              |
| [**WS \_ SPN \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | Tipo para especificar una identidad de punto de conexión representada por un SPN (nombre de entidad de seguridad de servicio). |
| [**WS \_ UNKNOWN \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | Tipo de una identidad de punto de conexión desconocida.                                                   |
| [**WS \_ UPN \_ ENDPOINT \_ IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | Tipo para especificar una identidad de punto de conexión representada por un UPN (nombre principal de usuario).     |



 

 

 




