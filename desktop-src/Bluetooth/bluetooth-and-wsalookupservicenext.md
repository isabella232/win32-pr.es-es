---
title: Bluetooth y WSALookupServiceNext
description: Bluetooth usa la función WSALookupServiceNext para hacer coincidir las consultas especificadas en una llamada anterior a WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth y WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904633"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="d348a-106">Bluetooth y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="d348a-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="d348a-107">Bluetooth usa la función [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para hacer coincidir las consultas especificadas en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span><span class="sxs-lookup"><span data-stu-id="d348a-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="d348a-108">Los resultados de la función **WSALookupServiceNext** se determinan mediante la configuración establecida en la estructura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) pasada en la llamada de función **WSALookupServiceBegin** inicial.</span><span class="sxs-lookup"><span data-stu-id="d348a-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="d348a-109">Los pasos para la consulta de dispositivos y la detección de servicios en Bluetooth son lo suficientemente diferentes como para merecer un trato independiente.</span><span class="sxs-lookup"><span data-stu-id="d348a-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="d348a-110">Para obtener más información sobre Bluetooth y la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para las consultas de dispositivos, consulte [Bluetooth y WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)consultar los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d348a-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="d348a-111">Para obtener más información sobre Bluetooth y la función **WSALookupServiceBegin** para la detección de servicios, consulte [Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d348a-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d348a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d348a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d348a-113">Detección de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d348a-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="d348a-114">Bluetooth y WSALookupServiceBegin para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d348a-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="d348a-115">Bluetooth y WSALookupServiceBegin para la detección de servicios</span><span class="sxs-lookup"><span data-stu-id="d348a-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="d348a-116">Bluetooth y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="d348a-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="d348a-117">**\_servicio de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="d348a-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="d348a-118">**conéctelo**</span><span class="sxs-lookup"><span data-stu-id="d348a-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="d348a-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="d348a-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="d348a-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="d348a-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="d348a-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="d348a-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="d348a-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="d348a-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="d348a-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="d348a-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 