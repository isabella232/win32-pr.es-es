---
title: Bluetooth y función getaddrinfo
description: La función función getaddrinfo proporciona traducción desde el nombre de host a la dirección para los transportes basados en IP. Dado que la función función getaddrinfo es específica de los transportes basados en IP, se produce un error en los sockets Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth y función getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793539"
---
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="6537b-105">Bluetooth y función getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="6537b-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="6537b-106">La función [**función getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) proporciona traducción desde el nombre de host a la dirección para los transportes basados en IP.</span><span class="sxs-lookup"><span data-stu-id="6537b-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="6537b-107">Dado que la función **función getaddrinfo** es específica de los transportes basados en IP, se produce un error en los sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="6537b-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="6537b-108">Para realizar la traducción desde el nombre de host a la dirección para los sockets de Bluetooth, use la función [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con **\_ contenedores LUP** para consultar los dispositivos remotos y, a continuación, busque un nombre remoto coincidente específico y la dirección correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6537b-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6537b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6537b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6537b-110">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6537b-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="6537b-111">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="6537b-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="6537b-112">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="6537b-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 