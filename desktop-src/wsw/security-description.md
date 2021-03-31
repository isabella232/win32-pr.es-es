---
title: Descripción de seguridad
description: Una descripción de seguridad se representa mediante una \_ \_ estructura de descripción de WS Security, y se proporciona una instancia de una descripción de seguridad al llamar a la función WsCreateChannel para crear un canal seguro o la función WsCreateListener para crear un agente de escucha.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Servicios Web de descripción de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104156980"
---
# <a name="security-description"></a><span data-ttu-id="998d8-106">Descripción de seguridad</span><span class="sxs-lookup"><span data-stu-id="998d8-106">Security Description</span></span>

<span data-ttu-id="998d8-107">Una descripción de seguridad se representa mediante una estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , y se proporciona una instancia de una descripción de seguridad al llamar a la función [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para crear un canal seguro o la función [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para crear un agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="998d8-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="998d8-108">Estructura de una descripción de seguridad</span><span class="sxs-lookup"><span data-stu-id="998d8-108">Structure of a Security Description</span></span>

<span data-ttu-id="998d8-109">El modelo básico de seguridad del canal es que un canal está protegido con uno o varios tokens de seguridad.</span><span class="sxs-lookup"><span data-stu-id="998d8-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="998d8-110">Al reflejar este modelo, la estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene una lista de enlaces de seguridad, representados por las estructuras de [**\_ \_ enlace de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , y cada enlace de seguridad describe cómo se obtiene y se utiliza un token de seguridad en el canal.</span><span class="sxs-lookup"><span data-stu-id="998d8-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="998d8-111">La selección de subtipos de enlace de seguridad que se incluyen en la descripción de seguridad decide el tipo de seguridad que se usa en un canal.</span><span class="sxs-lookup"><span data-stu-id="998d8-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="998d8-112">La configuración de seguridad opcional que es específica de un enlace de seguridad se especifica como [configuración de enlace](security-binding-settings.md) de seguridad en la estructura de enlace de seguridad. sin embargo, la configuración de todo el canal independiente de los enlaces de seguridad se especifica directamente como [configuración del canal de seguridad](security-channel-settings.md) en el campo **propiedades** de la descripción de seguridad.</span><span class="sxs-lookup"><span data-stu-id="998d8-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![Diagrama que muestra la estructura de una descripción de seguridad.](images/securitydescription.png)

<span data-ttu-id="998d8-114">Los siguientes elementos de API se usan con descripciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="998d8-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="998d8-115">Estructura</span><span class="sxs-lookup"><span data-stu-id="998d8-115">Structure</span></span>                                                    | <span data-ttu-id="998d8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="998d8-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="998d8-117">**Descripción de WS \_ Security \_**</span><span class="sxs-lookup"><span data-stu-id="998d8-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="998d8-118">La estructura de nivel superior que se usa para especificar los requisitos de seguridad para un canal (en el lado cliente) o un agente de escucha (en el lado servidor).</span><span class="sxs-lookup"><span data-stu-id="998d8-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 




