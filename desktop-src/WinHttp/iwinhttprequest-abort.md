---
description: El método Abort anula un método send de WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'IWinHttpRequest:: ABORT (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002746"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="2bc37-103">IWinHttpRequest:: ABORT (método)</span><span class="sxs-lookup"><span data-stu-id="2bc37-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="2bc37-104">El método **Abort** anula un método [](about-winhttp.md) [**send**](iwinhttprequest-send.md) de winhttp.</span><span class="sxs-lookup"><span data-stu-id="2bc37-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bc37-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="2bc37-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bc37-106">Parameters</span></span>

<span data-ttu-id="2bc37-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2bc37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bc37-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bc37-108">Return value</span></span>

<span data-ttu-id="2bc37-109">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="2bc37-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc37-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bc37-110">Remarks</span></span>

<span data-ttu-id="2bc37-111">Puede anular métodos de [**envío**](iwinhttprequest-send.md) asincrónicos y sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="2bc37-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="2bc37-112">Para anular un método de [**envío**](iwinhttprequest-send.md) sincrónico, debe llamar a **Abort** desde dentro de un evento [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="2bc37-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="2bc37-113">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="2bc37-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bc37-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bc37-114">Requirements</span></span>



| <span data-ttu-id="2bc37-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc37-115">Requirement</span></span> | <span data-ttu-id="2bc37-116">Value</span><span class="sxs-lookup"><span data-stu-id="2bc37-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc37-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bc37-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc37-118">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="2bc37-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2bc37-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bc37-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc37-120">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="2bc37-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2bc37-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2bc37-121">Redistributable</span></span><br/>          | <span data-ttu-id="2bc37-122">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2bc37-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2bc37-123">IDL</span><span class="sxs-lookup"><span data-stu-id="2bc37-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bc37-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bc37-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2bc37-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bc37-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2bc37-126"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bc37-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2bc37-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bc37-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bc37-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bc37-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2bc37-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bc37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc37-130">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2bc37-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="2bc37-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2bc37-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2bc37-132">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2bc37-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




