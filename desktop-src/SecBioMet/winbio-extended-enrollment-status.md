---
title: Estructura de WINBIO_EXTENDED_ENROLLMENT_STATUS (Winbio \_ Types. h)
description: Contiene información adicional sobre el estado de una inscripción que está en curso.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_ENROLLMENT_STATUS Structure
- PWINBIO_EXTENDED_ENROLLMENT_STATUS de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150010"
---
# <a name="winbio_extended_enrollment_status-structure"></a><span data-ttu-id="a0baf-105">WINBIO \_ \_ estructura de estado de inscripción extendida \_</span><span class="sxs-lookup"><span data-stu-id="a0baf-105">WINBIO\_EXTENDED\_ENROLLMENT\_STATUS structure</span></span>

<span data-ttu-id="a0baf-106">Contiene información adicional sobre el estado de una inscripción que está en curso.</span><span class="sxs-lookup"><span data-stu-id="a0baf-106">Contains additional information about the status of an enrollment that is in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0baf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0baf-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="a0baf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0baf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-109">**TemplateStatus**</span><span class="sxs-lookup"><span data-stu-id="a0baf-109">**TemplateStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-110">El estado de la recopilación de ejemplo para la plantilla de inscripción.</span><span class="sxs-lookup"><span data-stu-id="a0baf-110">The status of sample collection for the enrollment template.</span></span> <span data-ttu-id="a0baf-111">Los valores siguientes son posibles para este miembro.</span><span class="sxs-lookup"><span data-stu-id="a0baf-111">The following values are possible for this member.</span></span>



