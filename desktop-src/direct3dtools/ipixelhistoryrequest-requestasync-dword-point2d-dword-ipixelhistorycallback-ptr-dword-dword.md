---
description: Solicita una lista de resultados del historial de píxeles en el píxel especificado, render destino/UAV y frame.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538199"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="e2d07-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="e2d07-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="e2d07-104">Solicita una lista de resultados del historial de píxeles en el píxel especificado, render destino/UAV y frame.</span><span class="sxs-lookup"><span data-stu-id="e2d07-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d07-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2d07-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e2d07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2d07-106">Parameters</span></span>

<span data-ttu-id="e2d07-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="e2d07-107">*frameNumber* </span></span>  
<span data-ttu-id="e2d07-108">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="e2d07-108">The specified frame.</span></span>

<span data-ttu-id="e2d07-109">*píxel* </span><span class="sxs-lookup"><span data-stu-id="e2d07-109">*pixel* </span></span>  
<span data-ttu-id="e2d07-110">Píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="e2d07-110">The specified pixel.</span></span>

<span data-ttu-id="e2d07-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="e2d07-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="e2d07-112">Destino de representación especificado.</span><span class="sxs-lookup"><span data-stu-id="e2d07-112">The specified render target.</span></span>

<span data-ttu-id="e2d07-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e2d07-113">*requestCallback* </span></span>  
<span data-ttu-id="e2d07-114">Dirección de una devolución de llamada que se usa para notifify el host de los resultados.</span><span class="sxs-lookup"><span data-stu-id="e2d07-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="e2d07-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e2d07-115">*requestCookie* </span></span>  
<span data-ttu-id="e2d07-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="e2d07-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e2d07-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e2d07-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e2d07-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e2d07-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2d07-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2d07-119">Return value</span></span>

<span data-ttu-id="e2d07-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e2d07-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e2d07-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2d07-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d07-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d07-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e2d07-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2d07-123">Header</span></span></p></td><td><span data-ttu-id="e2d07-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e2d07-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e2d07-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d07-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e2d07-126">**IPixelHistoryRequest**</span><span class="sxs-lookup"><span data-stu-id="e2d07-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
