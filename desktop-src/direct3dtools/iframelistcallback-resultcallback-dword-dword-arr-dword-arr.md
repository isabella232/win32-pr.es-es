---
description: Función de devolución de llamada que se usa para notificar al host qué fotogramas se han capturado.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameListCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 00a991ec2d380d9c052f02ed69bb71d233fd0d93
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495749"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span data-ttu-id="69fc3-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="69fc3-103"><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>IFrameListCallback::ResultCallback method</span></span>

<span data-ttu-id="69fc3-104">Función de devolución de llamada que se usa para notificar al host qué fotogramas se han capturado.</span><span class="sxs-lookup"><span data-stu-id="69fc3-104">A callback function used to notify the host of which frames were captured.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fc3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69fc3-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a><span data-ttu-id="69fc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69fc3-106">Parameters</span></span>

<span data-ttu-id="69fc3-107">*numFrames* </span><span class="sxs-lookup"><span data-stu-id="69fc3-107">*numFrames* </span></span>  
<span data-ttu-id="69fc3-108">Número de fotogramas capturados.</span><span class="sxs-lookup"><span data-stu-id="69fc3-108">The number of frames captured.</span></span>

<span data-ttu-id="69fc3-109">*count0 \_ frameNumbers* </span><span class="sxs-lookup"><span data-stu-id="69fc3-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="69fc3-110">Números de fotogramas de los fotogramas capturados.</span><span class="sxs-lookup"><span data-stu-id="69fc3-110">The frame numbers of the captured frames.</span></span>

<span data-ttu-id="69fc3-111">*count0 \_ frameEventIDs* </span><span class="sxs-lookup"><span data-stu-id="69fc3-111">*count0\_frameEventIDs* </span></span>  
<span data-ttu-id="69fc3-112">Evento final asociado a cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="69fc3-112">The final event associated with each frame.</span></span>

## <a name="return-value"></a><span data-ttu-id="69fc3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69fc3-113">Return value</span></span>

<span data-ttu-id="69fc3-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="69fc3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69fc3-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69fc3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fc3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69fc3-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="69fc3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69fc3-117">Header</span></span></p></td><td><span data-ttu-id="69fc3-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="69fc3-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="69fc3-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="69fc3-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="69fc3-120">**IFrameListCallback**</span><span class="sxs-lookup"><span data-stu-id="69fc3-120">**IFrameListCallback**</span></span>](/windows/desktop/direct3dtools/iframelistcallback)

 

 
