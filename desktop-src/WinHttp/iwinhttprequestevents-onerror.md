---
description: Se produce cuando hay un error de tiempo de ejecución en la aplicación.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'IWinHttpRequestEvents:: OnError (evento)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002905"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="cd7f5-103">IWinHttpRequestEvents:: OnError (evento)</span><span class="sxs-lookup"><span data-stu-id="cd7f5-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="cd7f5-104">El evento **OnError** se produce cuando hay un error de tiempo de ejecución en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd7f5-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="cd7f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd7f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7f5-107">*Númeroerror* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd7f5-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7f5-108">Recibe el valor numérico del error.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="cd7f5-109">Los 16 bits inferiores de este número de error corresponden a uno de los errores enumerados en [**los mensajes de error**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="cd7f5-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd7f5-110">*ErrorDescription* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd7f5-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7f5-111">Especifica una breve descripción del error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7f5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd7f5-112">Return value</span></span>

<span data-ttu-id="cd7f5-113">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7f5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd7f5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cd7f5-115">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd7f5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd7f5-116">Requirements</span></span>



| <span data-ttu-id="cd7f5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7f5-117">Requirement</span></span> | <span data-ttu-id="cd7f5-118">Value</span><span class="sxs-lookup"><span data-stu-id="cd7f5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7f5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7f5-120">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="cd7f5-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="cd7f5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7f5-122">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="cd7f5-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="cd7f5-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cd7f5-123">Redistributable</span></span><br/>          | <span data-ttu-id="cd7f5-124">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="cd7f5-125">IDL</span><span class="sxs-lookup"><span data-stu-id="cd7f5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd7f5-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f5-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7f5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd7f5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7f5-128">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="cd7f5-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="cd7f5-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="cd7f5-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="cd7f5-130">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="cd7f5-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




