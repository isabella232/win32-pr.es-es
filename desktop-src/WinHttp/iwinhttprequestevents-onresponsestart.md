---
description: Se produce cuando se inicia la recepción de los datos de respuesta.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706607"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="feb1b-103">Evento IWinHttpRequestEvents:: OnResponseStart</span><span class="sxs-lookup"><span data-stu-id="feb1b-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="feb1b-104">El evento **OnResponseStart** se produce cuando se inicia la recepción de los datos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="feb1b-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb1b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="feb1b-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="feb1b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="feb1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb1b-107">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="feb1b-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb1b-108">Recibe el código de estado estándar devuelto con los datos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="feb1b-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="feb1b-109">Los códigos de estado se definen en [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="feb1b-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="feb1b-110">*ContentType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="feb1b-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb1b-111">Especifica el tipo de contenido recibido, como "text/html" o "image/gif".</span><span class="sxs-lookup"><span data-stu-id="feb1b-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb1b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="feb1b-112">Return value</span></span>

<span data-ttu-id="feb1b-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="feb1b-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb1b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="feb1b-114">Remarks</span></span>

<span data-ttu-id="feb1b-115">Para que se produzca este evento, utilice [**Open**](iwinhttprequest-open.md) para enviar una conexión http en modo asincrónico y utilice [**send**](iwinhttprequest-send.md) para enviar una solicitud de datos a un servidor de Internet.</span><span class="sxs-lookup"><span data-stu-id="feb1b-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="feb1b-116">Este es el primer evento de WinHTTP que debe producirse después del [**envío**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="feb1b-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="feb1b-117">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="feb1b-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="feb1b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb1b-118">Requirements</span></span>



| <span data-ttu-id="feb1b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb1b-119">Requirement</span></span> | <span data-ttu-id="feb1b-120">Value</span><span class="sxs-lookup"><span data-stu-id="feb1b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb1b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb1b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="feb1b-122">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="feb1b-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="feb1b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb1b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="feb1b-124">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="feb1b-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="feb1b-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="feb1b-125">Redistributable</span></span><br/>          | <span data-ttu-id="feb1b-126">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="feb1b-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="feb1b-127">IDL</span><span class="sxs-lookup"><span data-stu-id="feb1b-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="feb1b-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="feb1b-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb1b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="feb1b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb1b-130">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="feb1b-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="feb1b-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="feb1b-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="feb1b-132">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="feb1b-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




