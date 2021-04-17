---
description: Se produce cuando los datos están disponibles en la respuesta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Evento IWinHttpRequestEvents:: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678051"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="d92c2-103">Evento IWinHttpRequestEvents:: OnResponseDataAvailable</span><span class="sxs-lookup"><span data-stu-id="d92c2-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="d92c2-104">El evento **OnResponseDataAvailable** se produce cuando los datos están disponibles en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d92c2-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="d92c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d92c2-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="d92c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d92c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d92c2-107">*Datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d92c2-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d92c2-108">Matriz de bytes de base cero que recibe los datos de respuesta recibidos por los servicios HTTP de Microsoft Windows (WinHTTP) hasta el punto en que se produce este evento.</span><span class="sxs-lookup"><span data-stu-id="d92c2-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="d92c2-109">Se trata de una **variante** de tipo VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="d92c2-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d92c2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d92c2-110">Return value</span></span>

<span data-ttu-id="d92c2-111">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d92c2-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92c2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d92c2-112">Remarks</span></span>

<span data-ttu-id="d92c2-113">Dado que los datos se encuentran en bytes, se deben convertir a caracteres anchos cuando se colocan en una cadena de caracteres anchos (Unicode).</span><span class="sxs-lookup"><span data-stu-id="d92c2-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="d92c2-114">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="d92c2-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d92c2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92c2-115">Requirements</span></span>



| <span data-ttu-id="d92c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92c2-116">Requirement</span></span> | <span data-ttu-id="d92c2-117">Value</span><span class="sxs-lookup"><span data-stu-id="d92c2-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d92c2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d92c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d92c2-119">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="d92c2-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d92c2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d92c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d92c2-121">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="d92c2-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d92c2-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d92c2-122">Redistributable</span></span><br/>          | <span data-ttu-id="d92c2-123">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d92c2-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d92c2-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d92c2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d92c2-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d92c2-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92c2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d92c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92c2-127">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="d92c2-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="d92c2-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d92c2-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d92c2-129">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d92c2-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




