---
description: La consulta WSALookupServiceBegin usa \_ el nombre de host SVCID como el GUID de la clase de servicio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Función GetHostName (en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715128"
---
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="84eed-103">Función GetHostName (en el SPI</span><span class="sxs-lookup"><span data-stu-id="84eed-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="84eed-104">La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa \_ el nombre de host SVCID como el GUID de la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="84eed-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="84eed-105">Si *lpszServiceInstanceName* es null o hace referencia a una cadena nula (es decir,</span><span class="sxs-lookup"><span data-stu-id="84eed-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="84eed-106">""), el host local se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="84eed-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="84eed-107">De lo contrario, se producirá una búsqueda en un nombre de host especificado.</span><span class="sxs-lookup"><span data-stu-id="84eed-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="84eed-108">Con el fin de emular [**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname) , el \_ valor de Ws232.dll especificará un puntero nulo para *lpszServiceInstanceName* y especificará el nombre de retorno de LUP para \_ \_ que el nombre de host se devuelva en el parámetro *lpszServiceInstanceName* .</span><span class="sxs-lookup"><span data-stu-id="84eed-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="84eed-109">Si una aplicación usa esta consulta y especifica LUP \_ Return \_ addr, la dirección del host se proporcionará en una estructura de **\_ información de CSADDR** .</span><span class="sxs-lookup"><span data-stu-id="84eed-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="84eed-110">La \_ acción devolver \_ BLOB de LUP no está definida para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="84eed-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="84eed-111">La información del puerto se establecerá de forma predeterminada en cero, a menos que el *lpszQueryString* haga referencia a un servicio como FTP, en cuyo caso se proporcionará la dirección de transporte completa del servicio indicado.</span><span class="sxs-lookup"><span data-stu-id="84eed-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



