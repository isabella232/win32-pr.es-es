---
description: Devolución de llamada que notifica al host los resultados de la solicitud de historial de píxeles.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c43947148e2eb8139f3ad46157f19b1621a6c91e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359994"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span data-ttu-id="68eb3-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="68eb3-103"><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback::ResultCallback method</span></span>

<span data-ttu-id="68eb3-104">Devolución de llamada que notifica al host los resultados de la solicitud de historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="68eb3-104">A callback that notifies the host of pixel history request results.</span></span>

## <a name="syntax"></a><span data-ttu-id="68eb3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68eb3-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a><span data-ttu-id="68eb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68eb3-106">Parameters</span></span>

<span data-ttu-id="68eb3-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="68eb3-107">*count* </span></span>  
<span data-ttu-id="68eb3-108">Número de resultados.</span><span class="sxs-lookup"><span data-stu-id="68eb3-108">The number of results.</span></span>

<span data-ttu-id="68eb3-109">*count0 \_ pixelHistoryOperation* </span><span class="sxs-lookup"><span data-stu-id="68eb3-109">*count0\_pixelHistoryOperation* </span></span>  
<span data-ttu-id="68eb3-110">Resultados.</span><span class="sxs-lookup"><span data-stu-id="68eb3-110">The results.</span></span>

## <a name="return-value"></a><span data-ttu-id="68eb3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68eb3-111">Return value</span></span>

<span data-ttu-id="68eb3-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="68eb3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68eb3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68eb3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68eb3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68eb3-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="68eb3-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68eb3-115">Header</span></span></p></td><td><span data-ttu-id="68eb3-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="68eb3-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="68eb3-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="68eb3-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="68eb3-118">**IPixelHistoryCallback**</span><span class="sxs-lookup"><span data-stu-id="68eb3-118">**IPixelHistoryCallback**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
