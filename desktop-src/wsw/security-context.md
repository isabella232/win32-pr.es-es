---
title: Contexto de seguridad
description: Los contextos de seguridad permiten el establecimiento de un contexto de seguridad de mensaje de acuerdo con WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contexto de seguridad Native-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359525"
---
# <a name="security-context"></a>Contexto de seguridad

Los contextos de seguridad permiten el establecimiento de un contexto de seguridad de mensaje de acuerdo con WS-SecureConversation. Dicho contexto puede usarse para proteger los mensajes como una alternativa a la seguridad de una vacuna en la que se transmiten las credenciales para cada solicitud. El contexto de seguridad establecido es un método más eficaz para proteger los mensajes cuando se intercambian varios mensajes.


Los contextos de seguridad requieren la presencia de credenciales de seguridad de arranque que se usan para proteger los mensajes enviados en el contexto. Para este fin se pueden usar las estructuras de enlace de seguridad de mensajes WS [**\_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**\_ \_ \_ \_ \_ enlace**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)de seguridad de mensaje de token de WS XML y enlace de seguridad de mensaje de WS [**\_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) .

Los contextos de seguridad son una característica de seguridad de mensajes y se configuran mediante enlaces de seguridad de mensajes.

## <a name="client"></a>Remoto

En el lado del cliente, el contexto de seguridad está asociado a un canal determinado. Se configura mediante el [**enlace de \_ \_ seguridad de \_ mensaje \_ \_ de contexto de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). El canal determina el comportamiento y la duración del contexto. Cuando se envía el primer mensaje en el canal, se establece el contexto de seguridad. Después, el contexto se renueva de forma proactiva en un intervalo configurable. Si el servidor devuelve un error que indica que el contexto requiere una renovación, el contexto se renueva cuando se envía el siguiente mensaje. Si el canal está en estado abierto, un mensaje de cancelación cancela el contexto cuando se cierra el canal.

## <a name="server"></a>Servidor

En el servidor, un contexto de seguridad se configura de la misma manera que en el cliente. Sin embargo, no está vinculado a ningún canal determinado. En su lugar, todos los canales creados para el agente de escucha que tienen el conjunto de [**enlaces de seguridad de mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) pueden recibir mensajes con cualquiera de los contextos de seguridad que se establecieron en los canales de ese agente de escucha.

Cuando llega un mensaje en un canal que admite contextos de seguridad, el contexto utilizado por ese mensaje puede obtenerse mediante una llamada a la función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con el contexto de seguridad de la [**\_ \_ propiedad \_ \_ WS Message**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). El valor recuperado se puede usar con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) y [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).

## <a name="metadata"></a>Metadatos

La estructura de restricción de enlace de seguridad de [**mensaje de contexto de WS \_ \_ \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) se usa para extraer la Directiva de contexto de seguridad de los metadatos. Para obtener más información, consulte [importación de metadatos](metadata-import.md).

Los siguientes elementos de API se usan con contextos de seguridad.

| Enumeración                                                                    | Descripción                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**identificador de la propiedad de contexto de WS \_ Security \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica una propiedad de un objeto de contexto de seguridad. |



 



| Función                                                             | Descripción                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Obtiene una propiedad del contexto de seguridad especificado. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoca un contexto de seguridad.                        |



 



| Handle                                           | Descripción                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [\_contexto de seguridad de WS \_](ws-security-context.md) | Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad. |



 



| Estructura                                                               | Descripción                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**propiedad de contexto de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Define una propiedad de un [ \_ \_ contexto de seguridad de WS](ws-security-context.md). |



 

 

 




