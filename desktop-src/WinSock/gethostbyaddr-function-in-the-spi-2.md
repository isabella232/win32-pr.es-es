---
description: La consulta WSALookupServiceBegin usa SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Función gethostbyaddr en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541587"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="84c67-103">Función gethostbyaddr en el SPI</span><span class="sxs-lookup"><span data-stu-id="84c67-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="84c67-104">La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="84c67-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="84c67-105">La dirección de host se proporciona en *lpszServiceInstanceName* como una cadena de dirección IPv4 decimal con puntos (por ejemplo, 192.9.200.120).</span><span class="sxs-lookup"><span data-stu-id="84c67-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="84c67-106">El *\_32.dllWS2* especifica LUP \_ devolverá el \_ BLOB y el NSP coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente).</span><span class="sxs-lookup"><span data-stu-id="84c67-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="84c67-107">Los NSP deben respetar también estas \_ otras \_ \* marcas de devolución de LUP.</span><span class="sxs-lookup"><span data-stu-id="84c67-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="84c67-108">Marca</span><span class="sxs-lookup"><span data-stu-id="84c67-108">Flag</span></span>              | <span data-ttu-id="84c67-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="84c67-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c67-110">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="84c67-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="84c67-111">Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="84c67-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="84c67-112">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="84c67-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="84c67-113">Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero.</span><span class="sxs-lookup"><span data-stu-id="84c67-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
