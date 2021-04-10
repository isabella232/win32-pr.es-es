---
description: Una solicitud asincrónica para obtener información específica sobre un solo marco especificado.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152160"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="1698e-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="1698e-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="1698e-104">Una solicitud asincrónica para obtener información específica sobre un solo marco especificado.</span><span class="sxs-lookup"><span data-stu-id="1698e-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1698e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1698e-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1698e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1698e-106">Parameters</span></span>

<span data-ttu-id="1698e-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="1698e-107">*frameNumber* </span></span>  
<span data-ttu-id="1698e-108">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="1698e-108">The specified frame.</span></span>

<span data-ttu-id="1698e-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="1698e-109">*numColumns* </span></span>  
<span data-ttu-id="1698e-110">Columnas especificadas (campos).</span><span class="sxs-lookup"><span data-stu-id="1698e-110">The specified columns (fields).</span></span>

<span data-ttu-id="1698e-111">*\_columnas count1* </span><span class="sxs-lookup"><span data-stu-id="1698e-111">*count1\_columns* </span></span>  
<span data-ttu-id="1698e-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="1698e-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1698e-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1698e-113">*requestCallback* </span></span>  
<span data-ttu-id="1698e-114">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="1698e-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="1698e-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1698e-115">*requestCookie* </span></span>  
<span data-ttu-id="1698e-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="1698e-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1698e-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1698e-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1698e-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1698e-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1698e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1698e-119">Return value</span></span>

<span data-ttu-id="1698e-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1698e-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1698e-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1698e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1698e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1698e-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1698e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1698e-123">Header</span></span></p></td><td><span data-ttu-id="1698e-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1698e-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1698e-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="1698e-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1698e-126">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="1698e-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
