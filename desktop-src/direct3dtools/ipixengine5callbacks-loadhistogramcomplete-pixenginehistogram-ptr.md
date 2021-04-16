---
description: Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga del histograma.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks:: LoadHistogramComplete (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0e468422f722a8bd549d63f34225833462856b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686376"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span data-ttu-id="609d8-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks:: LoadHistogramComplete (método)</span><span class="sxs-lookup"><span data-stu-id="609d8-103"><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadHistogramComplete method</span></span>

<span data-ttu-id="609d8-104">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga del histograma.</span><span class="sxs-lookup"><span data-stu-id="609d8-104">A callback function used to notify the host when a histogram load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="609d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="609d8-105">Syntax</span></span>


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="609d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="609d8-106">Parameters</span></span>

<span data-ttu-id="609d8-107">*cargas* </span><span class="sxs-lookup"><span data-stu-id="609d8-107">*histogram* </span></span>  
<span data-ttu-id="609d8-108">Dirección de los datos del histograma para el histograma cargado.</span><span class="sxs-lookup"><span data-stu-id="609d8-108">The address of histogram data for the loaded histogram.</span></span>

## <a name="return-value"></a><span data-ttu-id="609d8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="609d8-109">Return value</span></span>

<span data-ttu-id="609d8-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="609d8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="609d8-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="609d8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="609d8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="609d8-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="609d8-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="609d8-113">Header</span></span></p></td><td><span data-ttu-id="609d8-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="609d8-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="609d8-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="609d8-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="609d8-116">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="609d8-116">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
