---
description: El \_ método put StopTime establece el valor de hora de finalización del Protocolo de tiempo de red (NTP). Si la hora de finalización es cero, la sesión no está enlazada.
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime: método de ut_StopTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679373"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="07f1e-104">ITTime::p \_ método StopTime UT</span><span class="sxs-lookup"><span data-stu-id="07f1e-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="07f1e-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07f1e-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="07f1e-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="07f1e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="07f1e-107">El método **Put \_ StopTime** establece el valor de hora de finalización del Protocolo de tiempo de red (NTP).</span><span class="sxs-lookup"><span data-stu-id="07f1e-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="07f1e-108">Si la hora de finalización es cero, la sesión no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="07f1e-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f1e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07f1e-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="07f1e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07f1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f1e-111">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="07f1e-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07f1e-112">Hora de detención de la sesión.</span><span class="sxs-lookup"><span data-stu-id="07f1e-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f1e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07f1e-113">Return value</span></span>

<span data-ttu-id="07f1e-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="07f1e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="07f1e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="07f1e-115">Return code</span></span>                                                                                   | <span data-ttu-id="07f1e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="07f1e-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="07f1e-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="07f1e-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="07f1e-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="07f1e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="07f1e-120">El parámetro de *tiempo* no es válido.</span><span class="sxs-lookup"><span data-stu-id="07f1e-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="07f1e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="07f1e-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="07f1e-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="07f1e-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="07f1e-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="07f1e-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="07f1e-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="07f1e-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="07f1e-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="07f1e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07f1e-127">Remarks</span></span>

<span data-ttu-id="07f1e-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="07f1e-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="07f1e-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="07f1e-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f1e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07f1e-130">Requirements</span></span>



| <span data-ttu-id="07f1e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f1e-131">Requirement</span></span> | <span data-ttu-id="07f1e-132">Value</span><span class="sxs-lookup"><span data-stu-id="07f1e-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07f1e-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="07f1e-133">TAPI version</span></span><br/> | <span data-ttu-id="07f1e-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="07f1e-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="07f1e-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07f1e-135">Header</span></span><br/>       | <dl> <span data-ttu-id="07f1e-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="07f1e-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07f1e-137">Library</span></span><br/>      | <dl> <span data-ttu-id="07f1e-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="07f1e-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07f1e-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="07f1e-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07f1e-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f1e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f1e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f1e-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="07f1e-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="07f1e-143">**ITTime:: get \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="07f1e-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




