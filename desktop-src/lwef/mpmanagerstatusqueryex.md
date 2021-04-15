---
title: Función MpManagerStatusQueryEx (MpClient. h)
description: Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de. | Función MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Función MpManagerStatusQueryEx características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689856"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="4a781-105">MpManagerStatusQueryEx función)</span><span class="sxs-lookup"><span data-stu-id="4a781-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="4a781-106">Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="4a781-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a781-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a781-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4a781-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a781-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a781-109">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a781-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a781-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="4a781-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="4a781-111">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="4a781-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="4a781-112">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="4a781-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4a781-113">*dwFlag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a781-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a781-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a781-114">Type: **DWORD**</span></span>

<span data-ttu-id="4a781-115">Controla qué información de consulta se devuelve.</span><span class="sxs-lookup"><span data-stu-id="4a781-115">Controls which query information is returned.</span></span> <span data-ttu-id="4a781-116">Algunos datos son caros y es posible que no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="4a781-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="4a781-117">Value</span><span class="sxs-lookup"><span data-stu-id="4a781-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="4a781-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4a781-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="4a781-119"><dt>**marcas de consulta de estado de MP \_ \_ \_ \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="4a781-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="4a781-120">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4a781-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="4a781-121"><dt>**marca de consulta de estado de MP \_ \_ \_ \_ nostate**</dt></span><span class="sxs-lookup"><span data-stu-id="4a781-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="4a781-122">No consulte la información de estado.</span><span class="sxs-lookup"><span data-stu-id="4a781-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a781-123">*pStatusInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4a781-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a781-124">Tipo: **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="4a781-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="4a781-125">Puntero a una estructura que devuelve información de estado relativa a los últimos análisis, amenazas activas y distintos Estados de los componentes.</span><span class="sxs-lookup"><span data-stu-id="4a781-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="4a781-126">Vea [**\_ información de MPSTATUS**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="4a781-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a781-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a781-127">Return value</span></span>

<span data-ttu-id="4a781-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a781-128">Type: **HRESULT**</span></span>

<span data-ttu-id="4a781-129">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a781-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="4a781-130">Se garantiza que esta llamada de función se realiza correctamente aunque no se esté ejecutando un servicio antimalware.</span><span class="sxs-lookup"><span data-stu-id="4a781-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="4a781-131">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="4a781-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="4a781-132">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="4a781-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a781-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a781-133">Requirements</span></span>



| <span data-ttu-id="4a781-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a781-134">Requirement</span></span> | <span data-ttu-id="4a781-135">Value</span><span class="sxs-lookup"><span data-stu-id="4a781-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a781-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a781-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4a781-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a781-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4a781-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a781-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4a781-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a781-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a781-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a781-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a781-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a781-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a781-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a781-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a781-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a781-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a781-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a781-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a781-145">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="4a781-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="4a781-146">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="4a781-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="4a781-147">**información de MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="4a781-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





