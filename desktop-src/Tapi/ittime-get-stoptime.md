---
description: El \_ método get StopTime obtiene el valor de hora de finalización del Protocolo de tiempo de red (NTP). Si la hora de finalización es cero, la sesión no está enlazada.
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'Método ITTime:: get_StopTime (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690244"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="cfaed-104">ITTime:: get \_ StopTime (método)</span><span class="sxs-lookup"><span data-stu-id="cfaed-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="cfaed-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfaed-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cfaed-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="cfaed-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cfaed-107">El método **Get \_ StopTime** obtiene el valor de hora de finalización del Protocolo de tiempo de red (NTP).</span><span class="sxs-lookup"><span data-stu-id="cfaed-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="cfaed-108">Si la hora de finalización es cero, la sesión no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="cfaed-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfaed-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfaed-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="cfaed-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfaed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfaed-111">*pTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfaed-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfaed-112">Puntero a la hora de detención de la sesión.</span><span class="sxs-lookup"><span data-stu-id="cfaed-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfaed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfaed-113">Return value</span></span>

<span data-ttu-id="cfaed-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="cfaed-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cfaed-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cfaed-115">Return code</span></span>                                                                                   | <span data-ttu-id="cfaed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfaed-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cfaed-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cfaed-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cfaed-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cfaed-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cfaed-120">El parámetro *pTime* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="cfaed-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="cfaed-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cfaed-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="cfaed-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cfaed-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cfaed-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="cfaed-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cfaed-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cfaed-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="cfaed-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="cfaed-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfaed-127">Requirements</span></span>



| <span data-ttu-id="cfaed-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfaed-128">Requirement</span></span> | <span data-ttu-id="cfaed-129">Value</span><span class="sxs-lookup"><span data-stu-id="cfaed-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfaed-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cfaed-130">TAPI version</span></span><br/> | <span data-ttu-id="cfaed-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cfaed-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cfaed-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfaed-132">Header</span></span><br/>       | <dl> <span data-ttu-id="cfaed-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfaed-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfaed-134">Library</span></span><br/>      | <dl> <span data-ttu-id="cfaed-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cfaed-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfaed-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="cfaed-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfaed-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfaed-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfaed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfaed-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="cfaed-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="cfaed-140">**ITTime::p UT \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="cfaed-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




