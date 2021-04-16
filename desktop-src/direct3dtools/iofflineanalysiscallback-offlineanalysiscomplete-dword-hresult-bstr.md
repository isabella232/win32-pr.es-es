---
description: Función de devolución de llamada que se usa para notificar al host que se ha completado el análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCallback:: OfflineAnalysisComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538205"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="c9dca-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback:: OfflineAnalysisComplete (método)</span><span class="sxs-lookup"><span data-stu-id="c9dca-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="c9dca-104">Función de devolución de llamada que se usa para notificar al host que se ha completado el análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c9dca-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9dca-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="c9dca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9dca-106">Parameters</span></span>

<span data-ttu-id="c9dca-107">*ellas* </span><span class="sxs-lookup"><span data-stu-id="c9dca-107">*cookie* </span></span>  
<span data-ttu-id="c9dca-108">Cookie que identifica de forma única la solicitud que inició el análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c9dca-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="c9dca-109">*da* </span><span class="sxs-lookup"><span data-stu-id="c9dca-109">*result* </span></span>  
<span data-ttu-id="c9dca-110">Indica si el análisis sin conexión se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c9dca-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="c9dca-111">Si se realiza correctamente, los resultados se escribieron en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c9dca-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="c9dca-112">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="c9dca-112">*outputFullFileName* </span></span>  
<span data-ttu-id="c9dca-113">Una cadena COM contianing el nombre del archivo donde se escribieron los resultados del análisis sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c9dca-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9dca-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9dca-114">Return value</span></span>

<span data-ttu-id="c9dca-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c9dca-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9dca-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9dca-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9dca-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9dca-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c9dca-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9dca-118">Header</span></span></p></td><td><span data-ttu-id="c9dca-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c9dca-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c9dca-120"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c9dca-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c9dca-121">**IOfflineAnalysisCallback**</span><span class="sxs-lookup"><span data-stu-id="c9dca-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
