---
description: La función GetHostName (usa la función WSALookupServiceBegin para consultar el \_ nombre de host de SVCID como el GUID de la clase de servicio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Función GetHostName (en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715129"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="c3d84-103">Función GetHostName (en la API</span><span class="sxs-lookup"><span data-stu-id="c3d84-103">gethostname Function in the API</span></span>

<span data-ttu-id="c3d84-104">La función [**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa la función [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar el \_ nombre de host de SVCID como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="c3d84-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="c3d84-105">Si el miembro **lpszServiceInstanceName** de la estructura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) pasada a la función **WSALookupServiceBegin** es **null** o hace referencia a una cadena **nula** (es decir,</span><span class="sxs-lookup"><span data-stu-id="c3d84-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="c3d84-106">""), el host local se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="c3d84-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="c3d84-107">De lo contrario, se produce una búsqueda en un nombre de host especificado.</span><span class="sxs-lookup"><span data-stu-id="c3d84-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="c3d84-108">Con el fin de emular **GetHostName (** , el Ws2 \_32.dll especifica un puntero **nulo** para el miembro **lpszServiceInstanceName** y especifica LUP \_ nombre devuelto para \_ que el nombre de host se devuelva en el miembro **lpszServiceInstanceName** .</span><span class="sxs-lookup"><span data-stu-id="c3d84-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="c3d84-109">Si una aplicación usa esta consulta y especifica LUP \_ Return \_ addr, la dirección del host se proporciona en una estructura de [**\_ información de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="c3d84-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="c3d84-110">La \_ acción devolver \_ BLOB de LUP no está definida para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="c3d84-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="c3d84-111">El valor predeterminado de la información de puerto es cero, a menos que el miembro **lpszQueryString** de la estructura **WSAQUERYSET** que se pasa a la función **WSALookupServiceBegin** haga referencia a un servicio como FTP, en cuyo caso se proporciona la dirección de transporte completa del servicio indicado.</span><span class="sxs-lookup"><span data-stu-id="c3d84-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3d84-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3d84-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3d84-113">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="c3d84-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="c3d84-114">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="c3d84-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="c3d84-115">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="c3d84-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
