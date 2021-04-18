---
description: Función gethostbyname en el SPI de Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Función gethostbyname en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715130"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="1bc47-103">Función gethostbyname en el SPI</span><span class="sxs-lookup"><span data-stu-id="1bc47-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="1bc47-104">La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTADDRBYNAME como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="1bc47-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="1bc47-105">El nombre de host se proporciona en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="1bc47-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="1bc47-106">El *\_32.dllWS2* especifica LUP \_ devolverá el \_ BLOB y el NSP coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente).</span><span class="sxs-lookup"><span data-stu-id="1bc47-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="1bc47-107">Los NSP deben respetar también estas \_ otras \_ \* marcas de devolución de LUP.</span><span class="sxs-lookup"><span data-stu-id="1bc47-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="1bc47-108">Marca</span><span class="sxs-lookup"><span data-stu-id="1bc47-108">Flag</span></span>              | <span data-ttu-id="1bc47-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bc47-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc47-110">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="1bc47-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="1bc47-111">Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="1bc47-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="1bc47-112">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="1bc47-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="1bc47-113">Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero.</span><span class="sxs-lookup"><span data-stu-id="1bc47-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="1bc47-114">Tenga en cuenta que esta rutina no resuelve los nombres de host que se componen de una cadena de dirección IPv4 decimal con puntos.</span><span class="sxs-lookup"><span data-stu-id="1bc47-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
