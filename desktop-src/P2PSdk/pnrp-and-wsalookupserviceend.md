---
description: PNRP usa la función WSALookupServiceEnd para hacer lo siguiente.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP y WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667929"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="eb048-103">PNRP y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="eb048-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="eb048-104">PNRP usa la función [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb048-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="eb048-105">Finalizar una consulta iniciada en una llamada anterior a [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="eb048-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="eb048-106">Desbloquear una llamada a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para detener la búsqueda</span><span class="sxs-lookup"><span data-stu-id="eb048-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="eb048-107">Una llamada a [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) finaliza una consulta y limpia el contexto.</span><span class="sxs-lookup"><span data-stu-id="eb048-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="eb048-108">El identificador obtenido a partir de una llamada a **WSALookupServiceBegin** se debe pasar como un parámetro a **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="eb048-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="eb048-109">Para obtener más información acerca de PNRP y la función [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consulte [PNRP y WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="eb048-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb048-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb048-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb048-111">PNRP y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="eb048-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="eb048-112">Códigos de error NSP de PNRP</span><span class="sxs-lookup"><span data-stu-id="eb048-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="eb048-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="eb048-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



