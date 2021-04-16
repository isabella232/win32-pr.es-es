---
description: Una solicitud asincrónica para obtener una lista de las fases usadas para el marco y el evento especificados.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest:: RequestSupportedStagesAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677187"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="71393-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest:: RequestSupportedStagesAsync (método)</span><span class="sxs-lookup"><span data-stu-id="71393-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="71393-104">Una solicitud asincrónica para obtener una lista de las fases usadas para el marco y el evento especificados.</span><span class="sxs-lookup"><span data-stu-id="71393-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="71393-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71393-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="71393-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71393-106">Parameters</span></span>

<span data-ttu-id="71393-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="71393-107">*frameNumber* </span></span>  
<span data-ttu-id="71393-108">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="71393-108">The specified frame.</span></span>

<span data-ttu-id="71393-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="71393-109">*eventID* </span></span>  
<span data-ttu-id="71393-110">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="71393-110">The specified event.</span></span>

<span data-ttu-id="71393-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="71393-111">*requestCallback* </span></span>  
<span data-ttu-id="71393-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="71393-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="71393-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="71393-113">*requestCookie* </span></span>  
<span data-ttu-id="71393-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="71393-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="71393-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="71393-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="71393-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="71393-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="71393-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71393-117">Return value</span></span>

<span data-ttu-id="71393-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="71393-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71393-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71393-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="71393-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71393-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="71393-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71393-121">Header</span></span></p></td><td><span data-ttu-id="71393-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="71393-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="71393-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="71393-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="71393-124">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="71393-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
