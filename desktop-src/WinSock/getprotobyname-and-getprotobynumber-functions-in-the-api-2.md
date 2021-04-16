---
description: Las funciones getprotobyname y getprotobynumber se implementan en el \_32.dll Ws2 mediante la consulta de una base de datos de protocolos locales. No dan como resultado ninguna consulta de resolución de nombres.
ms.assetid: e344c580-c81b-446a-93bb-6acf8f5a9f17
title: Funciones getprotobyname y getprotobynumber en la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4b507b79ba349b989ca4b2ef6aa67d77316f05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696383"
---
# <a name="getprotobyname-and-getprotobynumber-functions-in-the-api"></a><span data-ttu-id="481f6-104">Funciones getprotobyname y getprotobynumber en la API</span><span class="sxs-lookup"><span data-stu-id="481f6-104">getprotobyname and getprotobynumber Functions in the API</span></span>

<span data-ttu-id="481f6-105">Las funciones [**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname) y [**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber) se implementan en el \_32.dll Ws2 mediante la consulta de una base de datos de protocolos locales.</span><span class="sxs-lookup"><span data-stu-id="481f6-105">The [**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname) and [**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber) functions are implemented within the Ws2\_32.dll by consulting a local protocols database.</span></span> <span data-ttu-id="481f6-106">No dan como resultado ninguna consulta de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="481f6-106">They do not result in any name resolution query.</span></span>

## <a name="related-topics"></a><span data-ttu-id="481f6-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="481f6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="481f6-108">Resolución de nombres compatible para TCP/IP en la API de Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="481f6-108">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="481f6-109">Resolución de nombres independiente del Protocolo</span><span class="sxs-lookup"><span data-stu-id="481f6-109">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="481f6-110">Registro y resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="481f6-110">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



