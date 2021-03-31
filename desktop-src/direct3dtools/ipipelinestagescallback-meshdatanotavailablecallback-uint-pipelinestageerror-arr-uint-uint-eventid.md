---
description: Devolución de llamada que notifica al host las fases de canalización que no pueden devolver datos de malla para el evento especificado en la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback:: MeshDataNotAvailableCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 42391c342e2f11b39d1535b5286a92e161d0fd9b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495689"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span data-ttu-id="6503e-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback:: MeshDataNotAvailableCallback (método)</span><span class="sxs-lookup"><span data-stu-id="6503e-103"><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>IPipeLineStagesCallback::MeshDataNotAvailableCallback method</span></span>

<span data-ttu-id="6503e-104">Devolución de llamada que notifica al host las fases de canalización que no pueden devolver datos de malla para el evento especificado en la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="6503e-104">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6503e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6503e-105">Syntax</span></span>


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a><span data-ttu-id="6503e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6503e-106">Parameters</span></span>

<span data-ttu-id="6503e-107">*numberStages* </span><span class="sxs-lookup"><span data-stu-id="6503e-107">*numberStages* </span></span>  
<span data-ttu-id="6503e-108">El número de errores de fase devueltos.</span><span class="sxs-lookup"><span data-stu-id="6503e-108">The number of stage errors returned.</span></span>

<span data-ttu-id="6503e-109">*errores de count0 \_* </span><span class="sxs-lookup"><span data-stu-id="6503e-109">*count0\_errors* </span></span>  
<span data-ttu-id="6503e-110">Errores de la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="6503e-110">The pipeline stage errors.</span></span>

<span data-ttu-id="6503e-111">*Ancho* </span><span class="sxs-lookup"><span data-stu-id="6503e-111">*width* </span></span>  
<span data-ttu-id="6503e-112">El ancho de la cadena de intercambio asociada con la llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="6503e-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="6503e-113">Se usa cuando se solicitan imágenes de vista previa de canalización.</span><span class="sxs-lookup"><span data-stu-id="6503e-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="6503e-114">*alto* </span><span class="sxs-lookup"><span data-stu-id="6503e-114">*height* </span></span>  
<span data-ttu-id="6503e-115">El alto de la cadena de intercambio asociada con la llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="6503e-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="6503e-116">Se usa cuando se solicitan imágenes de vista previa de canalización.</span><span class="sxs-lookup"><span data-stu-id="6503e-116">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="6503e-117">*Eid* </span><span class="sxs-lookup"><span data-stu-id="6503e-117">*eid* </span></span>  
<span data-ttu-id="6503e-118">Evento representado en los resultados.</span><span class="sxs-lookup"><span data-stu-id="6503e-118">The event represented in the results.</span></span>

## <a name="return-value"></a><span data-ttu-id="6503e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6503e-119">Return value</span></span>

<span data-ttu-id="6503e-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6503e-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6503e-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6503e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6503e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6503e-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6503e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6503e-123">Header</span></span></p></td><td><span data-ttu-id="6503e-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6503e-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6503e-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="6503e-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6503e-126">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="6503e-126">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
