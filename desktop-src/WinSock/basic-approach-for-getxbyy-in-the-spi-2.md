---
description: La mayoría de las funciones de GetXbyY se traducen mediante Ws2 \_32.dll a una secuencia WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa uno de los conjuntos de GUID especiales como clase de servicio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Enfoque básico para GetXbyY en SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907959"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="0e403-103">Enfoque básico para GetXbyY en SPI</span><span class="sxs-lookup"><span data-stu-id="0e403-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="0e403-104">La mayoría de las funciones de **GetXbyY** se traducen mediante Ws2 \_32.dll a una secuencia [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de los conjuntos de GUID especiales como clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="0e403-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="0e403-105">Estos GUID identifican el tipo de operación **GetXbyY** que se está emulando.</span><span class="sxs-lookup"><span data-stu-id="0e403-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="0e403-106">La consulta está restringida a los NSP que admiten AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="0e403-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="0e403-107">Siempre que una función **GetXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , el \_32.dll Ws2 especificará la \_ marca LUP REturn \_ BLOB en **WSALookupServiceBegin** para que el NSP devuelva la información deseada.</span><span class="sxs-lookup"><span data-stu-id="0e403-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="0e403-108">Estas estructuras deben modificarse ligeramente en que los punteros contenidos en deben reemplazarse por desplazamientos que son relativos al inicio de los datos del BLOB.</span><span class="sxs-lookup"><span data-stu-id="0e403-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="0e403-109">Todos los valores a los que hacen referencia estos miembros de puntero deben, por supuesto, estar contenidos completamente dentro del BLOB y todas las cadenas son ASCII.</span><span class="sxs-lookup"><span data-stu-id="0e403-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



