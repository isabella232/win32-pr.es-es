---
title: Estructura de WINBIO_EXTENDED_ENGINE_INFO (Winbio \_ Types. h)
description: Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_ENGINE_INFO Structure
- PWINBIO_EXTENDED_ENGINE_INFO de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905617"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="ec553-105">WINBIO \_ \_ estructura de información del motor extendido \_</span><span class="sxs-lookup"><span data-stu-id="ec553-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="ec553-106">Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="ec553-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec553-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec553-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="ec553-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec553-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec553-109">**GenericEngineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ec553-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-110">Las capacidades genéricas del componente del motor que está conectado a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="ec553-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="ec553-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-112">El tipo de unidad biométrica para la que esta estructura contiene información sobre las capacidades y los requisitos de inscripción del adaptador de motor.</span><span class="sxs-lookup"><span data-stu-id="ec553-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="ec553-113">Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información del motor extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="ec553-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-114">**Cuestión**</span><span class="sxs-lookup"><span data-stu-id="ec553-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-115">Información sobre las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con un factor biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="ec553-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="ec553-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-117">Reserved.</span></span> <span data-ttu-id="ec553-118">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="ec553-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-120">Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con las características faciales.</span><span class="sxs-lookup"><span data-stu-id="ec553-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ec553-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-122">Reserved.</span></span> <span data-ttu-id="ec553-123">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-124">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="ec553-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec553-125">**Null**</span><span class="sxs-lookup"><span data-stu-id="ec553-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-126">Reserved.</span></span> <span data-ttu-id="ec553-127">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="ec553-128">**Huella digital**</span><span class="sxs-lookup"><span data-stu-id="ec553-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-129">Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con patrones de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ec553-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-131">Reserved.</span></span> <span data-ttu-id="ec553-132">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-133">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="ec553-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-134">El número de buenos ejemplos necesarios para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-135">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="ec553-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-136">El número total de buenos ejemplos necesarios para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-137">**Centro**</span><span class="sxs-lookup"><span data-stu-id="ec553-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-138">El número de buenos ejemplos para el centro de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-139">**Borde**</span><span class="sxs-lookup"><span data-stu-id="ec553-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-140">El número de buenos ejemplos para el borde superior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-141">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="ec553-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-142">El número de buenos ejemplos para el borde inferior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-143">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="ec553-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-144">El número de buenos ejemplos para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-145">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="ec553-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-146">El número de buenos ejemplos para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="ec553-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="ec553-147">**Iris**</span><span class="sxs-lookup"><span data-stu-id="ec553-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-148">Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con los patrones de iris.</span><span class="sxs-lookup"><span data-stu-id="ec553-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ec553-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-150">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-150">Reserved.</span></span> <span data-ttu-id="ec553-151">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-152">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="ec553-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec553-153">**Null**</span><span class="sxs-lookup"><span data-stu-id="ec553-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-154">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-154">Reserved.</span></span> <span data-ttu-id="ec553-155">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="ec553-156">**Voz**</span><span class="sxs-lookup"><span data-stu-id="ec553-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-157">Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con los patrones de voz.</span><span class="sxs-lookup"><span data-stu-id="ec553-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="ec553-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ec553-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-159">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-159">Reserved.</span></span> <span data-ttu-id="ec553-160">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ec553-161">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="ec553-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec553-162">**Null**</span><span class="sxs-lookup"><span data-stu-id="ec553-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="ec553-163">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec553-163">Reserved.</span></span> <span data-ttu-id="ec553-164">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ec553-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec553-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec553-165">Requirements</span></span>



| <span data-ttu-id="ec553-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec553-166">Requirement</span></span> | <span data-ttu-id="ec553-167">Value</span><span class="sxs-lookup"><span data-stu-id="ec553-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec553-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec553-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ec553-169">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec553-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="ec553-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec553-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ec553-171">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec553-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="ec553-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec553-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec553-173"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="ec553-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec553-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec553-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec553-175">**Constantes de capacidad de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="ec553-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="ec553-176">**WINBIO \_ constantes de \_ tipo biométrico**</span><span class="sxs-lookup"><span data-stu-id="ec553-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





