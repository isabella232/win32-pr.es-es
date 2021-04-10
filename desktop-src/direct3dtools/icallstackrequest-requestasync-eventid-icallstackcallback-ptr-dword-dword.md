---
description: Una solicitud asincrónica para obtener las RVA de la pila de llamadas (direcciones virtuales relativas) del evento especificado.
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ICallStackRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274729"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="ccfde-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="ccfde-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="ccfde-104">Una solicitud asincrónica para obtener las RVA de la pila de llamadas (direcciones virtuales relativas) del evento especificado.</span><span class="sxs-lookup"><span data-stu-id="ccfde-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccfde-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ccfde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccfde-106">Parameters</span></span>

<span data-ttu-id="ccfde-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="ccfde-107">*eventID* </span></span>  
<span data-ttu-id="ccfde-108">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="ccfde-108">The specified event.</span></span>

<span data-ttu-id="ccfde-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="ccfde-109">*requestCallback* </span></span>  
<span data-ttu-id="ccfde-110">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="ccfde-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="ccfde-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ccfde-111">*requestCookie* </span></span>  
<span data-ttu-id="ccfde-112">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="ccfde-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ccfde-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ccfde-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ccfde-114">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ccfde-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ccfde-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccfde-115">Return value</span></span>

<span data-ttu-id="ccfde-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ccfde-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccfde-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccfde-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccfde-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccfde-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ccfde-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccfde-119">Header</span></span></p></td><td><span data-ttu-id="ccfde-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ccfde-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ccfde-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="ccfde-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ccfde-122">**ICallStackRequest**</span><span class="sxs-lookup"><span data-stu-id="ccfde-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
