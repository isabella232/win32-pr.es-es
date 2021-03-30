---
description: Una solicitud asincrónica para obtener información sobre las columnas (campos) que admite este tipo de solicitud de eventos de marco.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsRequest:: RequestSupportedColumnsAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806199"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="425ba-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest:: RequestSupportedColumnsAsync (método)</span><span class="sxs-lookup"><span data-stu-id="425ba-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="425ba-104">Una solicitud asincrónica para obtener información sobre las columnas (campos) que admite este tipo de solicitud de eventos de marco.</span><span class="sxs-lookup"><span data-stu-id="425ba-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="425ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="425ba-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="425ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="425ba-106">Parameters</span></span>

<span data-ttu-id="425ba-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="425ba-107">*requestCallback* </span></span>  
<span data-ttu-id="425ba-108">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="425ba-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="425ba-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="425ba-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="425ba-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="425ba-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="425ba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="425ba-111">Return value</span></span>

<span data-ttu-id="425ba-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="425ba-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="425ba-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="425ba-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="425ba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="425ba-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="425ba-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="425ba-115">Header</span></span></p></td><td><span data-ttu-id="425ba-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="425ba-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="425ba-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="425ba-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="425ba-118">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="425ba-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
