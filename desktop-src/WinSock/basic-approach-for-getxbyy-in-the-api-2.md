---
description: La mayoría de las funciones de getXbyY se traducen mediante el Ws2 \_32.dll a una secuencia WSALookupServiceBegin, WSALookupServiceNext y WSALookupServiceEnd que usa uno de los conjuntos de GUID especiales como clase de servicio.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Enfoque básico para GetXbyY en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541635"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="ba265-103">Enfoque básico para GetXbyY en la API</span><span class="sxs-lookup"><span data-stu-id="ba265-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="ba265-104">La mayoría de las funciones de **getXbyY** se traducen mediante el Ws2 \_32.dll a una secuencia [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)y [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de los conjuntos de GUID especiales como clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="ba265-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="ba265-105">Estos GUID identifican el tipo de operación **getXbyY** que se está emulando.</span><span class="sxs-lookup"><span data-stu-id="ba265-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="ba265-106">La consulta está restringida a los proveedores de servicios de nombres que admiten AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="ba265-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="ba265-107">Cada vez que una función **getXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , el \_32.dll Ws2 especifica el \_ indicador LUP Return \_ BLOB en **WSALookupServiceBegin** para que el proveedor de servicios de nombres devuelva la información deseada.</span><span class="sxs-lookup"><span data-stu-id="ba265-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="ba265-108">Estas estructuras deben modificarse ligeramente en que los punteros contenidos en deben reemplazarse por desplazamientos que son relativos al inicio de los datos del BLOB.</span><span class="sxs-lookup"><span data-stu-id="ba265-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="ba265-109">Todos los valores a los que hacen referencia estos parámetros de puntero deben, por supuesto, estar contenidos completamente dentro del BLOB y todas las cadenas son ASCII.</span><span class="sxs-lookup"><span data-stu-id="ba265-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba265-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba265-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba265-111">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="ba265-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="ba265-112">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="ba265-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="ba265-113">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="ba265-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



