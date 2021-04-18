---
title: Función MpManagerStatusQuery (MpClient. h)
description: Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de. | Función MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Función MpManagerStatusQuery características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362049"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="addbe-105">MpManagerStatusQuery función)</span><span class="sxs-lookup"><span data-stu-id="addbe-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="addbe-106">\[**MpManagerStatusQuery** no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="addbe-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="addbe-107">En su lugar, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="addbe-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="addbe-108">Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="addbe-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="addbe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="addbe-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="addbe-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="addbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="addbe-111">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="addbe-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="addbe-112">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="addbe-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="addbe-113">Identificador de la interfaz del administrador de protección contra malware.</span><span class="sxs-lookup"><span data-stu-id="addbe-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="addbe-114">La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="addbe-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="addbe-115">*pStatusInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="addbe-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="addbe-116">Tipo: **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="addbe-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="addbe-117">Puntero a una estructura que devuelve información de estado relativa a los últimos análisis, amenazas activas y distintos Estados de los componentes.</span><span class="sxs-lookup"><span data-stu-id="addbe-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="addbe-118">Vea [**\_ información de MPSTATUS**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="addbe-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="addbe-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="addbe-119">Return value</span></span>

<span data-ttu-id="addbe-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="addbe-120">Type: **HRESULT**</span></span>

<span data-ttu-id="addbe-121">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="addbe-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="addbe-122">Se garantiza que esta llamada de función se realiza correctamente aunque no se esté ejecutando un servicio antimalware.</span><span class="sxs-lookup"><span data-stu-id="addbe-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="addbe-123">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="addbe-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="addbe-124">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="addbe-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="addbe-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="addbe-125">Requirements</span></span>



| <span data-ttu-id="addbe-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="addbe-126">Requirement</span></span> | <span data-ttu-id="addbe-127">Value</span><span class="sxs-lookup"><span data-stu-id="addbe-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="addbe-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="addbe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="addbe-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="addbe-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="addbe-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="addbe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="addbe-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="addbe-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="addbe-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="addbe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="addbe-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="addbe-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="addbe-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="addbe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="addbe-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="addbe-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="addbe-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="addbe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="addbe-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="addbe-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="addbe-138">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="addbe-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="addbe-139">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="addbe-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="addbe-140">**información de MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="addbe-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





