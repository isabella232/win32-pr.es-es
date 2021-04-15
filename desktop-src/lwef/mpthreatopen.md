---
title: Función MpThreatOpen (MpClient. h)
description: Devuelve un identificador de enumeración con el fin de recuperar las amenazas.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Función MpThreatOpen características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665999"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="19cdf-104">MpThreatOpen función)</span><span class="sxs-lookup"><span data-stu-id="19cdf-104">MpThreatOpen function</span></span>

<span data-ttu-id="19cdf-105">Devuelve un identificador de enumeración con el fin de recuperar las amenazas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="19cdf-106">Esta función se puede usar para abrir amenazas detectadas por un análisis específico, todas las amenazas activas del sistema, el historial de la desinfección de amenazas o todas las amenazas presentes en la base de datos de firmas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cdf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19cdf-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="19cdf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19cdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cdf-109">*hScanHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cdf-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="19cdf-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="19cdf-111">Puede ser un identificador de una operación de examen completada, devuelta por la función [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="19cdf-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="19cdf-112">Como alternativa, este parámetro se puede establecer en el identificador de la interfaz del administrador de protección contra malware devuelto por [**MpManagerOpen**](mpmanageropen.md) para enumerar todas las amenazas activas del sistema, el historial de la desinfección de amenazas o las amenazas de la base de datos de firmas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="19cdf-113">*ThreatSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cdf-114">Tipo: **MPTHREAT \_ source**</span><span class="sxs-lookup"><span data-stu-id="19cdf-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="19cdf-115">Se usa para controlar el origen de la enumeración de amenazas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="19cdf-116">Los valores posibles para este parámetro son:</span><span class="sxs-lookup"><span data-stu-id="19cdf-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="19cdf-117">Value</span><span class="sxs-lookup"><span data-stu-id="19cdf-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="19cdf-118">Significado</span><span class="sxs-lookup"><span data-stu-id="19cdf-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="19cdf-119"><dt>**\_examen de origen de MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="19cdf-120">Amenazas asociadas al identificador de examen específico.</span><span class="sxs-lookup"><span data-stu-id="19cdf-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="19cdf-121"><dt>**origen de MPTHREAT \_ \_ activo**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="19cdf-122">Amenazas que están activas actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="19cdf-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="19cdf-123"><dt>**\_historial de origen de MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="19cdf-124">Amenazas a las que se les actúa y se conserva como historial.</span><span class="sxs-lookup"><span data-stu-id="19cdf-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="19cdf-125"><dt>**MPTHREAT \_ cuarentena de origen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="19cdf-126">Amenazas que se ponen en cuarentena.</span><span class="sxs-lookup"><span data-stu-id="19cdf-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="19cdf-127"><dt>**\_firma de origen de MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="19cdf-128">Amenazas que se pueden detectar con la base de datos de firmas actual.</span><span class="sxs-lookup"><span data-stu-id="19cdf-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="19cdf-129"><dt>**\_Estado de origen de MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="19cdf-130">Amenazas que han actuado recientemente.</span><span class="sxs-lookup"><span data-stu-id="19cdf-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="19cdf-131">("Recientemente" se define mediante una configuración interna configurable).</span><span class="sxs-lookup"><span data-stu-id="19cdf-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="19cdf-132">*ThreatType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cdf-133">Tipo: **MPTHREAT \_ Type**</span><span class="sxs-lookup"><span data-stu-id="19cdf-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="19cdf-134">Se utiliza para filtrar amenazas enumeradas en función del tipo de detección.</span><span class="sxs-lookup"><span data-stu-id="19cdf-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="19cdf-135">Los valores posibles para este parámetro son:</span><span class="sxs-lookup"><span data-stu-id="19cdf-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="19cdf-136">Value</span><span class="sxs-lookup"><span data-stu-id="19cdf-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="19cdf-137">Significado</span><span class="sxs-lookup"><span data-stu-id="19cdf-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="19cdf-138"><dt>**MPTHREAT \_ Type \_ KNOWNBAD**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="19cdf-139">La detección se realiza en función de una firma específica, emulación u otro método de detección de amenazas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="19cdf-140"><dt>**tipo de MPTHREAT \_ \_ sospechoso**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="19cdf-141">La detección se realiza en función de la supervisión del comportamiento.</span><span class="sxs-lookup"><span data-stu-id="19cdf-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="19cdf-142"><dt>**\_tipo MPTHREAT \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="19cdf-143">La detección se realiza en función de amenazas desconocidas (sin clasificar).</span><span class="sxs-lookup"><span data-stu-id="19cdf-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="19cdf-144"><dt>**MPTHREAT \_ Type \_ KNOWNGOOD**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="19cdf-145">La detección se realiza en función de amenazas seguras conocidas.</span><span class="sxs-lookup"><span data-stu-id="19cdf-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="19cdf-146"><dt>**MPTHREAT \_ tipo \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="19cdf-147">La detección se realiza en función de las amenazas de NIS.</span><span class="sxs-lookup"><span data-stu-id="19cdf-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="19cdf-148">*phThreatEnumHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19cdf-149">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="19cdf-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="19cdf-150">Identificador de enumeración de amenazas devuelto que identifica el contexto de enumeración.</span><span class="sxs-lookup"><span data-stu-id="19cdf-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="19cdf-151">Este identificador se puede usar para enumerar información de amenazas mediante [**MpThreatEnumerate**](mpthreatenumerate.md).</span><span class="sxs-lookup"><span data-stu-id="19cdf-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="19cdf-152">El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="19cdf-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cdf-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19cdf-153">Return value</span></span>

<span data-ttu-id="19cdf-154">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19cdf-154">Type: **HRESULT**</span></span>

<span data-ttu-id="19cdf-155">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="19cdf-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="19cdf-156">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="19cdf-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="19cdf-157">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="19cdf-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cdf-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19cdf-158">Requirements</span></span>



| <span data-ttu-id="19cdf-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="19cdf-159">Requirement</span></span> | <span data-ttu-id="19cdf-160">Value</span><span class="sxs-lookup"><span data-stu-id="19cdf-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19cdf-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19cdf-161">Minimum supported client</span></span><br/> | <span data-ttu-id="19cdf-162">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="19cdf-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19cdf-163">Minimum supported server</span></span><br/> | <span data-ttu-id="19cdf-164">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="19cdf-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19cdf-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19cdf-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="19cdf-166"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="19cdf-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19cdf-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19cdf-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19cdf-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19cdf-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="19cdf-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cdf-170">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="19cdf-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="19cdf-171">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="19cdf-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="19cdf-172">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="19cdf-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="19cdf-173">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="19cdf-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="19cdf-174">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="19cdf-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





