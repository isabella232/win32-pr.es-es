---
description: Solicita una lista de eventos que provocan un cambio en el píxel especificado, el destino de representación/UAV y el marco.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: RequestIntersections (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537318"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="ed840-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: RequestIntersections (método)</span><span class="sxs-lookup"><span data-stu-id="ed840-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="ed840-104">Solicita una lista de eventos que provocan un cambio en el píxel especificado, el destino de representación/UAV y el marco.</span><span class="sxs-lookup"><span data-stu-id="ed840-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed840-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed840-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ed840-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed840-106">Parameters</span></span>

<span data-ttu-id="ed840-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="ed840-107">*frameNumber* </span></span>  
<span data-ttu-id="ed840-108">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="ed840-108">The specified frame.</span></span>

<span data-ttu-id="ed840-109">*píxel* </span><span class="sxs-lookup"><span data-stu-id="ed840-109">*pixel* </span></span>  
<span data-ttu-id="ed840-110">Píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="ed840-110">The specified pixel.</span></span>

<span data-ttu-id="ed840-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="ed840-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="ed840-112">Dirección del destino de representación especificado</span><span class="sxs-lookup"><span data-stu-id="ed840-112">The address of the specified render target</span></span>

<span data-ttu-id="ed840-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ed840-113">*requestCallback* </span></span>  
<span data-ttu-id="ed840-114">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="ed840-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ed840-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ed840-115">*requestCookie* </span></span>  
<span data-ttu-id="ed840-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="ed840-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ed840-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ed840-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ed840-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ed840-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed840-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed840-119">Return value</span></span>

<span data-ttu-id="ed840-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ed840-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed840-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed840-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed840-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed840-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ed840-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed840-123">Header</span></span></p></td><td><span data-ttu-id="ed840-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ed840-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ed840-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="ed840-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ed840-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="ed840-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
