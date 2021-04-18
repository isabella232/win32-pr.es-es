---
title: Url
description: Los elementos de la API de URL de WWSAPI proporcionan mecanismos para dividir y deshacer el escape de las direcciones URL en partes componentes, y para volver a combinar las partes componentes en una dirección URL.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- Servicios Web de URL para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2020
ms.locfileid: "105704909"
---
# <a name="url"></a><span data-ttu-id="62345-106">Url</span><span class="sxs-lookup"><span data-stu-id="62345-106">Url</span></span>

<span data-ttu-id="62345-107">Los elementos de la API de URL de WWSAPI proporcionan mecanismos para dividir y deshacer el escape de las direcciones URL en partes componentes, y para volver a combinar las partes componentes en una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="62345-107">The WWSAPI URL API elements provide mechanisms to split and unescape URLs into component parts, and to escape and combine component parts back into a URL.</span></span>

-   <span data-ttu-id="62345-108">Para dividir las direcciones URL y unescape en partes componentes, use la función [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) .</span><span class="sxs-lookup"><span data-stu-id="62345-108">To split and unescape URLs into component parts, use the [**WsDecodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) function.</span></span>
-   <span data-ttu-id="62345-109">Para escapar y combinar partes de componentes en una dirección URL, use la función [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) .</span><span class="sxs-lookup"><span data-stu-id="62345-109">To escape and combine component parts back into a URL, use the [**WsEncodeUrl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) function.</span></span>
-   <span data-ttu-id="62345-110">Para combinar direcciones URL relativas con una dirección URL base absoluta que forme una dirección URL absoluta, utilice la función [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) .</span><span class="sxs-lookup"><span data-stu-id="62345-110">To combine relative URLs with an absolute base URL forming an absolute URL, use the [**WsCombineUrl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) function.</span></span>

<span data-ttu-id="62345-111">Las enumeraciones siguientes forman parte de la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="62345-111">The following enumerations are part of the URL:</span></span>

-   [<span data-ttu-id="62345-112">**\_marcas de URL de WS \_**</span><span class="sxs-lookup"><span data-stu-id="62345-112">**WS\_URL\_FLAGS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="62345-113">**\_tipo de esquema de dirección URL de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="62345-113">**WS\_URL\_SCHEME\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

<span data-ttu-id="62345-114">Las siguientes funciones forman parte de la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="62345-114">The following functions are part of the URL:</span></span>

-   [<span data-ttu-id="62345-115">**WsCombineUrl**</span><span class="sxs-lookup"><span data-stu-id="62345-115">**WsCombineUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [<span data-ttu-id="62345-116">**WsDecodeUrl**</span><span class="sxs-lookup"><span data-stu-id="62345-116">**WsDecodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [<span data-ttu-id="62345-117">**WsEncodeUrl**</span><span class="sxs-lookup"><span data-stu-id="62345-117">**WsEncodeUrl**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

<span data-ttu-id="62345-118">Las siguientes estructuras forman parte de la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="62345-118">The following structures are part of the URL:</span></span>

-   [<span data-ttu-id="62345-119">**URL de WS \_ https \_**</span><span class="sxs-lookup"><span data-stu-id="62345-119">**WS\_HTTPS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [<span data-ttu-id="62345-120">**URL de WS \_ http \_**</span><span class="sxs-lookup"><span data-stu-id="62345-120">**WS\_HTTP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [<span data-ttu-id="62345-121">**URL de WS \_ NETPIPE \_**</span><span class="sxs-lookup"><span data-stu-id="62345-121">**WS\_NETPIPE\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="62345-122">**URL de WS \_ NETTCP \_**</span><span class="sxs-lookup"><span data-stu-id="62345-122">**WS\_NETTCP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [<span data-ttu-id="62345-123">**URL de WS \_ SOAPUDP \_**</span><span class="sxs-lookup"><span data-stu-id="62345-123">**WS\_SOAPUDP\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [<span data-ttu-id="62345-124">**URL de WS \_**</span><span class="sxs-lookup"><span data-stu-id="62345-124">**WS\_URL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




