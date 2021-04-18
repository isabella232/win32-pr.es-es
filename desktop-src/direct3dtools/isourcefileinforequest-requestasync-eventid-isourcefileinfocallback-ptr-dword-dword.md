---
description: Una solicitud asincrónica para obtener los archivos de origen asociados a la pila de llamadas de un evento.
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISourceFileInfoRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714755"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="cd665-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="cd665-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="cd665-104">Una solicitud asincrónica para obtener los archivos de origen asociados a la pila de llamadas de un evento.</span><span class="sxs-lookup"><span data-stu-id="cd665-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd665-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd665-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="cd665-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd665-106">Parameters</span></span>

<span data-ttu-id="cd665-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="cd665-107">*eventID* </span></span>  
<span data-ttu-id="cd665-108">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="cd665-108">The specified event.</span></span>

<span data-ttu-id="cd665-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="cd665-109">*requestCallback* </span></span>  
<span data-ttu-id="cd665-110">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="cd665-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="cd665-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="cd665-111">*requestCookie* </span></span>  
<span data-ttu-id="cd665-112">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="cd665-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="cd665-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="cd665-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="cd665-114">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cd665-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd665-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd665-115">Return value</span></span>

<span data-ttu-id="cd665-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cd665-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd665-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd665-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd665-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd665-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cd665-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd665-119">Header</span></span></p></td><td><span data-ttu-id="cd665-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cd665-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cd665-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="cd665-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cd665-122">**ISourceFileInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="cd665-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
