---
description: Función de devolución de llamada que se usa para notificar al host el progreso del análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCallback:: OfflineAnalysisProgress (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423128"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="619ab-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback:: OfflineAnalysisProgress (método)</span><span class="sxs-lookup"><span data-stu-id="619ab-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="619ab-104">Función de devolución de llamada que se usa para notificar al host el progreso del análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="619ab-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="619ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="619ab-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="619ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="619ab-106">Parameters</span></span>

<span data-ttu-id="619ab-107">*ellas* </span><span class="sxs-lookup"><span data-stu-id="619ab-107">*cookie* </span></span>  
<span data-ttu-id="619ab-108">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="619ab-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="619ab-109">*progreso* </span><span class="sxs-lookup"><span data-stu-id="619ab-109">*progress* </span></span>  
<span data-ttu-id="619ab-110">Porcentaje de progreso.</span><span class="sxs-lookup"><span data-stu-id="619ab-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="619ab-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="619ab-111">Return value</span></span>

<span data-ttu-id="619ab-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="619ab-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="619ab-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="619ab-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="619ab-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="619ab-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="619ab-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="619ab-115">Header</span></span></p></td><td><span data-ttu-id="619ab-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="619ab-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="619ab-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="619ab-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="619ab-118">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="619ab-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
