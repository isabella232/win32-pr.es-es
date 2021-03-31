---
title: Estructuras 2,0 de la API del servidor HTTP
description: La API del servidor HTTP versión 2,0 proporciona las siguientes estructuras para escribir aplicaciones
ms.assetid: 5a8e28e9-f85b-4550-929e-53f38eca6a8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5e41016592e16fcf159188cc1ebc760568f807
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418729"
---
# <a name="http-server-api-version-20-structures"></a><span data-ttu-id="cf8b8-103">Estructuras 2,0 de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="cf8b8-103">HTTP Server API Version 2.0 Structures</span></span>

<span data-ttu-id="cf8b8-104">La API del servidor HTTP versión 2,0 proporciona las siguientes estructuras para escribir aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="cf8b8-104">The HTTP Server API version 2.0 provides the following structures for writing applications:</span></span>

-   [<span data-ttu-id="cf8b8-105">**información de límite de ancho de \_ banda http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-105">**HTTP\_BANDWIDTH\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)
-   [<span data-ttu-id="cf8b8-106">**\_información de enlace http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-106">**HTTP\_BINDING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_binding_info)
-   [<span data-ttu-id="cf8b8-107">**\_información de \_ enlace de canal http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-107">**HTTP\_CHANNEL\_BIND\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_channel_bind_info)
-   [<span data-ttu-id="cf8b8-108">**\_información de \_ límite de conexión HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-108">**HTTP\_CONNECTION\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_connection_limit_info)
-   [<span data-ttu-id="cf8b8-109">**\_información del caudal de http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-109">**HTTP\_FLOWRATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_flowrate_info)
-   [<span data-ttu-id="cf8b8-110">**\_información de \_ extremo de escucha http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-110">**HTTP\_LISTEN\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_listen_endpoint_info)
-   [<span data-ttu-id="cf8b8-111">**\_datos de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-111">**HTTP\_LOG\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_data)
-   [<span data-ttu-id="cf8b8-112">**\_datos de \_ campos de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-112">**HTTP\_LOG\_FIELDS\_DATA**</span></span>](/windows/desktop/api/Http/ns-http-http_log_fields_data)
-   [<span data-ttu-id="cf8b8-113">**\_información de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-113">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
-   [<span data-ttu-id="cf8b8-114">**HTTP \_ varios \_ \_ encabezados conocidos**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-114">**HTTP\_MULTIPLE\_KNOWN\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_multiple_known_headers)
-   [<span data-ttu-id="cf8b8-115">**\_marcas de propiedades http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-115">**HTTP\_PROPERTY\_FLAGS**</span></span>](/windows/desktop/api/Http/ns-http-http_property_flags)
-   [<span data-ttu-id="cf8b8-116">**\_información de \_ configuración de QoS de http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-116">**HTTP\_QOS\_SETTING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_qos_setting_info)
-   [<span data-ttu-id="cf8b8-117">**información de autenticación de la \_ solicitud HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-117">**HTTP\_REQUEST\_AUTH\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_auth_info)
-   [<span data-ttu-id="cf8b8-118">**\_Estado de \_ enlace de canal de solicitud HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-118">**HTTP\_REQUEST\_CHANNEL\_BIND\_STATUS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_channel_bind_status)
-   [<span data-ttu-id="cf8b8-119">**información de la \_ solicitud HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-119">**HTTP\_REQUEST\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_request_info)
-   [<span data-ttu-id="cf8b8-120">**\_Solicitud HTTP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-120">**HTTP\_REQUEST\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v1)
-   [<span data-ttu-id="cf8b8-121">**\_Solicitud HTTP \_ V2**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-121">**HTTP\_REQUEST\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_request_v2)
-   [<span data-ttu-id="cf8b8-122">**\_información de respuesta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-122">**HTTP\_RESPONSE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_response_info)
-   [<span data-ttu-id="cf8b8-123">**\_Respuesta HTTP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-123">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
-   [<span data-ttu-id="cf8b8-124">**\_Respuesta HTTP \_ V2**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-124">**HTTP\_RESPONSE\_V2**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v2)
-   [<span data-ttu-id="cf8b8-125">**\_ \_ parámetros básicos de autenticación del servidor HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-125">**HTTP\_SERVER\_AUTHENTICATION\_BASIC\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_basic_params)
-   [<span data-ttu-id="cf8b8-126">**\_parámetros de \_ Resumen de autenticación del servidor HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-126">**HTTP\_SERVER\_AUTHENTICATION\_DIGEST\_PARAMS**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_digest_params)
-   [<span data-ttu-id="cf8b8-127">**\_información de \_ autenticación del servidor HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-127">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
-   [<span data-ttu-id="cf8b8-128">**\_ \_ enlace de servicio HTTP \_ A**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-128">**HTTP\_SERVICE\_BINDING\_A**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_a)
-   [<span data-ttu-id="cf8b8-129">**\_enlace de servicio HTTP \_ \_ W**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-129">**HTTP\_SERVICE\_BINDING\_W**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_w)
-   [<span data-ttu-id="cf8b8-130">**\_base de \_ enlace de servicio HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-130">**HTTP\_SERVICE\_BINDING\_BASE**</span></span>](/windows/desktop/api/Http/ns-http-http_service_binding_base)
-   [<span data-ttu-id="cf8b8-131">**\_tipo de \_ enlace de servicio HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-131">**HTTP\_SERVICE\_BINDING\_TYPE**</span></span>](/windows/desktop/api/Http/ne-http-http_service_binding_type)
-   [<span data-ttu-id="cf8b8-132">**\_conjunto de \_ caché de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-132">**HTTP\_SERVICE\_CONFIG\_CACHE\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_cache_set)
-   [<span data-ttu-id="cf8b8-133">**\_tiempo de espera de configuración del servicio HTTP \_ \_ \_ establecido**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-133">**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set)
-   [<span data-ttu-id="cf8b8-134">**\_información de estado de http \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-134">**HTTP\_STATE\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_state_info)
-   [<span data-ttu-id="cf8b8-135">**información de límite de tiempo de \_ espera http \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-135">**HTTP\_TIMEOUT\_LIMIT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

 

 




