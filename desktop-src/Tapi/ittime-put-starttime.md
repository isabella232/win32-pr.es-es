---
description: El \_ método startTime Put establece el valor de hora de inicio de 32 bits NTP (Protocolo de tiempo de red). La sesión se considera activa desde este momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'ITTime: método de ut_StartTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679374"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="c69b6-104">ITTime::p \_ método startTime de UT</span><span class="sxs-lookup"><span data-stu-id="c69b6-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="c69b6-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c69b6-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c69b6-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="c69b6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c69b6-107">El **método \_ startTime Put** establece el valor de hora de inicio de 32 bits NTP (Protocolo de tiempo de red).</span><span class="sxs-lookup"><span data-stu-id="c69b6-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="c69b6-108">La sesión se considera activa desde este momento.</span><span class="sxs-lookup"><span data-stu-id="c69b6-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69b6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c69b6-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="c69b6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c69b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c69b6-111">*Hora* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c69b6-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c69b6-112">Hora de inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="c69b6-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c69b6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c69b6-113">Return value</span></span>

<span data-ttu-id="c69b6-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c69b6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c69b6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c69b6-115">Return code</span></span>                                                                                   | <span data-ttu-id="c69b6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c69b6-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c69b6-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c69b6-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c69b6-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c69b6-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c69b6-120">El parámetro *Tim* e no es válido.</span><span class="sxs-lookup"><span data-stu-id="c69b6-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="c69b6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c69b6-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c69b6-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c69b6-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c69b6-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c69b6-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c69b6-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c69b6-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="c69b6-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c69b6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c69b6-127">Remarks</span></span>

<span data-ttu-id="c69b6-128">Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos.</span><span class="sxs-lookup"><span data-stu-id="c69b6-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="c69b6-129">El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="c69b6-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c69b6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c69b6-130">Requirements</span></span>



| <span data-ttu-id="c69b6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69b6-131">Requirement</span></span> | <span data-ttu-id="c69b6-132">Value</span><span class="sxs-lookup"><span data-stu-id="c69b6-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c69b6-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c69b6-133">TAPI version</span></span><br/> | <span data-ttu-id="c69b6-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c69b6-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c69b6-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c69b6-135">Header</span></span><br/>       | <dl> <span data-ttu-id="c69b6-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c69b6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c69b6-137">Library</span></span><br/>      | <dl> <span data-ttu-id="c69b6-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c69b6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c69b6-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="c69b6-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c69b6-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69b6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c69b6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69b6-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="c69b6-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="c69b6-143">**ITTime:: get \_ startTime**</span><span class="sxs-lookup"><span data-stu-id="c69b6-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




