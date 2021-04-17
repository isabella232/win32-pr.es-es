---
title: Resultados de procesamiento de seguridad
description: En un canal seguro, solo los mensajes que superan correctamente las comprobaciones de seguridad se entregan a la aplicación.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Servicios Web de resultados de procesamiento de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105705075"
---
# <a name="security-processing-results"></a>Resultados de procesamiento de seguridad

En un canal seguro, solo los mensajes que superan correctamente las comprobaciones de seguridad se entregan a la aplicación. Para estos mensajes, algunos resultados de la comprobación de seguridad se adjuntan como propiedades del mensaje y la aplicación puede extraer y examinar estas propiedades para realizar pasos adicionales, como las comprobaciones de autorización.


La función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) se puede usar para recuperar cualquiera de las propiedades relacionadas con la seguridad definidas en el identificador de la [**\_ propiedad de mensaje de \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** devuelve un error para las consultas que solicitan propiedades de seguridad no aplicables al tipo de seguridad que se usa en el canal. El mensaje sigue siendo el propietario de las propiedades devueltas por la función de consulta.

Los siguientes elementos de API se usan con los resultados de procesamiento de seguridad.

| Enumeración                                                                | Descripción                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**identificador de la propiedad de token de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Define las claves para los campos y propiedades que se pueden extraer de un token de seguridad. |



 



| Función                                                         | Descripción                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrae un campo o una propiedad de un token de seguridad. |



 



| Handle                                       | Descripción                                     |
|----------------------------------------------|-------------------------------------------------|
| [\_token de seguridad de WS \_](ws-security-token.md) | Un identificador opaco que representa un token de seguridad. |



 

 

 




