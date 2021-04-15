---
description: Siempre se debe tener cuidado para tener en cuenta las diferencias entre el orden de bytes utilizado para almacenar enteros por la arquitectura de host y el orden de bytes que se usa en la conexión mediante protocolos de transporte individuales.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordenación de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497470"
---
# <a name="byte-ordering"></a><span data-ttu-id="fcb6f-103">ordenación de bytes</span><span class="sxs-lookup"><span data-stu-id="fcb6f-103">Byte Ordering</span></span>

<span data-ttu-id="fcb6f-104">Siempre se debe tener cuidado para tener en cuenta las diferencias entre el orden de bytes utilizado para almacenar enteros por la arquitectura de host y el orden de bytes que se usa en la conexión mediante protocolos de transporte individuales.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="fcb6f-105">Cualquier referencia a una dirección o número de Puerto pasado a o desde una rutina de Windows Sockets debe estar en el orden de la red (Big-endian) para el protocolo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="fcb6f-106">En el caso de IP, incluye los parámetros de puerto y dirección IP de una estructura [**sockaddr**](sockaddr-2.md) (pero no el parámetro de la *\_ familia sin* ).</span><span class="sxs-lookup"><span data-stu-id="fcb6f-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="fcb6f-107">Varios sistemas UNIX operan en CPU que representan enteros en el orden de bytes de la red (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="fcb6f-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="fcb6f-108">Por lo tanto, la necesidad de convertir enteros del orden de bytes del host al orden de bytes de la red se puede omitir sin causar problemas, incluso si no se recomienda para la portabilidad.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="fcb6f-109">En cambio, el orden de los bytes utilizado para representar enteros en la mayoría de las CPU de Intel® es Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="fcb6f-110">Por lo tanto, se convierte en obligatorio que los enteros se conviertan del orden de bytes del host al orden de bytes de red antes de usarse en las estructuras y funciones de sockets Winsock.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="fcb6f-111">Considere una aplicación que normalmente se pone en contacto con un servidor en el puerto TCP correspondiente al servicio de hora, pero proporciona un mecanismo para que el usuario especifique un puerto alternativo.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="fcb6f-112">El número de Puerto devuelto por [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) ya está en el orden de la red, que es el formato necesario para construir una dirección, de modo que no se requiere ninguna traducción.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="fcb6f-113">Sin embargo, si el usuario decide usar un puerto diferente, especificado como un entero, la aplicación debe convertirlo del host al orden de la red TCP/IP (mediante la función [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) antes de usarlo para construir una dirección.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="fcb6f-114">Por el contrario, si la aplicación mostrara el número de puerto en una dirección (devuelto por [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) por ejemplo), el número de puerto se debe convertir de la red al orden del host (mediante la función [**NTOHS**](/windows/desktop/api/winsock/nf-winsock-ntohs) o [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) antes de que se pueda mostrar.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="fcb6f-115">Como los pedidos de bytes de Internet e Intel son diferentes, las conversiones descritas en el anterior son inevitables.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="fcb6f-116">Se recomienda a los escritores de aplicaciones que utilicen las funciones de conversión estándar que se proporcionan como parte de Winsock en lugar de escribir su propio código de conversión, ya que es probable que las implementaciones futuras de Winsock se ejecuten en sistemas para los que el orden del host es idéntico al orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="fcb6f-117">Solo es posible que las aplicaciones que usan las funciones de conversión estándar entre el host y el orden de bytes de la red sean portátiles.</span><span class="sxs-lookup"><span data-stu-id="fcb6f-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcb6f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcb6f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb6f-119">**getpeername**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="fcb6f-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="fcb6f-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="fcb6f-122">**htons**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="fcb6f-123">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="fcb6f-124">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="fcb6f-125">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="fcb6f-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="fcb6f-126">**sockaddr**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="fcb6f-127">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="fcb6f-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="fcb6f-128">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="fcb6f-129">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="fcb6f-130">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="fcb6f-131">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="fcb6f-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



