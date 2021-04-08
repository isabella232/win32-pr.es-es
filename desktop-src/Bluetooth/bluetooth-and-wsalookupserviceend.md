---
title: Bluetooth y WSALookupServiceEnd
description: Bluetooth usa la función WSALookupServiceEnd para finalizar una consulta iniciada en una llamada anterior a WSALookupServiceBegin y, quizás, extendida en llamadas posteriores a WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995341"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="43e69-106">Bluetooth y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="43e69-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="43e69-107">Bluetooth usa la función [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para finalizar una consulta iniciada en una llamada anterior a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)y, quizás, extendida en llamadas posteriores a [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="43e69-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="43e69-108">La llamada a **WSALookupServiceEnd** finaliza la consulta y limpia el contexto.</span><span class="sxs-lookup"><span data-stu-id="43e69-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="43e69-109">Los pasos para la consulta de dispositivos y la detección de servicios en Bluetooth son lo suficientemente diferentes como para merecer un trato independiente.</span><span class="sxs-lookup"><span data-stu-id="43e69-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="43e69-110">Para obtener más información sobre Bluetooth y la función [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para las consultas de dispositivos, consulte [Bluetooth y WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)consultar los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="43e69-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="43e69-111">Para obtener más información sobre Bluetooth y la función **WSALookupServiceBegin** para la detección de servicios, consulte [Bluetooth y WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="43e69-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43e69-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43e69-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e69-113">Detección de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="43e69-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="43e69-114">Bluetooth y WSALookupServiceBegin para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="43e69-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="43e69-115">Bluetooth y WSALookupServiceBegin para la detección de servicios</span><span class="sxs-lookup"><span data-stu-id="43e69-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="43e69-116">Bluetooth y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="43e69-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="43e69-117">**\_servicio de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="43e69-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="43e69-118">**conéctelo**</span><span class="sxs-lookup"><span data-stu-id="43e69-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="43e69-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="43e69-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="43e69-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="43e69-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="43e69-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="43e69-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="43e69-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="43e69-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="43e69-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="43e69-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="43e69-124">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="43e69-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 