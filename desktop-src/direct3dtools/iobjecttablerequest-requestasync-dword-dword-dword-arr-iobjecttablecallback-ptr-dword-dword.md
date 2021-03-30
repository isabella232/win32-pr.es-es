---
description: Solicita que se obtenga la información especificada de la tabla de objetos para el evento especificado.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806194"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="60f7c-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="60f7c-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="60f7c-104">Solicita que se obtenga la información especificada de la tabla de objetos para el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="60f7c-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60f7c-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="60f7c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60f7c-106">Parameters</span></span>

<span data-ttu-id="60f7c-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="60f7c-107">*eventID* </span></span>  
<span data-ttu-id="60f7c-108">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="60f7c-108">The specified event.</span></span>

<span data-ttu-id="60f7c-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="60f7c-109">*numColumns* </span></span>  
<span data-ttu-id="60f7c-110">El número de columnas (campos) de información que se van a obtener.</span><span class="sxs-lookup"><span data-stu-id="60f7c-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="60f7c-111">*\_columnas count1* </span><span class="sxs-lookup"><span data-stu-id="60f7c-111">*count1\_columns* </span></span>  
<span data-ttu-id="60f7c-112">Columnas especificadas (campos).</span><span class="sxs-lookup"><span data-stu-id="60f7c-112">The specified columns (fields).</span></span>

<span data-ttu-id="60f7c-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="60f7c-113">*requestCallback* </span></span>  
<span data-ttu-id="60f7c-114">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="60f7c-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="60f7c-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="60f7c-115">*requestCookie* </span></span>  
<span data-ttu-id="60f7c-116">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="60f7c-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="60f7c-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="60f7c-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="60f7c-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="60f7c-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="60f7c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60f7c-119">Return value</span></span>

<span data-ttu-id="60f7c-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="60f7c-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60f7c-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60f7c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f7c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60f7c-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="60f7c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60f7c-123">Header</span></span></p></td><td><span data-ttu-id="60f7c-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="60f7c-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="60f7c-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="60f7c-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="60f7c-126">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="60f7c-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
