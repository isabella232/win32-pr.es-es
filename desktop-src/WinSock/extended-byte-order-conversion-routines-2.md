---
description: Windows Sockets 2 no supone que el orden de bytes de la red para todos los protocolos es el mismo.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Rutinas de conversión extendida Byte-Order
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541603"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="33604-103">Rutinas de conversión extendida Byte-Order</span><span class="sxs-lookup"><span data-stu-id="33604-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="33604-104">Windows Sockets 2 no supone que el orden de bytes de la red para todos los protocolos es el mismo.</span><span class="sxs-lookup"><span data-stu-id="33604-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="33604-105">Se proporciona un conjunto de rutinas de conversión para convertir cantidades de 16 y 32 bits a y desde el orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="33604-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="33604-106">Estas rutinas toman como parámetro de entrada el identificador de socket que tiene una estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) asociada.</span><span class="sxs-lookup"><span data-stu-id="33604-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="33604-107">El miembro **NetworkByteOrder** de la estructura de **\_ información de WSAPROTOCOL** especifica el orden de bytes de red deseado (actualmente big-endian o Little-endian).</span><span class="sxs-lookup"><span data-stu-id="33604-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33604-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33604-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33604-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="33604-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="33604-110">**htons**</span><span class="sxs-lookup"><span data-stu-id="33604-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="33604-111">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="33604-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="33604-112">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="33604-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="33604-113">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="33604-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="33604-114">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="33604-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="33604-115">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="33604-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="33604-116">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="33604-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="33604-117">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="33604-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="33604-118">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="33604-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="33604-119">**información de WSAPROTOCOL \_**</span><span class="sxs-lookup"><span data-stu-id="33604-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
