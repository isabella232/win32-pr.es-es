---
description: Proporciona eventos para los servicios HTTP de Microsoft Windows (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interfaz IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678293"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="ce078-103">Interfaz IWinHttpRequestEvents</span><span class="sxs-lookup"><span data-stu-id="ce078-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="ce078-104">La interfaz **IWinHttpRequestEvents** proporciona eventos para los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="ce078-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="ce078-105">Solo usa métodos de evento.</span><span class="sxs-lookup"><span data-stu-id="ce078-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="ce078-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce078-106">Members</span></span>

<span data-ttu-id="ce078-107">La interfaz **IWinHttpRequestEvents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ce078-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ce078-108">**IWinHttpRequestEvents** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ce078-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="ce078-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce078-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ce078-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce078-110">Methods</span></span>

<span data-ttu-id="ce078-111">La interfaz **IWinHttpRequestEvents** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ce078-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="ce078-112">Método</span><span class="sxs-lookup"><span data-stu-id="ce078-112">Method</span></span>                                                                           | <span data-ttu-id="ce078-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce078-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="ce078-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="ce078-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="ce078-115">Se produce cuando hay un error de tiempo de ejecución en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce078-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="ce078-116">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="ce078-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="ce078-117">Se produce cuando los datos están disponibles en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce078-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="ce078-118">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="ce078-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="ce078-119">Se produce cuando se completan los datos de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce078-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="ce078-120">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="ce078-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="ce078-121">Se produce cuando se inicia la recepción de los datos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce078-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="ce078-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce078-122">Remarks</span></span>

<span data-ttu-id="ce078-123">En el procedimiento siguiente se describe cómo registrarse para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ce078-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="ce078-124">Obtenga una interfaz [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) llamando a **QueryInterface** en un objeto [**IWinHttpRequest**](iwinhttprequest-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ce078-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="ce078-125">Llame a [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) en la interfaz devuelta y pase **IID \_ IWinHttpRequestEvents** a *riid*.</span><span class="sxs-lookup"><span data-stu-id="ce078-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="ce078-126">Llame a [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) en el punto de conexión devuelto y pase un puntero a una interfaz **IUnknown** en un objeto que implemente **IWinHttpRequestEvents** en *pUnk*.</span><span class="sxs-lookup"><span data-stu-id="ce078-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="ce078-127">Las notificaciones se pueden finalizar llamando a [unvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) en el punto de conexión devuelto en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="ce078-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="ce078-128">Para ver algún código que se registra para las notificaciones COM, consulte la sección Client del artículo [puntos de conexión com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="ce078-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="ce078-129">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="ce078-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce078-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce078-130">Requirements</span></span>



| <span data-ttu-id="ce078-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce078-131">Requirement</span></span> | <span data-ttu-id="ce078-132">Value</span><span class="sxs-lookup"><span data-stu-id="ce078-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce078-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce078-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ce078-134">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="ce078-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ce078-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce078-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ce078-136">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="ce078-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ce078-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ce078-137">Redistributable</span></span><br/>          | <span data-ttu-id="ce078-138">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ce078-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ce078-139">IDL</span><span class="sxs-lookup"><span data-stu-id="ce078-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce078-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce078-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce078-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce078-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce078-142">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ce078-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="ce078-143">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="ce078-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

