---
title: Contexto de seguridad
description: Los contextos de seguridad permiten el establecimiento de un contexto de seguridad de mensajes según WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexto de seguridad Native-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467027"
---
# <a name="security-context"></a>Contexto de seguridad

Los contextos de seguridad permiten el establecimiento de un contexto de seguridad de mensajes según WS-SecureConversation. A continuación, ese contexto se puede usar para proteger los mensajes como alternativa a la seguridad de un solo uso donde se transmiten las credenciales para cada solicitud. El contexto de seguridad establecido es un método más eficaz para proteger los mensajes cuando se intercambian varios mensajes.


Los contextos de seguridad requieren la presencia de credenciales de seguridad de arranque que se usan para proteger los mensajes enviados en el contexto. Para ello, se pueden usar las estructuras [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS XML TOKEN MESSAGE \_ \_ SECURITY \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)y [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)

Los contextos de seguridad son una característica de seguridad de mensajes y se configuran mediante enlaces de seguridad de mensajes.

## <a name="client"></a>Remoto

En el lado cliente, el contexto de seguridad está asociado a un canal determinado. Se configura mediante [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). El canal determina el comportamiento y la duración del contexto. Cuando se envía el primer mensaje en el canal, se establece el contexto de seguridad. Después de eso, el contexto se renueva proactivamente en un intervalo configurable. Si el servidor devuelve un error que indica que el contexto requiere renovación, el contexto se renueva cuando se envía el mensaje siguiente. Si el canal está en estado abierto, el contexto se cancela mediante un mensaje de cancelación cuando se cierra el canal.

## <a name="server"></a>Servidor

En el servidor, un contexto de seguridad se configura de la misma manera que en el cliente. Sin embargo, no está vinculado a ningún canal determinado. En su lugar, todos los canales creados para el agente de escucha que tienen establecido [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) pueden recibir mensajes con cualquiera de los contextos de seguridad establecidos en los canales de ese agente de escucha.

Cuando un mensaje llega a un canal que admite contextos de seguridad, el contexto utilizado por ese mensaje se puede obtener llamando a la función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con el contexto de seguridad de la propiedad [**de WS \_ MESSAGE \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). El valor recuperado se puede usar con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) y [**WsGetSecurityContextProperty.**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)

## <a name="metadata"></a>Metadatos

La [**estructura WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) se usa para extraer la directiva de contexto de seguridad de los metadatos. Para obtener más información, vea [Importación de metadatos.](metadata-import.md)

Los siguientes elementos de API se usan con contextos de seguridad.

| Enumeración                                                                    | Descripción                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**IDENTIFICADOR DE PROPIEDAD \_ DEL CONTEXTO DE SEGURIDAD \_ \_ \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica una propiedad de un objeto de contexto de seguridad. |



 



| Función                                                             | Descripción                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Obtiene una propiedad del contexto de seguridad especificado. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoca un contexto de seguridad.                        |



 



| Handle                                           | Descripción                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [CONTEXTO DE SEGURIDAD DE WS \_ \_](ws-security-context.md) | Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad. |



 



| Estructura                                                               | Descripción                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**WS \_ SECURITY \_ CONTEXT \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Define una propiedad de un [contexto \_ de seguridad \_ de WS](ws-security-context.md). |



 

 

 




