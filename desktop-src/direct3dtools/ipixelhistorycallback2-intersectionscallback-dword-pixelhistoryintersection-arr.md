---
description: Devolución de llamada que notifica al host la información de intersección del historial de píxeles devuelta por la solicitud asociada.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback2:: IntersectionsCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152277"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="098f0-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2:: IntersectionsCallback (método)</span><span class="sxs-lookup"><span data-stu-id="098f0-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="098f0-104">Devolución de llamada que notifica al host la información de intersección del historial de píxeles devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="098f0-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="098f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="098f0-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="098f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="098f0-106">Parameters</span></span>

<span data-ttu-id="098f0-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="098f0-107">*count* </span></span>  
<span data-ttu-id="098f0-108">Número de intersecciones del historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="098f0-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="098f0-109">*intersecciones de count0 \_* </span><span class="sxs-lookup"><span data-stu-id="098f0-109">*count0\_intersections* </span></span>  
<span data-ttu-id="098f0-110">Intersecciones del historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="098f0-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="098f0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="098f0-111">Return value</span></span>

<span data-ttu-id="098f0-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="098f0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="098f0-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="098f0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="098f0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="098f0-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="098f0-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="098f0-115">Header</span></span></p></td><td><span data-ttu-id="098f0-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="098f0-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="098f0-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="098f0-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="098f0-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="098f0-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
