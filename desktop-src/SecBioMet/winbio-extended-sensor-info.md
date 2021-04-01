---
title: Estructura de WINBIO_EXTENDED_SENSOR_INFO (Winbio \_ Types. h)
description: Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_SENSOR_INFO Structure
- PWINBIO_EXTENDED_SENSOR_INFO de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996038"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="36515-105">WINBIO \_ \_ estructura de información del sensor extendido \_</span><span class="sxs-lookup"><span data-stu-id="36515-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="36515-106">Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="36515-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="36515-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36515-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="36515-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="36515-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="36515-109">**GenericSensorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="36515-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="36515-110">Las capacidades genéricas del componente de sensor que está conectado a una unidad biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="36515-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="36515-111">**Factor**</span><span class="sxs-lookup"><span data-stu-id="36515-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="36515-112">El tipo de unidad biométrica para la que esta estructura contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor.</span><span class="sxs-lookup"><span data-stu-id="36515-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="36515-113">Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información del sensor extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="36515-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="36515-114">**Cuestión**</span><span class="sxs-lookup"><span data-stu-id="36515-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="36515-115">Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con un factor biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="36515-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="36515-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="36515-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="36515-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="36515-117">Reserved.</span></span> <span data-ttu-id="36515-118">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="36515-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="36515-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="36515-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="36515-120">Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con las características faciales.</span><span class="sxs-lookup"><span data-stu-id="36515-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="36515-121">**Tramas**</span><span class="sxs-lookup"><span data-stu-id="36515-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="36515-122">Tamaño del fotograma de la cámara, indicado como una longitud y un ancho en píxeles por los miembros **derecho** e **inferior** de la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36515-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="36515-123">El punto (0,0) representa la esquina superior izquierda del marco.</span><span class="sxs-lookup"><span data-stu-id="36515-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="36515-124">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="36515-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="36515-125">Desplazamiento del fotograma de la cámara para la superficie de la cámara de vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="36515-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="36515-126">Un valor de (0,0) indica que el fotograma de la cámara para la superficie y la cámara de vídeo se superponen por completo.</span><span class="sxs-lookup"><span data-stu-id="36515-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="36515-127">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="36515-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="36515-128">Orientación preferida para la cámara.</span><span class="sxs-lookup"><span data-stu-id="36515-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="36515-129">**Huella digital**</span><span class="sxs-lookup"><span data-stu-id="36515-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="36515-130">Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con patrones de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="36515-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="36515-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="36515-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="36515-132">Reservado.</span><span class="sxs-lookup"><span data-stu-id="36515-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="36515-133">**Iris**</span><span class="sxs-lookup"><span data-stu-id="36515-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="36515-134">Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de iris.</span><span class="sxs-lookup"><span data-stu-id="36515-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="36515-135">**Tramas**</span><span class="sxs-lookup"><span data-stu-id="36515-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="36515-136">Tamaño del fotograma de la cámara, indicado como una longitud y un ancho en píxeles por los miembros **derecho** e **inferior** de la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36515-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="36515-137">El punto (0,0) representa la esquina superior izquierda del marco.</span><span class="sxs-lookup"><span data-stu-id="36515-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="36515-138">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="36515-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="36515-139">Desplazamiento del fotograma de la cámara para el iris de la cámara de vídeo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="36515-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="36515-140">Un valor de (0,0) indica que el fotograma de la cámara del iris y la cámara de vídeo se superponen por completo.</span><span class="sxs-lookup"><span data-stu-id="36515-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="36515-141">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="36515-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="36515-142">Orientación preferida para la cámara.</span><span class="sxs-lookup"><span data-stu-id="36515-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="36515-143">**Voz**</span><span class="sxs-lookup"><span data-stu-id="36515-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="36515-144">Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de voz.</span><span class="sxs-lookup"><span data-stu-id="36515-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="36515-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="36515-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="36515-146">Reservado.</span><span class="sxs-lookup"><span data-stu-id="36515-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36515-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36515-147">Requirements</span></span>



| <span data-ttu-id="36515-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="36515-148">Requirement</span></span> | <span data-ttu-id="36515-149">Value</span><span class="sxs-lookup"><span data-stu-id="36515-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36515-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36515-150">Minimum supported client</span></span><br/> | <span data-ttu-id="36515-151">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="36515-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="36515-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36515-152">Minimum supported server</span></span><br/> | <span data-ttu-id="36515-153">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="36515-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="36515-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36515-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="36515-155"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="36515-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36515-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="36515-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36515-157">**Constantes de capacidad de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="36515-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="36515-158">**WINBIO \_ constantes de \_ tipo biométrico**</span><span class="sxs-lookup"><span data-stu-id="36515-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="36515-159">**Constantes de orientación de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="36515-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