| <span data-ttu-id="a0baf-112">Value</span><span class="sxs-lookup"><span data-stu-id="a0baf-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="a0baf-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a0baf-113">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="a0baf-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a0baf-114"><dt>**S\_OK**</dt></span></span> </dl>                                                                     | <span data-ttu-id="a0baf-115">La inscripción está lista para guardarse.</span><span class="sxs-lookup"><span data-stu-id="a0baf-115">The enrollment is ready to be saved.</span></span><br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <span data-ttu-id="a0baf-116"><dt>**WINBIO \_ \_ operación no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0baf-116"><dt>**WINBIO\_E\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a0baf-117">No hay ninguna inscripción en curso.</span><span class="sxs-lookup"><span data-stu-id="a0baf-117">No enrollment is in progress.</span></span><br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <span data-ttu-id="a0baf-118"><dt>**WINBIO \_ \_ más \_ datos**</dt></span><span class="sxs-lookup"><span data-stu-id="a0baf-118"><dt>**WINBIO\_I\_MORE\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="a0baf-119">Se requieren más muestras para completar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="a0baf-119">More samples are required to complete the template.</span></span><br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <span data-ttu-id="a0baf-120"><dt>**WINBIO \_ \_ captura incorrecta \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0baf-120"><dt>**WINBIO\_E\_BAD\_CAPTURE**</dt></span></span> </dl>                   | <span data-ttu-id="a0baf-121">El ejemplo más reciente no se puede usar.</span><span class="sxs-lookup"><span data-stu-id="a0baf-121">The most recent sample is not usable.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="a0baf-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="a0baf-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-123">La razón por la que el ejemplo más reciente no se puede usar, si el valor del miembro **TemplateStatus** es **WINBIO \_ E \_ mala \_ Capture**.</span><span class="sxs-lookup"><span data-stu-id="a0baf-123">The reason that the most recent sample is unusable, if the value of the **TemplateStatus** member is **WINBIO\_E\_BAD\_CAPTURE**.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-124">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="a0baf-124">**PercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-125">La mejor estimación del adaptador de motor para el porcentaje de la plantilla que se ha completado, como un valor de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="a0baf-125">The best estimate from the engine adapter for the percentage of the template that is complete, as a value from 0 to 100.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-126">**Factor**</span><span class="sxs-lookup"><span data-stu-id="a0baf-126">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-127">El tipo de unidad biométrica para la que esta estructura contiene información sobre las capacidades y los requisitos de inscripción del adaptador de motor.</span><span class="sxs-lookup"><span data-stu-id="a0baf-127">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="a0baf-128">Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de [**\_ \_ \_ información del motor extendido WINBIO**](winbio-extended-engine-info.md) se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="a0baf-128">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-129">**Subfactor**</span><span class="sxs-lookup"><span data-stu-id="a0baf-129">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-130">Un valor de **\_ \_ subtipo biométrico WINBIO** que proporciona información adicional sobre la inscripción.</span><span class="sxs-lookup"><span data-stu-id="a0baf-130">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that provides additional information about the enrollment.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-131">**Cuestión**</span><span class="sxs-lookup"><span data-stu-id="a0baf-131">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-132">Información sobre el estado de una inscripción en curso para un factor biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="a0baf-132">Information about the status of an enrollment that is in progress for a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-133">**Null**</span><span class="sxs-lookup"><span data-stu-id="a0baf-133">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-134">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a0baf-134">Reserved.</span></span> <span data-ttu-id="a0baf-135">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a0baf-135">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-136">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="a0baf-136">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-137">Información sobre el estado de una inscripción que está en curso para las características faciales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-137">Information about the status of an enrollment that is in progress for facial features.</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-138">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="a0baf-138">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-139">Posición en el marco de la cámara de la parte del individuo que se va a inscribir, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a0baf-139">The position within the camera frame of the face of the individual to enroll, in pixels.</span></span> <span data-ttu-id="a0baf-140">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="a0baf-140">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="a0baf-141">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-141">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="a0baf-142">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-142">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-143">**Distancia**</span><span class="sxs-lookup"><span data-stu-id="a0baf-143">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-144">Distancia entre la ubicación real de la superficie y la distancia focal ideal para la superficie.</span><span class="sxs-lookup"><span data-stu-id="a0baf-144">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="a0baf-145">Este valor va de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="a0baf-145">This value ranges from -100 to 100.</span></span> <span data-ttu-id="a0baf-146">0 indica la distancia ideal, los valores positivos indican que la ubicación real de la superficie está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.</span><span class="sxs-lookup"><span data-stu-id="a0baf-146">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0baf-147">**Huella digital**</span><span class="sxs-lookup"><span data-stu-id="a0baf-147">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-148">Información sobre el estado de una inscripción que está en curso para patrones de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-148">Information about the status of an enrollment that is in progress for fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-149">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="a0baf-149">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-150">El número total de ejemplos necesarios para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-150">The total number of samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-151">**Centro**</span><span class="sxs-lookup"><span data-stu-id="a0baf-151">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-152">El número de muestras para el centro de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-152">The number of samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-153">**Borde**</span><span class="sxs-lookup"><span data-stu-id="a0baf-153">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-154">El número de muestras para el borde superior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-154">The number of samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-155">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="a0baf-155">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-156">El número de muestras del borde inferior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-156">The number of samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-157">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="a0baf-157">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-158">El número de muestras para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-158">The number of samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-159">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="a0baf-159">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-160">El número de muestras para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="a0baf-160">The number of samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0baf-161">**Iris**</span><span class="sxs-lookup"><span data-stu-id="a0baf-161">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-162">Información sobre el estado de una inscripción que está en curso para los patrones de iris.</span><span class="sxs-lookup"><span data-stu-id="a0baf-162">Information about the status of an enrollment that is in progress for iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-163">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a0baf-163">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-164">Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a0baf-164">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="a0baf-165">Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del iris del ojo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-165">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="a0baf-166">Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del iris del ojo del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-166">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="a0baf-167">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo adecuado del individuo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-167">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="a0baf-168">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="a0baf-168">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="a0baf-169">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-169">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="a0baf-170">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-170">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-171">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a0baf-171">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-172">Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a0baf-172">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="a0baf-173">Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío.</span><span class="sxs-lookup"><span data-stu-id="a0baf-173">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="a0baf-174">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo izquierdo del individuo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-174">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="a0baf-175">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="a0baf-175">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="a0baf-176">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-176">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="a0baf-177">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-177">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-178">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a0baf-178">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-179">Posición del centro de uno de los alumnos del individuo que se va a inscribir.</span><span class="sxs-lookup"><span data-stu-id="a0baf-179">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="a0baf-180">Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del centro del Pupil de ese ojo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-180">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="a0baf-181">Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del centro del Pupil del ojo del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="a0baf-181">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="a0baf-182">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la derecha del individuo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-182">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-183">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a0baf-183">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-184">Posición del centro de uno de los alumnos del individuo que se va a inscribir.</span><span class="sxs-lookup"><span data-stu-id="a0baf-184">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="a0baf-185">Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío.</span><span class="sxs-lookup"><span data-stu-id="a0baf-185">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="a0baf-186">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la parte izquierda del individuo.</span><span class="sxs-lookup"><span data-stu-id="a0baf-186">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="a0baf-187">**Distancia**</span><span class="sxs-lookup"><span data-stu-id="a0baf-187">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-188">Distancia entre la ubicación real del iris y la distancia focal ideal para el iris.</span><span class="sxs-lookup"><span data-stu-id="a0baf-188">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="a0baf-189">Este valor va de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="a0baf-189">This value ranges from -100 to 100.</span></span> <span data-ttu-id="a0baf-190">0 indica la distancia ideal, los valores positivos indican que la ubicación real del iris está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.</span><span class="sxs-lookup"><span data-stu-id="a0baf-190">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0baf-191">**Voz**</span><span class="sxs-lookup"><span data-stu-id="a0baf-191">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-192">Información sobre el estado de una inscripción que está en curso para modelos de voz.</span><span class="sxs-lookup"><span data-stu-id="a0baf-192">Information about the status of an enrollment that is in progress for voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="a0baf-193">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a0baf-193">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a0baf-194">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a0baf-194">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0baf-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0baf-195">Requirements</span></span>



| <span data-ttu-id="a0baf-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0baf-196">Requirement</span></span> | <span data-ttu-id="a0baf-197">Value</span><span class="sxs-lookup"><span data-stu-id="a0baf-197">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0baf-198">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0baf-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a0baf-199">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0baf-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a0baf-200">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0baf-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a0baf-201">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0baf-201">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="a0baf-202">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0baf-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0baf-203"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="a0baf-203"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





