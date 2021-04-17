---
description: Una solicitud asincrónica para obtener datos del sombreador de cálculo para el envío especificado.
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderDataAsync\_EventID\_IPipeLineStagesCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest2:: RequestComputeShaderDataAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F73EA7B4-9E20-4BFD-8F87-20CE0B6C96D8
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderDataAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cf0d4725d8d2172900a96e58b4c8786ca2a9c851
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714753"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderdataasync-method"></a><span data-ttu-id="db95d-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2:: RequestComputeShaderDataAsync (método)</span><span class="sxs-lookup"><span data-stu-id="db95d-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderdataasync_eventid_ipipelinestagescallback2_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderDataAsync method</span></span>

<span data-ttu-id="db95d-104">Una solicitud asincrónica para obtener datos del sombreador de cálculo para el envío especificado.</span><span class="sxs-lookup"><span data-stu-id="db95d-104">An asynchronous request to get compute shader data for the specified dispatch.</span></span>

## <a name="syntax"></a><span data-ttu-id="db95d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db95d-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderDataAsync(
   EventID                    eventID,
   IPipeLineStagesCallback2 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="db95d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db95d-106">Parameters</span></span>

<span data-ttu-id="db95d-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="db95d-107">*eventID* </span></span>  
<span data-ttu-id="db95d-108">Evento de envío especificado.</span><span class="sxs-lookup"><span data-stu-id="db95d-108">The specified dispatch event.</span></span>

<span data-ttu-id="db95d-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="db95d-109">*requestCallback* </span></span>  
<span data-ttu-id="db95d-110">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="db95d-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="db95d-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="db95d-111">*requestCookie* </span></span>  
<span data-ttu-id="db95d-112">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="db95d-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="db95d-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="db95d-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="db95d-114">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="db95d-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="db95d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db95d-115">Return value</span></span>

<span data-ttu-id="db95d-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="db95d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db95d-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db95d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db95d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db95d-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="db95d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db95d-119">Header</span></span></p></td><td><span data-ttu-id="db95d-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="db95d-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="db95d-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="db95d-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="db95d-122">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="db95d-122">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
