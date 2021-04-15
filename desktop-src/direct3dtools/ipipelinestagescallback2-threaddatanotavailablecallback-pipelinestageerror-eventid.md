---
description: Devolución de llamada que notifica al host que ThreadData no está disponible para una fase de canalización y un evento determinados.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2:: ThreadDataNotAvailableCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677188"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span data-ttu-id="6651d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2:: ThreadDataNotAvailableCallback (método)</span><span class="sxs-lookup"><span data-stu-id="6651d-103"><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>IPipeLineStagesCallback2::ThreadDataNotAvailableCallback method</span></span>

<span data-ttu-id="6651d-104">Devolución de llamada que notifica al host que ThreadData no está disponible para una fase de canalización y un evento determinados.</span><span class="sxs-lookup"><span data-stu-id="6651d-104">A callback that notifies the host that ThreadData is unavailable for a particular pipeline stage and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="6651d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6651d-105">Syntax</span></span>


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a><span data-ttu-id="6651d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6651d-106">Parameters</span></span>

<span data-ttu-id="6651d-107">*error* </span><span class="sxs-lookup"><span data-stu-id="6651d-107">*error* </span></span>  
<span data-ttu-id="6651d-108">Error en la fase de la canalización.</span><span class="sxs-lookup"><span data-stu-id="6651d-108">The pipeline stage error.</span></span>

<span data-ttu-id="6651d-109">*Eid* </span><span class="sxs-lookup"><span data-stu-id="6651d-109">*eid* </span></span>  
<span data-ttu-id="6651d-110">Evento representado en los resultados.</span><span class="sxs-lookup"><span data-stu-id="6651d-110">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="6651d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6651d-111">Return value</span></span>

<span data-ttu-id="6651d-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6651d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6651d-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6651d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6651d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6651d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6651d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6651d-115">Header</span></span></p></td><td><span data-ttu-id="6651d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6651d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6651d-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="6651d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6651d-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="6651d-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
