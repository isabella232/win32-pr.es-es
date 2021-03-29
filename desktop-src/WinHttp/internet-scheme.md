---
description: Esquemas de Internet compatibles con WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912410"
---
# <a name="internet_scheme"></a><span data-ttu-id="b3e3a-103">esquema de INTERNET \_</span><span class="sxs-lookup"><span data-stu-id="b3e3a-103">INTERNET\_SCHEME</span></span>

<span data-ttu-id="b3e3a-104">Esquemas de Internet compatibles con WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-104">Internet schemes supported by WinHTTP.</span></span>

<dl> <dt>

<span data-ttu-id="b3e3a-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**esquema de INTERNET \_ \_ http**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-105"><span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**INTERNET\_SCHEME\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e3a-106">1</span><span class="sxs-lookup"><span data-stu-id="b3e3a-106">1</span></span>
</dt> <dt>



<span data-ttu-id="b3e3a-107">Un esquema HTTP de Internet.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-107">An HTTP internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3e3a-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**esquema de INTERNET \_ \_ https**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-108"><span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**INTERNET\_SCHEME\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e3a-109">2</span><span class="sxs-lookup"><span data-stu-id="b3e3a-109">2</span></span>
</dt> <dt>



<span data-ttu-id="b3e3a-110">Un esquema de Internet HTTPS (SSL).</span><span class="sxs-lookup"><span data-stu-id="b3e3a-110">An HTTPS (SSL) internet scheme.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3e3a-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**esquema de INTERNET \_ \_ FTP**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-111"><span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**INTERNET\_SCHEME\_FTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e3a-112">3</span><span class="sxs-lookup"><span data-stu-id="b3e3a-112">3</span></span>
</dt> <dt>



<span data-ttu-id="b3e3a-113">Un esquema de Internet FTP.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-113">An FTP internet scheme.</span></span> <span data-ttu-id="b3e3a-114">Este esquema solo se admite para su uso en [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="b3e3a-114">This scheme is only supported for use in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) and [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b3e3a-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**esquema de INTERNET \_ \_ Socks**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-115"><span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**INTERNET\_SCHEME\_SOCKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e3a-116">4</span><span class="sxs-lookup"><span data-stu-id="b3e3a-116">4</span></span>
</dt> <dt>



<span data-ttu-id="b3e3a-117">Un esquema de Internet SOCKS.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-117">A SOCKS internet scheme.</span></span> <span data-ttu-id="b3e3a-118">Este esquema solo se admite para su uso en la [**\_ entrada de \_ resultados \_ del proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span><span class="sxs-lookup"><span data-stu-id="b3e3a-118">This scheme is only supported for use in [**WINHTTP\_PROXY\_RESULT\_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3e3a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3e3a-119">Requirements</span></span>



| <span data-ttu-id="b3e3a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e3a-120">Requirement</span></span> | <span data-ttu-id="b3e3a-121">Value</span><span class="sxs-lookup"><span data-stu-id="b3e3a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e3a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3e3a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e3a-123">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="b3e3a-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="b3e3a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3e3a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e3a-125">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="b3e3a-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="b3e3a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3e3a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3e3a-127"><dt>Winhttp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e3a-127"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e3a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3e3a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e3a-129">**\_entrada de \_ resultado del proxy WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-129">**WINHTTP\_PROXY\_RESULT\_ENTRY**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




