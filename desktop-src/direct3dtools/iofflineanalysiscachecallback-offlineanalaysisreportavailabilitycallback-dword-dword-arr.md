---
description: Función de devolución de llamada que se usa para notificar al host qué Marcos tienen informes de análisis sin conexión disponibles.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696090"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="806d1-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback:: OfflineAnalaysisReportAvailabilityCallback (método)</span><span class="sxs-lookup"><span data-stu-id="806d1-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="806d1-104">Función de devolución de llamada que se usa para notificar al host qué Marcos tienen informes de análisis sin conexión disponibles.</span><span class="sxs-lookup"><span data-stu-id="806d1-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="806d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="806d1-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="806d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="806d1-106">Parameters</span></span>

<span data-ttu-id="806d1-107">*numFramesWithReports* </span><span class="sxs-lookup"><span data-stu-id="806d1-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="806d1-108">Número de fotogramas de count0 \_ framesWithReports.</span><span class="sxs-lookup"><span data-stu-id="806d1-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="806d1-109">*count0 \_ framesWithReports* </span><span class="sxs-lookup"><span data-stu-id="806d1-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="806d1-110">Una matriz que contiene los números de marco de los marcos que tienen informes de análisis sin conexión disponibles.</span><span class="sxs-lookup"><span data-stu-id="806d1-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="806d1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="806d1-111">Return value</span></span>

<span data-ttu-id="806d1-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="806d1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="806d1-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="806d1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="806d1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806d1-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="806d1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="806d1-115">Header</span></span></p></td><td><span data-ttu-id="806d1-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="806d1-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="806d1-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="806d1-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="806d1-118">**IOfflineAnalysisCacheCallback**</span><span class="sxs-lookup"><span data-stu-id="806d1-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
