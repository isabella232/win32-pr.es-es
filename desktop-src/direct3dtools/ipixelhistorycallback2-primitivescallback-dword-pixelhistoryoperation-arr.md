---
description: Devolución de llamada que notifica al host la información de la operación primitiva del historial de píxeles devuelta por la solicitud asociada.
MS-HAID: vspixengine.IPixelHistoryCallback2\_PrimitivesCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryCallback2::P método rimitivesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2A67EC3B-72F2-4347-AD23-961CDE0D456F
api_name:
- IPixelHistoryCallback2.PrimitivesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8512bde1acd96ebbe132eeb91872d04ce043b44f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537923"
---
# <a name="span-idvspixengineipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arrspanipixelhistorycallback2primitivescallback-method"></a><span data-ttu-id="17dbb-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::P método rimitivesCallback</span><span class="sxs-lookup"><span data-stu-id="17dbb-103"><span id="vspixengine.ipixelhistorycallback2_primitivescallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback2::PrimitivesCallback method</span></span>

<span data-ttu-id="17dbb-104">Devolución de llamada que notifica al host la información de la operación primitiva del historial de píxeles devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="17dbb-104">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="17dbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17dbb-105">Syntax</span></span>


```C++
HRESULT PrimitivesCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_primitives
);
```

## <a name="parameters"></a><span data-ttu-id="17dbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17dbb-106">Parameters</span></span>

<span data-ttu-id="17dbb-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="17dbb-107">*count* </span></span>  
<span data-ttu-id="17dbb-108">Número de primitivas.</span><span class="sxs-lookup"><span data-stu-id="17dbb-108">The number of primitives.</span></span>

<span data-ttu-id="17dbb-109">*\_primitivas count0* </span><span class="sxs-lookup"><span data-stu-id="17dbb-109">*count0\_primitives* </span></span>  
<span data-ttu-id="17dbb-110">Primitivas.</span><span class="sxs-lookup"><span data-stu-id="17dbb-110">The primitives.</span></span>

## <a name="return-value"></a><span data-ttu-id="17dbb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dbb-111">Return value</span></span>

<span data-ttu-id="17dbb-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="17dbb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17dbb-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17dbb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="17dbb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dbb-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="17dbb-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17dbb-115">Header</span></span></p></td><td><span data-ttu-id="17dbb-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="17dbb-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="17dbb-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="17dbb-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="17dbb-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="17dbb-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
