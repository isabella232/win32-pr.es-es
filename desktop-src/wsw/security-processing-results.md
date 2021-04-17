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
# <a name="security-processing-results"></a><span data-ttu-id="50d13-106">Resultados de procesamiento de seguridad</span><span class="sxs-lookup"><span data-stu-id="50d13-106">Security Processing Results</span></span>

<span data-ttu-id="50d13-107">En un canal seguro, solo los mensajes que superan correctamente las comprobaciones de seguridad se entregan a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50d13-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="50d13-108">Para estos mensajes, algunos resultados de la comprobación de seguridad se adjuntan como propiedades del mensaje y la aplicación puede extraer y examinar estas propiedades para realizar pasos adicionales, como las comprobaciones de autorización.</span><span class="sxs-lookup"><span data-stu-id="50d13-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="50d13-109">La función [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) se puede usar para recuperar cualquiera de las propiedades relacionadas con la seguridad definidas en el identificador de la [**\_ propiedad de mensaje de \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="50d13-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="50d13-110">**WsGetMessageProperty** devuelve un error para las consultas que solicitan propiedades de seguridad no aplicables al tipo de seguridad que se usa en el canal.</span><span class="sxs-lookup"><span data-stu-id="50d13-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="50d13-111">El mensaje sigue siendo el propietario de las propiedades devueltas por la función de consulta.</span><span class="sxs-lookup"><span data-stu-id="50d13-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="50d13-112">Los siguientes elementos de API se usan con los resultados de procesamiento de seguridad.</span><span class="sxs-lookup"><span data-stu-id="50d13-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="50d13-113">Enumeración</span><span class="sxs-lookup"><span data-stu-id="50d13-113">Enumeration</span></span>                                                                | <span data-ttu-id="50d13-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d13-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50d13-115">**identificador de la propiedad de token de WS \_ Security \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="50d13-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="50d13-116">Define las claves para los campos y propiedades que se pueden extraer de un token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="50d13-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="50d13-117">Función</span><span class="sxs-lookup"><span data-stu-id="50d13-117">Function</span></span>                                                         | <span data-ttu-id="50d13-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d13-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="50d13-119">**WsGetSecurityTokenProperty**</span><span class="sxs-lookup"><span data-stu-id="50d13-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="50d13-120">Extrae un campo o una propiedad de un token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="50d13-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="50d13-121">Handle</span><span class="sxs-lookup"><span data-stu-id="50d13-121">Handle</span></span>                                       | <span data-ttu-id="50d13-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d13-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="50d13-123">\_token de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="50d13-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="50d13-124">Un identificador opaco que representa un token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="50d13-124">An opaque handle representing a security token.</span></span> |



 

 

 




