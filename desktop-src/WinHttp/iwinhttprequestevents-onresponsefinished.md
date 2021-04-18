---
description: Se produce cuando se completan los datos de la respuesta.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Evento IWinHttpRequestEvents:: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706609"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="6cccc-103">Evento IWinHttpRequestEvents:: OnResponseFinished</span><span class="sxs-lookup"><span data-stu-id="6cccc-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="6cccc-104">El evento **OnResponseFinished** se produce cuando se completan los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6cccc-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cccc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cccc-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="6cccc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cccc-106">Parameters</span></span>

<span data-ttu-id="6cccc-107">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6cccc-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cccc-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cccc-108">Return value</span></span>

<span data-ttu-id="6cccc-109">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="6cccc-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cccc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cccc-110">Remarks</span></span>

<span data-ttu-id="6cccc-111">Este evento indica que se han recibido todos los datos de respuesta que pertenecen a la solicitud más reciente.</span><span class="sxs-lookup"><span data-stu-id="6cccc-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="6cccc-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) no vuelve a aparecer hasta la siguiente solicitud.</span><span class="sxs-lookup"><span data-stu-id="6cccc-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="6cccc-113">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="6cccc-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6cccc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cccc-114">Requirements</span></span>



| <span data-ttu-id="6cccc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cccc-115">Requirement</span></span> | <span data-ttu-id="6cccc-116">Value</span><span class="sxs-lookup"><span data-stu-id="6cccc-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cccc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cccc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6cccc-118">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="6cccc-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="6cccc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cccc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6cccc-120">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="6cccc-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="6cccc-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6cccc-121">Redistributable</span></span><br/>          | <span data-ttu-id="6cccc-122">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6cccc-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="6cccc-123">IDL</span><span class="sxs-lookup"><span data-stu-id="6cccc-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cccc-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cccc-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cccc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cccc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cccc-126">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="6cccc-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="6cccc-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="6cccc-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="6cccc-128">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6cccc-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




