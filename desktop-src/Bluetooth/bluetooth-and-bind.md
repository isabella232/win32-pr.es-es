---
title: Bluetooth y BIND
description: Bluetooth utiliza la función de enlace para enlazar con un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth y BIND
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904798"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="80f8f-107">Bluetooth y BIND</span><span class="sxs-lookup"><span data-stu-id="80f8f-107">Bluetooth and bind</span></span>

<span data-ttu-id="80f8f-108">Bluetooth utiliza la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) para enlazar con un socket.</span><span class="sxs-lookup"><span data-stu-id="80f8f-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="80f8f-109">Para enlazar un Socket Bluetooth, llame a la función **BIND** mediante la estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) .</span><span class="sxs-lookup"><span data-stu-id="80f8f-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="80f8f-110">Use la estructura **SOCKADDR \_ BTH** con la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="80f8f-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="80f8f-111">En las aplicaciones cliente, el miembro del puerto debe ser cero para permitir que se asigne un punto de conexión local adecuado.</span><span class="sxs-lookup"><span data-stu-id="80f8f-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="80f8f-112">En las aplicaciones de servidor, el miembro del puerto debe ser un número de puerto o un puerto BT válido \_ \_ ; los puertos asignados automáticamente mediante \_ el puerto BT \_ Any se pueden consultar posteriormente con una llamada a la función [**getsockname**](bluetooth-and-getsockname.md) .</span><span class="sxs-lookup"><span data-stu-id="80f8f-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="80f8f-113">El intervalo válido para solicitar un puerto RFCOMM específico es de 1 a 30.</span><span class="sxs-lookup"><span data-stu-id="80f8f-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="80f8f-114">Los canales de servidor son recursos globales y solo hay 30 canales de servidor disponibles para RFCOMM en cualquier dispositivo Bluetooth, que deben ser compartidos por todos los Windows Sockets que pertenecen a la familia de direcciones de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="80f8f-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="80f8f-115">Si no hay ningún canal de servidor disponible, o si el canal de servidor especificado ya está reservado, se produce un error en la llamada de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="80f8f-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="80f8f-116">Cuando se devuelve correctamente de BIND, el canal de servidor se reserva hasta que se cierra el socket.</span><span class="sxs-lookup"><span data-stu-id="80f8f-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="80f8f-117">Use la función [**getsockname**](bluetooth-and-getsockname.md) para recuperar el número de canal para el registro de SDP.</span><span class="sxs-lookup"><span data-stu-id="80f8f-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="80f8f-118">Las aplicaciones deben usar la asignación automática para el canal del servidor.</span><span class="sxs-lookup"><span data-stu-id="80f8f-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="80f8f-119">La función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) no anuncia automáticamente la aplicación de servidor mediante el SDP de Bluetooth; las aplicaciones deben llamar a la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para que las aplicaciones Bluetooth remotas las encuentren.</span><span class="sxs-lookup"><span data-stu-id="80f8f-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80f8f-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80f8f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80f8f-121">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="80f8f-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="80f8f-122">**volver**</span><span class="sxs-lookup"><span data-stu-id="80f8f-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 