---
title: HTTP_RESPONSE (http. h)
description: La versión de la \_ estructura de respuesta http depende de la versión de la cola de solicitudes utilizada como sigue la API de servidor http versión 1,0, que es una \_ estructura de solicitud HTTP \_ v1. API de servidor HTTP versión 2,0 cola de solicitudes es una \_ estructura de solicitud HTTP \_ V2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422183"
---
# <a name="http_response"></a><span data-ttu-id="31510-106">\_respuesta http</span><span class="sxs-lookup"><span data-stu-id="31510-106">HTTP\_RESPONSE</span></span>

<span data-ttu-id="31510-107">La versión de la estructura de **\_ respuesta http** depende de la versión de la cola de solicitudes utilizada como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="31510-107">The version of the **HTTP\_RESPONSE** structure is dependent on the version of the request queue used as follows:</span></span>

-   <span data-ttu-id="31510-108">API de servidor HTTP versión 1,0 cola de solicitudes: se trata de una estructura de [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .</span><span class="sxs-lookup"><span data-stu-id="31510-108">HTTP Server API Version 1.0 request queue: This is an [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) structure.</span></span>
-   <span data-ttu-id="31510-109">API de servidor HTTP versión 2,0 cola de solicitudes: se trata de una estructura de [**\_ solicitud HTTP \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) .</span><span class="sxs-lookup"><span data-stu-id="31510-109">HTTP Server API Version 2.0 request queue: This is an [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) structure.</span></span>

<span data-ttu-id="31510-110">No use la [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) y [**la \_ solicitud HTTP \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directamente en el código; mediante el uso de la **\_ respuesta http** , se asegura de que se usa la versión adecuada de la estructura en función de la versión de la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="31510-110">Do not use [**HTTP\_REQUEST\_V1**](/windows/desktop/api/Http/ns-http-http_request_v1) and [**HTTP\_REQUEST\_V2**](/windows/desktop/api/Http/ns-http-http_request_v2) directly in your code; using **HTTP\_RESPONSE** instead ensures the proper version of the structure is used based on the version of the request queue.</span></span>


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

<span data-ttu-id="31510-111">**\_respuesta http**</span><span class="sxs-lookup"><span data-stu-id="31510-111">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="31510-112">La solicitud fue de una cola de solicitudes v1.</span><span class="sxs-lookup"><span data-stu-id="31510-112">Request was from a v1 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="31510-113">**\_respuesta http**</span><span class="sxs-lookup"><span data-stu-id="31510-113">**HTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="31510-114">La solicitud fue de una cola de solicitudes V2.</span><span class="sxs-lookup"><span data-stu-id="31510-114">Request was from a v2 request queue.</span></span>

</dd> <dt>

<span data-ttu-id="31510-115">**respuesta de PHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="31510-115">**PHTTP\_RESPONSE**</span></span>
</dt> <dd>

<span data-ttu-id="31510-116">Puntero a una estructura de **\_ respuesta http** .</span><span class="sxs-lookup"><span data-stu-id="31510-116">Pointer to an **HTTP\_RESPONSE** structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31510-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31510-117">Requirements</span></span>



| <span data-ttu-id="31510-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="31510-118">Requirement</span></span> | <span data-ttu-id="31510-119">Value</span><span class="sxs-lookup"><span data-stu-id="31510-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="31510-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31510-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31510-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31510-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31510-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31510-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31510-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31510-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31510-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31510-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31510-125"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="31510-125"><dt>Http.h</dt></span></span> </dl> |



 

 





