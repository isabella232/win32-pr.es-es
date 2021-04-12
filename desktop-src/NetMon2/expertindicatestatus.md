---
description: La función ExpertIndicateStatus indica el porcentaje de finalización del análisis de expertos del archivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Función ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153865"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="45741-103">ExpertIndicateStatus función)</span><span class="sxs-lookup"><span data-stu-id="45741-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="45741-104">La función **ExpertIndicateStatus** indica el porcentaje de finalización del análisis del experto en el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="45741-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="45741-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45741-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="45741-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45741-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45741-107">*hExpertKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45741-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45741-108">Identificador de experto único.</span><span class="sxs-lookup"><span data-stu-id="45741-108">Unique expert identifier.</span></span> <span data-ttu-id="45741-109">Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="45741-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="45741-110">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="45741-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45741-111">Estado actual del análisis.</span><span class="sxs-lookup"><span data-stu-id="45741-111">Current status of the analysis.</span></span> <span data-ttu-id="45741-112">Especifique uno de los siguientes valores de [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="45741-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="45741-113">Value</span><span class="sxs-lookup"><span data-stu-id="45741-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="45741-114">Significado</span><span class="sxs-lookup"><span data-stu-id="45741-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="45741-115"><dt>**EXPERTSTATUS \_ INactivo**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="45741-116">El experto nunca comenzó.</span><span class="sxs-lookup"><span data-stu-id="45741-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="45741-117"><dt>**Inicio de EXPERTSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="45741-118">Se está iniciando el experto.</span><span class="sxs-lookup"><span data-stu-id="45741-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="45741-119"><dt>**EXPERTSTATUS en \_ ejecución**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="45741-120">El experto se ejecuta con normalidad.</span><span class="sxs-lookup"><span data-stu-id="45741-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="45741-121"><dt>**problema de EXPERTSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="45741-122">Un problema especificado en el parámetro substatus detuvo el experto.</span><span class="sxs-lookup"><span data-stu-id="45741-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="45741-123"><dt>**EXPERTSTATUS \_ anulado**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="45741-124">Monitor de red detuvo el experto.</span><span class="sxs-lookup"><span data-stu-id="45741-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="45741-125"><dt>**EXPERTSTATUS \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="45741-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="45741-126">El experto ha finalizado el análisis correctamente.</span><span class="sxs-lookup"><span data-stu-id="45741-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="45741-127">*Subestado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45741-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45741-128">Extensión o aclaración de la información proporcionada por el parámetro *status* .</span><span class="sxs-lookup"><span data-stu-id="45741-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="45741-129">*szText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45741-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45741-130">Indicador de estado de texto opcional.</span><span class="sxs-lookup"><span data-stu-id="45741-130">Optional text status indicator.</span></span>

<span data-ttu-id="45741-131">Este valor de parámetro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="45741-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="45741-132">*PercentDone* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="45741-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45741-133">Porcentaje de los datos de captura que ha procesado el experto.</span><span class="sxs-lookup"><span data-stu-id="45741-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="45741-134">Cuando el experto completa correctamente el análisis de un archivo de captura, el sistema establece el porcentaje en 100.</span><span class="sxs-lookup"><span data-stu-id="45741-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="45741-135">Se omitirá cualquier número mayor que 99.</span><span class="sxs-lookup"><span data-stu-id="45741-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45741-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45741-136">Return value</span></span>

<span data-ttu-id="45741-137">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="45741-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="45741-138">Si la función no es correcta, el valor devuelto es NMERR \_ Expert \_ Terminate; el experto debe limpiar y volver inmediatamente sin completar la captura.</span><span class="sxs-lookup"><span data-stu-id="45741-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="45741-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45741-139">Remarks</span></span>

<span data-ttu-id="45741-140">La función **ExpertIndicateStatus** solo puede ser llamada por expertos que implementan la función de exportación [Ejecutar](run.md) o [configurar](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="45741-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="45741-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45741-141">Requirements</span></span>



| <span data-ttu-id="45741-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="45741-142">Requirement</span></span> | <span data-ttu-id="45741-143">Value</span><span class="sxs-lookup"><span data-stu-id="45741-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45741-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45741-144">Minimum supported client</span></span><br/> | <span data-ttu-id="45741-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="45741-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="45741-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45741-146">Minimum supported server</span></span><br/> | <span data-ttu-id="45741-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45741-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="45741-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45741-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="45741-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="45741-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="45741-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45741-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="45741-151"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45741-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="45741-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45741-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45741-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45741-153"><dt>Nmapi.dll</dt></span></span> </dl> |
