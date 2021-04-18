---
description: La función gethostbyaddr usa la función WSALookupServiceBegin para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Función gethostbyaddr en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715131"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="86c5d-103">Función gethostbyaddr en la API</span><span class="sxs-lookup"><span data-stu-id="86c5d-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="86c5d-104">La función [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la función [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="86c5d-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="86c5d-105">La dirección del host se proporciona como una cadena IPv4 decimnal con puntos (por ejemplo, "192.9.200.120") en el miembro *lpszServiceInstanceName* de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="86c5d-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="86c5d-106">El \_32.dll Ws2 especifica LUP \_ devolverá el \_ BLOB y el proveedor de servicios de nombres coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente).</span><span class="sxs-lookup"><span data-stu-id="86c5d-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="86c5d-107">Los proveedores de servicios de nombres deben cumplir \_ también estas otras \_ \* marcas de devolución de LUP.</span><span class="sxs-lookup"><span data-stu-id="86c5d-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="86c5d-108">Marca</span><span class="sxs-lookup"><span data-stu-id="86c5d-108">Flag</span></span>              | <span data-ttu-id="86c5d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c5d-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c5d-110">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="86c5d-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="86c5d-111">Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="86c5d-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="86c5d-112">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="86c5d-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="86c5d-113">Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero.</span><span class="sxs-lookup"><span data-stu-id="86c5d-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="86c5d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86c5d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86c5d-115">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="86c5d-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="86c5d-116">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="86c5d-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="86c5d-117">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="86c5d-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
