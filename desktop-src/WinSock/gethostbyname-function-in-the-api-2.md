---
description: Función gethostbyname en la API de Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Función gethostbyname en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154283"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="acc50-103">Función gethostbyname en la API</span><span class="sxs-lookup"><span data-stu-id="acc50-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="acc50-104">La función [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa la función [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTADDRBYNAME como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="acc50-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="acc50-105">El nombre de host se proporciona en el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) que se pasa a la función **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="acc50-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="acc50-106">El \_32.dll Ws2 especifica LUP \_ devolverá el \_ BLOB y el proveedor de servicios de nombres coloca una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en el BLOB (mediante desplazamientos en lugar de punteros, como se describió anteriormente).</span><span class="sxs-lookup"><span data-stu-id="acc50-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="acc50-107">Los proveedores de servicios de nombres deben cumplir \_ también estas otras \_ \* marcas de devolución de LUP.</span><span class="sxs-lookup"><span data-stu-id="acc50-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="acc50-108">Marca</span><span class="sxs-lookup"><span data-stu-id="acc50-108">Flag</span></span>              | <span data-ttu-id="acc50-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="acc50-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc50-110">\_nombre devuelto de LUP \_</span><span class="sxs-lookup"><span data-stu-id="acc50-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="acc50-111">Devuelve el miembro de **\_ nombre h** de la estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="acc50-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="acc50-112">LUP \_ devolver \_ dirección</span><span class="sxs-lookup"><span data-stu-id="acc50-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="acc50-113">Devuelve la información de dirección de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) en las estructuras de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . el valor predeterminado de la información de puerto es cero.</span><span class="sxs-lookup"><span data-stu-id="acc50-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="acc50-114">Tenga en cuenta que esta rutina no resuelve los nombres de host que se componen de una dirección IPv4 con puntos.</span><span class="sxs-lookup"><span data-stu-id="acc50-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="acc50-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acc50-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc50-116">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="acc50-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="acc50-117">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="acc50-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="acc50-118">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="acc50-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
