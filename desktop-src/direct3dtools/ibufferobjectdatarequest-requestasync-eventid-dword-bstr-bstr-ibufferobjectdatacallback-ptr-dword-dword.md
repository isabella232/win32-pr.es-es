---
description: Solicita obtener el contenido sin procesar de un objeto (búfer, textura, vista de destino de representación, etc.).
MS-HAID: vspixengine.IBufferObjectDataRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_BSTR\_IBufferObjectDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IBufferObjectDataRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 899954DC-6196-4F79-AFB4-5E692DAA03EC
api_name:
- IBufferObjectDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 97d35f656f373f2f0040d49a78a2c0d376bc4266
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152219"
---
# <a name="span-idvspixengineibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dwordspanibufferobjectdatarequestrequestasync-method"></a><span data-ttu-id="4a63e-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="4a63e-103"><span id="vspixengine.ibufferobjectdatarequest_requestasync_eventid_dword_bstr_bstr_ibufferobjectdatacallback_ptr_dword_dword"></span>IBufferObjectDataRequest::RequestAsync method</span></span>

<span data-ttu-id="4a63e-104">Solicita obtener el contenido sin procesar de un objeto (búfer, textura, vista de destino de representación, etc.).</span><span class="sxs-lookup"><span data-stu-id="4a63e-104">Requests to get the raw contents of an object (buffer, texture, render target view, etc.)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a63e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a63e-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   BSTR                        Format,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4a63e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a63e-106">Parameters</span></span>

<span data-ttu-id="4a63e-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="4a63e-107">*eventID* </span></span>  
<span data-ttu-id="4a63e-108">Evento especificado con el que se va a hacer coincidir el contenido del búfer (por ejemplo, un destino de representación podría cambiar con el tiempo).</span><span class="sxs-lookup"><span data-stu-id="4a63e-108">The specified event to match the buffer's content to (for example, a render target could change over time).</span></span>

<span data-ttu-id="4a63e-109">*RequestedDataUID* </span><span class="sxs-lookup"><span data-stu-id="4a63e-109">*RequestedDataUID* </span></span>  
<span data-ttu-id="4a63e-110">Dirección del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="4a63e-110">The address of the specified object.</span></span>

<span data-ttu-id="4a63e-111">*Filesystem* </span><span class="sxs-lookup"><span data-stu-id="4a63e-111">*File* </span></span>  
<span data-ttu-id="4a63e-112">Cadena COM que contiene la ruta de acceso del archivo donde se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="4a63e-112">A COM string that contains the pathname of the file where results are written.</span></span>

<span data-ttu-id="4a63e-113">*Aplique* </span><span class="sxs-lookup"><span data-stu-id="4a63e-113">*Format* </span></span>  
<span data-ttu-id="4a63e-114">No se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="4a63e-114">Not currently used.</span></span> <span data-ttu-id="4a63e-115">Cadena COM que especifica el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="4a63e-115">A COM string that specifies the output format.</span></span>

<span data-ttu-id="4a63e-116">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4a63e-116">*requestCallback* </span></span>  
<span data-ttu-id="4a63e-117">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="4a63e-117">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4a63e-118">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4a63e-118">*requestCookie* </span></span>  
<span data-ttu-id="4a63e-119">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="4a63e-119">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4a63e-120">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4a63e-120">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4a63e-121">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4a63e-121">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a63e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a63e-122">Return value</span></span>

<span data-ttu-id="4a63e-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4a63e-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a63e-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a63e-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a63e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a63e-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4a63e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a63e-126">Header</span></span></p></td><td><span data-ttu-id="4a63e-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4a63e-127">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4a63e-128"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="4a63e-128"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4a63e-129">**IBufferObjectDataRequest**</span><span class="sxs-lookup"><span data-stu-id="4a63e-129">**IBufferObjectDataRequest**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatarequest)

 

 
