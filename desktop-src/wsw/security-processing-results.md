---
title: Resultados del procesamiento de seguridad
description: En un canal seguro, solo los mensajes que pasan correctamente comprobaciones de seguridad se entregan a la aplicación.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Servicios web de resultados de procesamiento de seguridad para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53009729b3d7f1c8ff6b9e38a054d8dbadf202b7a0caa4a92c7861232c8390a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962934"
---
# <a name="security-processing-results"></a>Resultados del procesamiento de seguridad

En un canal seguro, solo los mensajes que pasan correctamente comprobaciones de seguridad se entregan a la aplicación. Para estos mensajes, algunos resultados de la comprobación de seguridad se adjuntan como propiedades del mensaje y la aplicación puede extraer y examinar estas propiedades para realizar pasos adicionales, como comprobaciones de autorización.


La función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) se puede usar para recuperar cualquiera de las propiedades relacionadas con la seguridad definidas en el identificador de [**propiedad de WS \_ MESSAGE \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** devuelve un error para las consultas que solicitan propiedades de seguridad no aplicables al tipo de seguridad utilizado en el canal. El mensaje sigue siendo propietario de las propiedades devueltas por la función de consulta.

Los siguientes elementos de API se usan con los resultados del procesamiento de seguridad.

| Enumeración                                                                | Descripción                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**IDENTIFICADOR DE PROPIEDAD \_ DEL TOKEN DE SEGURIDAD \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Define las claves de los campos y propiedades que se pueden extraer de un token de seguridad. |



 



| Función                                                         | Descripción                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Extrae un campo o una propiedad de un token de seguridad. |



 



| Handle                                       | Descripción                                     |
|----------------------------------------------|-------------------------------------------------|
| [TOKEN DE SEGURIDAD DE WS \_ \_](ws-security-token.md) | Identificador opaco que representa un token de seguridad. |



 

 

 




