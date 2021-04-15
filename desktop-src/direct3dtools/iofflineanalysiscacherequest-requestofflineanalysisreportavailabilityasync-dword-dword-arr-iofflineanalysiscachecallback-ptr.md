---
description: Solicitudes para almacenar en caché el informe de análisis sin conexión de los marcos especificados.
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCacheRequest:: RequestOfflineAnalysisReportAvailabilityAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538211"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="af6ed-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest:: RequestOfflineAnalysisReportAvailabilityAsync (método)</span><span class="sxs-lookup"><span data-stu-id="af6ed-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="af6ed-104">Solicitudes para almacenar en caché el informe de análisis sin conexión de los marcos especificados.</span><span class="sxs-lookup"><span data-stu-id="af6ed-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af6ed-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="af6ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af6ed-106">Parameters</span></span>

<span data-ttu-id="af6ed-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="af6ed-107">*numFrames* </span></span>  
<span data-ttu-id="af6ed-108">Número de fotogramas para los que se van a generar informes de análisis.</span><span class="sxs-lookup"><span data-stu-id="af6ed-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="af6ed-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="af6ed-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="af6ed-110">Marcos especificados.</span><span class="sxs-lookup"><span data-stu-id="af6ed-110">The specified frames.</span></span>

<span data-ttu-id="af6ed-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="af6ed-111">*requestCallback* </span></span>  
<span data-ttu-id="af6ed-112">La dirección de una devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="af6ed-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="af6ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af6ed-113">Return value</span></span>

<span data-ttu-id="af6ed-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="af6ed-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af6ed-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af6ed-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6ed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af6ed-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="af6ed-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af6ed-117">Header</span></span></p></td><td><span data-ttu-id="af6ed-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="af6ed-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="af6ed-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="af6ed-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="af6ed-120">**IOfflineAnalysisCacheRequest**</span><span class="sxs-lookup"><span data-stu-id="af6ed-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
