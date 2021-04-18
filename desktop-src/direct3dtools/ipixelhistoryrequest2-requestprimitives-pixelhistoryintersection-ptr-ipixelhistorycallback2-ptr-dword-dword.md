---
description: Solicita una lista de primitivas de una intersección determinada. Para obtener más información, vea la función miembro RequestIntersections.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryRequest2:: RequestPrimitives (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714703"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="3f3e7-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2:: RequestPrimitives (método)</span><span class="sxs-lookup"><span data-stu-id="3f3e7-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="3f3e7-105">Solicita una lista de primitivas de una intersección determinada.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="3f3e7-106">Para obtener más información, vea la función miembro RequestIntersections.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f3e7-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3f3e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f3e7-108">Parameters</span></span>

<span data-ttu-id="3f3e7-109">*intersección* </span><span class="sxs-lookup"><span data-stu-id="3f3e7-109">*intersection* </span></span>  
<span data-ttu-id="3f3e7-110">Dirección de la intersección especificada.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-110">The address of the specified intersection.</span></span>

<span data-ttu-id="3f3e7-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="3f3e7-111">*requestCallback* </span></span>  
<span data-ttu-id="3f3e7-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="3f3e7-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="3f3e7-113">*requestCookie* </span></span>  
<span data-ttu-id="3f3e7-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3f3e7-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="3f3e7-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3f3e7-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f3e7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f3e7-117">Return value</span></span>

<span data-ttu-id="3f3e7-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3f3e7-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f3e7-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f3e7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3e7-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3f3e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f3e7-121">Header</span></span></p></td><td><span data-ttu-id="3f3e7-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3f3e7-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3f3e7-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="3f3e7-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3f3e7-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="3f3e7-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
