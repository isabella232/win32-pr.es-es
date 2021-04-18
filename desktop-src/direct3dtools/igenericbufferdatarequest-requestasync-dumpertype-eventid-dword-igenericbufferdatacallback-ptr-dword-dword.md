---
description: Solicita que se devuelvan datos de objetos genéricos que describen un objeto en el archivo. vsglog para el evento especificado y en el formato especificado.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IGenericBufferDataRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714764"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span data-ttu-id="bb31b-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="bb31b-103"><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync method</span></span>

<span data-ttu-id="bb31b-104">Solicita que se devuelvan datos de objetos genéricos que describen un objeto en el archivo. vsglog para el evento especificado y en el formato especificado.</span><span class="sxs-lookup"><span data-stu-id="bb31b-104">Requests to return generic object data that describes an object in the .vsglog file for the specified event and in the specified format.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb31b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb31b-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="bb31b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb31b-106">Parameters</span></span>

<span data-ttu-id="bb31b-107">*dumperType* </span><span class="sxs-lookup"><span data-stu-id="bb31b-107">*dumperType* </span></span>  
<span data-ttu-id="bb31b-108">Formato especificado de la representación textual del objeto (HTML, XML, etc.).</span><span class="sxs-lookup"><span data-stu-id="bb31b-108">The specified format of the textual representation of the object (HTML, XML, etc.)</span></span>

<span data-ttu-id="bb31b-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="bb31b-109">*eventID* </span></span>  
<span data-ttu-id="bb31b-110">Evento especificado con el que se va a hacer coincidir el contenido del búfer (por ejemplo, un destino de representación podría cambiar con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="bb31b-110">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="bb31b-111">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="bb31b-111">*RequestedDataUID* </span></span>  
<span data-ttu-id="bb31b-112">Dirección del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="bb31b-112">The address of the specified object.</span></span>

<span data-ttu-id="bb31b-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="bb31b-113">*requestCallback* </span></span>  
<span data-ttu-id="bb31b-114">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="bb31b-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="bb31b-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="bb31b-115">*requestCookie* </span></span>  
<span data-ttu-id="bb31b-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="bb31b-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="bb31b-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="bb31b-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="bb31b-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bb31b-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb31b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb31b-119">Return value</span></span>

<span data-ttu-id="bb31b-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bb31b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb31b-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb31b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb31b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb31b-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bb31b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb31b-123">Header</span></span></p></td><td><span data-ttu-id="bb31b-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bb31b-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="bb31b-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="bb31b-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="bb31b-126">**IGenericBufferDataRequest**</span><span class="sxs-lookup"><span data-stu-id="bb31b-126">**IGenericBufferDataRequest**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
