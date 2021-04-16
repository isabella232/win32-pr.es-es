---
description: El \_ método get startTime obtiene el valor de hora de inicio de NTP (Protocolo de tiempo de red) de 32 bits. La sesión se considera activa desde este momento.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'Método ITTime:: get_StartTime (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690245"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="8a002-104">ITTime:: get \_ startTime (método)</span><span class="sxs-lookup"><span data-stu-id="8a002-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="8a002-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8a002-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a002-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8a002-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a002-107">El método **Get \_ startTime** obtiene el valor de hora de inicio de NTP (Protocolo de tiempo de red) de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8a002-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="8a002-108">La sesión se considera activa desde este momento.</span><span class="sxs-lookup"><span data-stu-id="8a002-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a002-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a002-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="8a002-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a002-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a002-111">*pTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a002-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a002-112">Puntero a la hora de inicio de la sesión.</span><span class="sxs-lookup"><span data-stu-id="8a002-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a002-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a002-113">Return value</span></span>

<span data-ttu-id="8a002-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8a002-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8a002-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a002-115">Return code</span></span>                                                                                   | <span data-ttu-id="8a002-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a002-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8a002-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a002-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a002-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8a002-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a002-120">El parámetro *pTime* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8a002-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="8a002-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a002-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8a002-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8a002-123"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8a002-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8a002-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8a002-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8a002-126">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8a002-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8a002-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a002-127">Requirements</span></span>



| <span data-ttu-id="8a002-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a002-128">Requirement</span></span> | <span data-ttu-id="8a002-129">Value</span><span class="sxs-lookup"><span data-stu-id="8a002-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a002-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8a002-130">TAPI version</span></span><br/> | <span data-ttu-id="8a002-131">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8a002-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8a002-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a002-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8a002-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a002-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a002-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8a002-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8a002-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a002-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a002-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a002-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a002-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a002-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a002-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="8a002-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="8a002-140">**ITTime::p UT \_ hora_inicio**</span><span class="sxs-lookup"><span data-stu-id="8a002-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




