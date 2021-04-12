---
title: Estructuras 1,0 de la API del servidor HTTP
description: Estructuras 1,0 de la API del servidor HTTP
ms.assetid: e38f7a05-f966-4853-be3b-5cdbf224719e
keywords:
- Estructuras de API de servidor HTTP
- Estructuras HTTP, API de servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67cdd426bbe9329e089352999acf5c0f79b6f94f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420671"
---
# <a name="http-server-api-version-10-structures"></a><span data-ttu-id="ec381-105">Estructuras 1,0 de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="ec381-105">HTTP Server API Version 1.0 Structures</span></span>

<span data-ttu-id="ec381-106">La API del servidor HTTP proporciona las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="ec381-106">The HTTP Server API provides the following structures:</span></span>

-   [<span data-ttu-id="ec381-107">**versión de HTTPAPI \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-107">**HTTPAPI\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-httpapi_version)
-   [<span data-ttu-id="ec381-108">**\_intervalo de bytes http \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-108">**HTTP\_BYTE\_RANGE**</span></span>](/windows/desktop/api/Http/ns-http-http_byte_range)
-   [<span data-ttu-id="ec381-109">**\_Directiva de caché http \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-109">**HTTP\_CACHE\_POLICY**</span></span>](/windows/desktop/api/Http/ns-http-http_cache_policy)
-   [<span data-ttu-id="ec381-110">**URL de HTTP \_ cocida \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-110">**HTTP\_COOKED\_URL**</span></span>](/windows/desktop/api/Http/ns-http-http_cooked_url)
-   [<span data-ttu-id="ec381-111">**\_fragmento de datos HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-111">**HTTP\_DATA\_CHUNK**</span></span>](/windows/desktop/api/Http/ns-http-http_data_chunk)
-   [<span data-ttu-id="ec381-112">**\_encabezado HTTP conocido \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-112">**HTTP\_KNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_known_header)
-   <span data-ttu-id="ec381-113">[**\_solicitud http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec381-113">[**HTTP\_REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85))</span></span>
-   [<span data-ttu-id="ec381-114">**\_encabezados de solicitud HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-114">**HTTP\_REQUEST\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_request_headers)
-   [<span data-ttu-id="ec381-115">**\_respuesta http**</span><span class="sxs-lookup"><span data-stu-id="ec381-115">**HTTP\_RESPONSE**</span></span>](http-response.md)
-   [<span data-ttu-id="ec381-116">**\_encabezados de respuesta HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-116">**HTTP\_RESPONSE\_HEADERS**</span></span>](/windows/desktop/api/Http/ns-http-http_response_headers)
-   [<span data-ttu-id="ec381-117">**\_parámetro de \_ \_ escucha IP \_ de configuración de servicio HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-117">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_param)
-   [<span data-ttu-id="ec381-118">**\_consulta de \_ escucha de IP de configuración de servicio HTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-118">**HTTP\_SERVICE\_CONFIG\_IP\_LISTEN\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ip_listen_query)
-   [<span data-ttu-id="ec381-119">**\_ \_ clave SSL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-119">**HTTP\_SERVICE\_CONFIG\_SSL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_key)
-   [<span data-ttu-id="ec381-120">**\_ \_ parámetro SSL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-120">**HTTP\_SERVICE\_CONFIG\_SSL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_param)
-   [<span data-ttu-id="ec381-121">**\_ \_ consulta SSL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-121">**HTTP\_SERVICE\_CONFIG\_SSL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_query)
-   [<span data-ttu-id="ec381-122">**\_ \_ conjunto SSL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-122">**HTTP\_SERVICE\_CONFIG\_SSL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set)
-   [<span data-ttu-id="ec381-123">**\_ \_ \_ \_ clave SNI SSL de configuración del servicio HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-123">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_key)
-   [<span data-ttu-id="ec381-124">**\_consulta de \_ \_ SSL \_ SNI \_ de configuración del servicio http**</span><span class="sxs-lookup"><span data-stu-id="ec381-124">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_query)
-   [<span data-ttu-id="ec381-125">**\_ \_ \_ \_ conjunto SNI SSL de configuración de servicio HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-125">**HTTP\_SERVICE\_CONFIG\_SSL\_SNI\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_ssl_sni_set)
-   [<span data-ttu-id="ec381-126">**\_ \_ clave URLACL de configuración de servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-126">**HTTP\_SERVICE\_CONFIG\_URLACL\_KEY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_key)
-   [<span data-ttu-id="ec381-127">**\_ \_ parámetro URLACL de configuración de servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-127">**HTTP\_SERVICE\_CONFIG\_URLACL\_PARAM**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_param)
-   [<span data-ttu-id="ec381-128">**\_consulta de \_ URLACL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-128">**HTTP\_SERVICE\_CONFIG\_URLACL\_QUERY**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_query)
-   [<span data-ttu-id="ec381-129">**\_conjunto de \_ URLACL de configuración del servicio HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-129">**HTTP\_SERVICE\_CONFIG\_URLACL\_SET**</span></span>](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set)
-   [<span data-ttu-id="ec381-130">**\_información de \_ certificado de cliente SSL \_ de http \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-130">**HTTP\_SSL\_CLIENT\_CERT\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_client_cert_info)
-   [<span data-ttu-id="ec381-131">**\_información SSL de http \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-131">**HTTP\_SSL\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_ssl_info)
-   [<span data-ttu-id="ec381-132">**\_dirección de transporte HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-132">**HTTP\_TRANSPORT\_ADDRESS**</span></span>](/windows/desktop/api/Http/ns-http-http_transport_address)
-   [<span data-ttu-id="ec381-133">**\_encabezado HTTP desconocido \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-133">**HTTP\_UNKNOWN\_HEADER**</span></span>](/windows/desktop/api/Http/ns-http-http_unknown_header)
-   [<span data-ttu-id="ec381-134">**versión de HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="ec381-134">**HTTP\_VERSION**</span></span>](/windows/desktop/api/Http/ns-http-http_version)

## <a name="related-topics"></a><span data-ttu-id="ec381-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec381-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec381-136">Funciones de la API del servidor HTTP versión 1,0</span><span class="sxs-lookup"><span data-stu-id="ec381-136">HTTP Server API Version 1.0 Functions</span></span>](http-server-api-version-1-0-functions.md)
</dt> </dl>

 

 