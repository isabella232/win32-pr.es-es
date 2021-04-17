---
title: Bluetooth y BLOB
description: Bluetooth usa la estructura de BLOBs para pasar o recibir datos específicos del transporte a la estructura WSAQUERYSET durante las llamadas a las funciones WSASetService o WSALookupService \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth y BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656385"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="6730e-107">Bluetooth y BLOB</span><span class="sxs-lookup"><span data-stu-id="6730e-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="6730e-108">Bluetooth usa la estructura de [**blobs**](/windows/desktop/api/nspapi/ns-nspapi-blob) para pasar o recibir datos específicos del transporte a la estructura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante las llamadas a las funciones [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* .</span><span class="sxs-lookup"><span data-stu-id="6730e-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="6730e-109">Para su uso con Bluetooth y la función [**WSASetService**](bluetooth-and-wsasetservice.md) , los miembros de la estructura de [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) deben tener la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="6730e-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="6730e-110">El miembro **cbsize** debe establecerse en el tamaño de la estructura de [**\_ \_ servicio del conjunto BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) que se usa en el miembro **pBlobData** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="6730e-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="6730e-111">El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ servicio establecida en BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="6730e-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="6730e-112">Para su uso con Bluetooth y [WSALookupServiceBegin para la consulta de dispositivos](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="6730e-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="6730e-113">El miembro **cbsize** debe establecerse en el tamaño de la estructura del [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilizada en el miembro **pBlobData** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="6730e-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="6730e-114">El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .</span><span class="sxs-lookup"><span data-stu-id="6730e-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="6730e-115">Para su uso con Bluetooth y [WSALookupServiceBegin para la detección de servicios](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="6730e-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="6730e-116">El miembro **cbsize** debe establecerse en el tamaño de la estructura del [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilizada en el miembro **pBlobData** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="6730e-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="6730e-117">El miembro **pBlobData** debe ser un puntero a una estructura de [**\_ \_ servicio de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .</span><span class="sxs-lookup"><span data-stu-id="6730e-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="6730e-118">Para obtener más información, vea la sección Comentarios en la página de referencia de la estructura de [**\_ \_ servicio de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="6730e-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6730e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6730e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6730e-120">Bluetooth y WSALookupServiceBegin para la consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6730e-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="6730e-121">Bluetooth y WSALookupServiceBegin para la detección de servicios</span><span class="sxs-lookup"><span data-stu-id="6730e-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="6730e-122">Bluetooth y WSASetService</span><span class="sxs-lookup"><span data-stu-id="6730e-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="6730e-123">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6730e-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="6730e-124">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="6730e-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="6730e-125">**\_dispositivo de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="6730e-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="6730e-126">**\_servicio de consulta de BTH \_**</span><span class="sxs-lookup"><span data-stu-id="6730e-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="6730e-127">**BTH \_ establecer \_ servicio**</span><span class="sxs-lookup"><span data-stu-id="6730e-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="6730e-128">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="6730e-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="6730e-129">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="6730e-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="6730e-130">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="6730e-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 