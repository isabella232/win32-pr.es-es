---
title: Configuración del canal de seguridad
description: La configuración del canal de seguridad controla la manera en que se aplica y se comprueba la seguridad en un canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Servicios Web de configuración del canal de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149740"
---
# <a name="security-channel-settings"></a><span data-ttu-id="a9de0-106">Configuración del canal de seguridad</span><span class="sxs-lookup"><span data-stu-id="a9de0-106">Security Channel Settings</span></span>

<span data-ttu-id="a9de0-107">La configuración del canal de seguridad controla la manera en que se aplica y se comprueba la seguridad en un canal.</span><span class="sxs-lookup"><span data-stu-id="a9de0-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="a9de0-108">Cada configuración de canal de seguridad se representa mediante una colección de pares propiedad-valor, con las claves de propiedad definidas por el identificador de la [**\_ \_ propiedad \_ WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a9de0-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="a9de0-109">Cada propiedad de la colección tiene un valor predeterminado razonable.</span><span class="sxs-lookup"><span data-stu-id="a9de0-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="a9de0-110">Debido a estos valores predeterminados, es posible definir y usar una descripción de seguridad sin especificar ninguna configuración de canal de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a9de0-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="a9de0-111">La [configuración de enlace de seguridad](security-binding-settings.md) contiene colecciones similares de pares de valor y propiedad cuyas claves están definidas por la estructura de la [**\_ \_ \_ propiedad de enlace de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) .</span><span class="sxs-lookup"><span data-stu-id="a9de0-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="a9de0-112">La diferencia entre estos dos tipos de configuración es que la configuración del canal de seguridad se limita a una descripción de seguridad (es decir, que contiene propiedades de seguridad de todo el canal), mientras que la configuración de enlace de seguridad se limita a uno de los enlaces de seguridad y puede haber muchos enlaces de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a9de0-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="a9de0-113">Por lo tanto, por ejemplo, una descripción de seguridad personalizada que contiene tres enlaces de seguridad tendrá un contenedor de configuración del canal de seguridad para todo el canal y tres bolsas de configuración de enlace de seguridad, uno para cada enlace de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a9de0-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="a9de0-114">Las enumeraciones siguientes se usan con la configuración del canal de seguridad:</span><span class="sxs-lookup"><span data-stu-id="a9de0-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="a9de0-115">**\_nivel de protección de WS \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="a9de0-116">**identificador de la \_ propiedad de token de seguridad de solicitud WS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="a9de0-117">**\_identificador del \_ algoritmo de seguridad de WS \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="a9de0-118">**identificador de la propiedad del algoritmo WS \_ Security \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="a9de0-119">**\_diseño del \_ encabezado de seguridad de WS \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="a9de0-120">**versión del encabezado de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="a9de0-121">**identificador de la propiedad de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="a9de0-122">**uso de la marca de tiempo de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="a9de0-123">**identificador de la propiedad de token de seguridad de WS \_ XML \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="a9de0-124">Las siguientes estructuras se usan con la configuración del canal de seguridad:</span><span class="sxs-lookup"><span data-stu-id="a9de0-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="a9de0-125">**\_propiedad de \_ token de seguridad de solicitud WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="a9de0-126">**\_propiedad del \_ algoritmo de seguridad de WS \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="a9de0-127">**\_conjunto de \_ algoritmos de WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="a9de0-128">**\_propiedad WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="a9de0-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="a9de0-129">**\_propiedad de \_ token de seguridad \_ \_ de WS XML**</span><span class="sxs-lookup"><span data-stu-id="a9de0-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




