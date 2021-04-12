---
description: Una solicitud asincrónica para iniciar una acción (por ejemplo, capturar un fotograma) en el motor.
MS-HAID: vspixengine.IRunActionRequest\_RequestAsync\_REFGUID\_IUnknown\_ptr\_IRunActionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IRunActionRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4A4DF4BE-383D-4B36-9195-61720C3B4D97
api_name:
- IRunActionRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 179abf44231d122ca82527fc5739b876395c327b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152616"
---
# <a name="span-idvspixengineirunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dwordspanirunactionrequestrequestasync-method"></a><span data-ttu-id="76ea9-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="76ea9-103"><span id="vspixengine.irunactionrequest_requestasync_refguid_iunknown_ptr_irunactioncallback_ptr_dword_dword"></span>IRunActionRequest::RequestAsync method</span></span>

<span data-ttu-id="76ea9-104">Una solicitud asincrónica para iniciar una acción (por ejemplo, capturar un fotograma) en el motor.</span><span class="sxs-lookup"><span data-stu-id="76ea9-104">An asynchronous request to initiate an action (for example, capture a frame) in the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ea9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76ea9-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   REFGUID              action,
   IUnknown *           actionPayload,
   IRunActionCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="76ea9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76ea9-106">Parameters</span></span>

<span data-ttu-id="76ea9-107">*actuar* </span><span class="sxs-lookup"><span data-stu-id="76ea9-107">*action* </span></span>  
<span data-ttu-id="76ea9-108">La acción especificada.</span><span class="sxs-lookup"><span data-stu-id="76ea9-108">The specified action.</span></span>

<span data-ttu-id="76ea9-109">*actionPayload* </span><span class="sxs-lookup"><span data-stu-id="76ea9-109">*actionPayload* </span></span>  
<span data-ttu-id="76ea9-110">La carga de la acción especificada.</span><span class="sxs-lookup"><span data-stu-id="76ea9-110">The payload of the specified action.</span></span>

<span data-ttu-id="76ea9-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="76ea9-111">*requestCallback* </span></span>  
<span data-ttu-id="76ea9-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="76ea9-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="76ea9-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="76ea9-113">*requestCookie* </span></span>  
<span data-ttu-id="76ea9-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="76ea9-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="76ea9-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="76ea9-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="76ea9-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="76ea9-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="76ea9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76ea9-117">Return value</span></span>

<span data-ttu-id="76ea9-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="76ea9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76ea9-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76ea9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ea9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ea9-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="76ea9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76ea9-121">Header</span></span></p></td><td><span data-ttu-id="76ea9-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="76ea9-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="76ea9-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="76ea9-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="76ea9-124">**IRunActionRequest**</span><span class="sxs-lookup"><span data-stu-id="76ea9-124">**IRunActionRequest**</span></span>](/windows/desktop/direct3dtools/irunactionrequest)

 

 
