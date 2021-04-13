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
# <a name="security-context"></a><span data-ttu-id="73478-106">Contexto de seguridad</span><span class="sxs-lookup"><span data-stu-id="73478-106">Security Context</span></span>

<span data-ttu-id="73478-107">Los contextos de seguridad permiten el establecimiento de un contexto de seguridad de mensaje de acuerdo con WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="73478-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="73478-108">Dicho contexto puede usarse para proteger los mensajes como una alternativa a la seguridad de una vacuna en la que se transmiten las credenciales para cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="73478-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="73478-109">El contexto de seguridad establecido es un método más eficaz para proteger los mensajes cuando se intercambian varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="73478-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="73478-110">Los contextos de seguridad requieren la presencia de credenciales de seguridad de arranque que se usan para proteger los mensajes enviados en el contexto.</span><span class="sxs-lookup"><span data-stu-id="73478-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="73478-111">Para este fin se pueden usar las estructuras de enlace de seguridad de mensajes WS [**\_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**\_ \_ \_ \_ \_ enlace**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)de seguridad de mensaje de token de WS XML y enlace de seguridad de mensaje de WS [**\_ username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) .</span><span class="sxs-lookup"><span data-stu-id="73478-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="73478-112">Los contextos de seguridad son una característica de seguridad de mensajes y se configuran mediante enlaces de seguridad de mensajes.</span><span class="sxs-lookup"><span data-stu-id="73478-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="73478-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="73478-113">Client</span></span>

<span data-ttu-id="73478-114">En el lado del cliente, el contexto de seguridad está asociado a un canal determinado.</span><span class="sxs-lookup"><span data-stu-id="73478-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="73478-115">Se configura mediante el [**enlace de \_ \_ seguridad de \_ mensaje \_ \_ de contexto de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span><span class="sxs-lookup"><span data-stu-id="73478-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="73478-116">El canal determina el comportamiento y la duración del contexto.</span><span class="sxs-lookup"><span data-stu-id="73478-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="73478-117">Cuando se envía el primer mensaje en el canal, se establece el contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73478-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="73478-118">Después, el contexto se renueva de forma proactiva en un intervalo configurable.</span><span class="sxs-lookup"><span data-stu-id="73478-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="73478-119">Si el servidor devuelve un error que indica que el contexto requiere una renovación, el contexto se renueva cuando se envía el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="73478-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="73478-120">Si el canal está en estado abierto, un mensaje de cancelación cancela el contexto cuando se cierra el canal.</span><span class="sxs-lookup"><span data-stu-id="73478-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="73478-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="73478-121">Server</span></span>

<span data-ttu-id="73478-122">En el servidor, un contexto de seguridad se configura de la misma manera que en el cliente.</span><span class="sxs-lookup"><span data-stu-id="73478-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="73478-123">Sin embargo, no está vinculado a ningún canal determinado.</span><span class="sxs-lookup"><span data-stu-id="73478-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="73478-124">En su lugar, todos los canales creados para el agente de escucha que tienen el conjunto de [**enlaces de seguridad de mensaje de contexto de WS \_ Security \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) pueden recibir mensajes con cualquiera de los contextos de seguridad que se establecieron en los canales de ese agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="73478-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="73478-125">Cuando llega un mensaje en un canal que admite contextos de seguridad, el contexto utilizado por ese mensaje puede obtenerse mediante una llamada a la función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con el contexto de seguridad de la [**\_ \_ propiedad \_ \_ WS Message**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="73478-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="73478-126">El valor recuperado se puede usar con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) y [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span><span class="sxs-lookup"><span data-stu-id="73478-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="73478-127">Metadatos</span><span class="sxs-lookup"><span data-stu-id="73478-127">Metadata</span></span>

<span data-ttu-id="73478-128">La estructura de restricción de enlace de seguridad de [**mensaje de contexto de WS \_ \_ \_ \_ \_ \_ Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) se usa para extraer la Directiva de contexto de seguridad de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="73478-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="73478-129">Para obtener más información, consulte [importación de metadatos](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="73478-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="73478-130">Los siguientes elementos de API se usan con contextos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73478-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="73478-131">Enumeración</span><span class="sxs-lookup"><span data-stu-id="73478-131">Enumeration</span></span>                                                                    | <span data-ttu-id="73478-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="73478-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="73478-133">**identificador de la propiedad de contexto de WS \_ Security \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="73478-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="73478-134">Identifica una propiedad de un objeto de contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73478-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="73478-135">Función</span><span class="sxs-lookup"><span data-stu-id="73478-135">Function</span></span>                                                             | <span data-ttu-id="73478-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="73478-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="73478-137">**WsGetSecurityContextProperty**</span><span class="sxs-lookup"><span data-stu-id="73478-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="73478-138">Obtiene una propiedad del contexto de seguridad especificado.</span><span class="sxs-lookup"><span data-stu-id="73478-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="73478-139">**WsRevokeSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="73478-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="73478-140">Revoca un contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73478-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="73478-141">Handle</span><span class="sxs-lookup"><span data-stu-id="73478-141">Handle</span></span>                                           | <span data-ttu-id="73478-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="73478-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="73478-143">\_contexto de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="73478-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="73478-144">Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73478-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="73478-145">Estructura</span><span class="sxs-lookup"><span data-stu-id="73478-145">Structure</span></span>                                                               | <span data-ttu-id="73478-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="73478-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="73478-147">**propiedad de contexto de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="73478-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="73478-148">Define una propiedad de un [ \_ \_ contexto de seguridad de WS](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="73478-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




