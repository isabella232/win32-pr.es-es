---
description: Solicita la salida fotogramas del destino de representación, evento y marco especificados.
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameBufferRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714711"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="6d8dd-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="6d8dd-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="6d8dd-104">Solicita la salida fotogramas del destino de representación, evento y marco especificados.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d8dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d8dd-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="6d8dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d8dd-106">Parameters</span></span>

<span data-ttu-id="6d8dd-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-107">*frameNumber* </span></span>  
<span data-ttu-id="6d8dd-108">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-108">The specified frame.</span></span>

<span data-ttu-id="6d8dd-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-109">*eventID* </span></span>  
<span data-ttu-id="6d8dd-110">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-110">The specified event.</span></span>

<span data-ttu-id="6d8dd-111">*renderTargetIndex* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="6d8dd-112">Índice del destino de representación especificado.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-112">The index of the specified render target.</span></span>

<span data-ttu-id="6d8dd-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-113">*requestCallback* </span></span>  
<span data-ttu-id="6d8dd-114">La dirección de una devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="6d8dd-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-115">*requestCookie* </span></span>  
<span data-ttu-id="6d8dd-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="6d8dd-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="6d8dd-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="6d8dd-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d8dd-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d8dd-119">Return value</span></span>

<span data-ttu-id="6d8dd-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6d8dd-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d8dd-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d8dd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8dd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8dd-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6d8dd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d8dd-123">Header</span></span></p></td><td><span data-ttu-id="6d8dd-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6d8dd-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6d8dd-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="6d8dd-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6d8dd-126">**IFrameBufferRequest**</span><span class="sxs-lookup"><span data-stu-id="6d8dd-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
