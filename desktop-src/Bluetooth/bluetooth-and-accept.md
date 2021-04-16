---
title: Bluetooth y aceptar
description: Bluetooth usa la función Accept para habilitar los intentos de conexión entrantes en un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept
- Bluetooth
- Bluetooth
- Bluetooth y aceptar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656386"
---
# <a name="bluetooth-and-accept"></a><span data-ttu-id="8c140-107">Bluetooth y aceptar</span><span class="sxs-lookup"><span data-stu-id="8c140-107">Bluetooth and accept</span></span>

<span data-ttu-id="8c140-108">Bluetooth usa la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar los intentos de conexión entrantes en un socket.</span><span class="sxs-lookup"><span data-stu-id="8c140-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="8c140-109">La \_ Dirección BTH de la aplicación cliente se obtiene al leer la sección específica del transporte Bluetooth de la estructura [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) devuelta.</span><span class="sxs-lookup"><span data-stu-id="8c140-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="8c140-110">El uso de la función **Accept** con Bluetooth tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="8c140-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="8c140-111">El parámetro *addr* de la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un búfer que recibe la dirección de la entidad de conexión, como se conoce en el nivel de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="8c140-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="8c140-112">Se devuelve un puntero a una estructura de [**\_ BTH de SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la dirección del dispositivo Bluetooth remoto.</span><span class="sxs-lookup"><span data-stu-id="8c140-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="8c140-113">El parámetro *addrlen* de la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un entero que contiene la longitud, en bytes, de addr. El entero debe ser mayor o igual que el valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span><span class="sxs-lookup"><span data-stu-id="8c140-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c140-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c140-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c140-115">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="8c140-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="8c140-116">**acept**</span><span class="sxs-lookup"><span data-stu-id="8c140-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 