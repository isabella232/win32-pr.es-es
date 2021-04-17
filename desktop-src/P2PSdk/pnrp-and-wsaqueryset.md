---
description: PNRP usa la estructura WSAQUERYSET junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP y WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667928"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="c92b5-103">PNRP y WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="c92b5-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="c92b5-104">PNRP usa la estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) junto con varias funciones para facilitar la resolución de nombres y la enumeración de nombres y nubes.</span><span class="sxs-lookup"><span data-stu-id="c92b5-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="c92b5-105">Para obtener definiciones completas de las funciones de [**WSAQUERYSET**](winsock-nsp-reference-links.md) o Windows Sockets, consulte sus correspondientes definiciones en la documentación de la API de Windows Sockets 2 en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c92b5-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="c92b5-106">WSAQUERYSET y WSASetService</span><span class="sxs-lookup"><span data-stu-id="c92b5-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="c92b5-107">La función [**WSASetService**](winsock-nsp-reference-links.md) utiliza la estructura **WSAQUERYSET** para registrar o quitar nombres de mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c92b5-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="c92b5-108">En la página [PNRP y WSASetService](pnrp-and-wsasetservice.md) se describe el uso de la estructura **WSAQUERYSET** con esta función.</span><span class="sxs-lookup"><span data-stu-id="c92b5-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="c92b5-109">WSAQUERYSET y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="c92b5-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="c92b5-110">La estructura [**WSAQUERYSET**](winsock-nsp-reference-links.md) se usa en gran medida con las funciones **WSALookupServiceBegin**, **WSALookupServiceNext** y **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="c92b5-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="c92b5-111">Los detalles sobre cómo estas funciones usan la estructura **WSAQUERYSET** se detallan en las páginas de referencia siguientes:</span><span class="sxs-lookup"><span data-stu-id="c92b5-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="c92b5-112">PNRP y WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="c92b5-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="c92b5-113">PNRP y WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="c92b5-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="c92b5-114">PNRP y WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="c92b5-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="c92b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c92b5-115">Requirements</span></span>



| <span data-ttu-id="c92b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c92b5-116">Requirement</span></span> | <span data-ttu-id="c92b5-117">Value</span><span class="sxs-lookup"><span data-stu-id="c92b5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c92b5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c92b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c92b5-119">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c92b5-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c92b5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c92b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c92b5-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c92b5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c92b5-122">Versión</span><span class="sxs-lookup"><span data-stu-id="c92b5-122">Version</span></span><br/>                  | <span data-ttu-id="c92b5-123">Windows XP con SP1 con Advanced Networking Pack para Windows XP</span><span class="sxs-lookup"><span data-stu-id="c92b5-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="c92b5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c92b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c92b5-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="c92b5-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c92b5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c92b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92b5-127">PNRP y BLOB</span><span class="sxs-lookup"><span data-stu-id="c92b5-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="c92b5-128">PNRP y WSASetService</span><span class="sxs-lookup"><span data-stu-id="c92b5-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




