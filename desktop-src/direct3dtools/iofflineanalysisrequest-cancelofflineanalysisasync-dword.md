---
description: Solicitudes para cancelar el análisis sin conexión en una solicitud de análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494878"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="b9039-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest:: CancelOfflineAnalysisAsync (método)</span><span class="sxs-lookup"><span data-stu-id="b9039-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="b9039-104">Solicitudes para cancelar el análisis sin conexión en una solicitud de análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b9039-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9039-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9039-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="b9039-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9039-106">Parameters</span></span>

<span data-ttu-id="b9039-107">*ellas* </span><span class="sxs-lookup"><span data-stu-id="b9039-107">*cookie* </span></span>  
<span data-ttu-id="b9039-108">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="b9039-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9039-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9039-109">Return value</span></span>

<span data-ttu-id="b9039-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b9039-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9039-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9039-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9039-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9039-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b9039-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9039-113">Header</span></span></p></td><td><span data-ttu-id="b9039-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b9039-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b9039-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="b9039-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b9039-116">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="b9039-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
