---
title: Win32_WinSAT (clase)
description: Define la información de evaluación de resumen para la evaluación formal más reciente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- WinSAT de clase de Win32_WinSAT
- Win32_WinSAT de clase WinSAT, descrito
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705187"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="3189d-105">Win32 \_ WinSAT (clase)</span><span class="sxs-lookup"><span data-stu-id="3189d-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="3189d-106">\[**Win32 \_** Es posible que WinSAT se modifique o no esté disponible para las versiones después de Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="3189d-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="3189d-107">Define la información de evaluación de resumen para la evaluación formal más reciente.</span><span class="sxs-lookup"><span data-stu-id="3189d-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="3189d-108">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3189d-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3189d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3189d-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="3189d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3189d-110">Members</span></span>

<span data-ttu-id="3189d-111">La clase de **Win32 \_ WinSAT** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3189d-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="3189d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3189d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3189d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3189d-113">Properties</span></span>

<span data-ttu-id="3189d-114">La clase de **Win32 \_ WinSAT** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3189d-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3189d-115">**CPUScore**</span><span class="sxs-lookup"><span data-stu-id="3189d-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-116">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-118">Una puntuación para los procesadores del equipo.</span><span class="sxs-lookup"><span data-stu-id="3189d-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="3189d-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-120">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-122">Después Windows 8.1, WinSAT ya no evaluará las capacidades de los gráficos tridimensionales (juegos) del equipo y la capacidad del controlador de gráficos para representar objetos y ejecutar sombreadores mediante esta evaluación.</span><span class="sxs-lookup"><span data-stu-id="3189d-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="3189d-123">Por compatibilidad, WinSAT informa de los valores de centinela de las métricas y puntuaciones, pero no se calculan en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="3189d-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-124">**DiskScore**</span><span class="sxs-lookup"><span data-stu-id="3189d-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-125">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-127">Una puntuación para el rendimiento de lectura secuencial en el disco duro principal del equipo.</span><span class="sxs-lookup"><span data-stu-id="3189d-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-128">**GraphicsScore**</span><span class="sxs-lookup"><span data-stu-id="3189d-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-129">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-131">Una puntuación para las capacidades de gráficos del equipo.</span><span class="sxs-lookup"><span data-stu-id="3189d-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-132">**MemoryScore**</span><span class="sxs-lookup"><span data-stu-id="3189d-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-133">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-135">Una puntuación para el rendimiento de la memoria y la capacidad del equipo.</span><span class="sxs-lookup"><span data-stu-id="3189d-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="3189d-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3189d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3189d-139">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3189d-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="3189d-140">Esta propiedad debe establecerse en "MostRecentAssessment" en la cláusula WHERE de la consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="3189d-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="3189d-141">**WinSATAssessmentState**</span><span class="sxs-lookup"><span data-stu-id="3189d-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3189d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-144">Estado de la evaluación.</span><span class="sxs-lookup"><span data-stu-id="3189d-144">State of the assessment.</span></span> <span data-ttu-id="3189d-145">Para obtener una descripción de los valores posibles, vea la enumeración [**\_ \_ Estado de evaluación de WINSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .</span><span class="sxs-lookup"><span data-stu-id="3189d-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="3189d-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span><span class="sxs-lookup"><span data-stu-id="3189d-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3189d-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Válido** (1)</span><span class="sxs-lookup"><span data-stu-id="3189d-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3189d-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span><span class="sxs-lookup"><span data-stu-id="3189d-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3189d-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span><span class="sxs-lookup"><span data-stu-id="3189d-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3189d-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**No válido** (4)</span><span class="sxs-lookup"><span data-stu-id="3189d-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3189d-151">**WinSPRLevel**</span><span class="sxs-lookup"><span data-stu-id="3189d-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3189d-152">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="3189d-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3189d-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3189d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3189d-154">Puntuación base del equipo.</span><span class="sxs-lookup"><span data-stu-id="3189d-154">Base score for the computer.</span></span> <span data-ttu-id="3189d-155">Para obtener más información sobre el valor de puntuación, vea la propiedad [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .</span><span class="sxs-lookup"><span data-stu-id="3189d-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3189d-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3189d-156">Remarks</span></span>

<span data-ttu-id="3189d-157">Para obtener información sobre las puntuaciones de subcomponentes, como **MemoryScore**, vea la propiedad [**IProvideWinSATAssessmentInfo:: score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .</span><span class="sxs-lookup"><span data-stu-id="3189d-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="3189d-158">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3189d-158">Examples</span></span>

<span data-ttu-id="3189d-159">Para obtener un ejemplo en el que se muestra cómo usar WMI para recuperar datos de esta clase, vea el método [**IProvideWinSATVisuals:: get \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .</span><span class="sxs-lookup"><span data-stu-id="3189d-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3189d-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3189d-160">Requirements</span></span>



| <span data-ttu-id="3189d-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="3189d-161">Requirement</span></span> | <span data-ttu-id="3189d-162">Value</span><span class="sxs-lookup"><span data-stu-id="3189d-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3189d-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3189d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="3189d-164">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3189d-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3189d-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3189d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="3189d-166">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3189d-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3189d-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3189d-167">Namespace</span></span><br/>                | <span data-ttu-id="3189d-168">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3189d-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="3189d-169">MOF</span><span class="sxs-lookup"><span data-stu-id="3189d-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3189d-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3189d-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="3189d-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3189d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3189d-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3189d-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 





