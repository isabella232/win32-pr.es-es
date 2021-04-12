---
title: WINBIO_PRESENCE_PROPERTIES Union (Winbio \_ Types. h)
description: Contiene valores biométricos que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES Unión Plataforma de biometría de Windows API
- Plataforma de biometría de Windows API de puntero de PWINBIO_PRESENCE_PROPERTIES Union
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489556"
---
# <a name="winbio_presence_properties-union"></a><span data-ttu-id="c53e4-105">WINBIO \_ Unión de propiedades de presencia \_</span><span class="sxs-lookup"><span data-stu-id="c53e4-105">WINBIO\_PRESENCE\_PROPERTIES union</span></span>

<span data-ttu-id="c53e4-106">Contiene valores biométricos que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.</span><span class="sxs-lookup"><span data-stu-id="c53e4-106">Contains biometric values that the Windows Biometric Framework used to determine that an individual was present.</span></span>

## <a name="syntax"></a><span data-ttu-id="c53e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c53e4-107">Syntax</span></span>


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a><span data-ttu-id="c53e4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c53e4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c53e4-109">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="c53e4-109">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-110">Valores de la ubicación de las características faciales que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.</span><span class="sxs-lookup"><span data-stu-id="c53e4-110">Values for the location of facial features that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="c53e4-111">**BoundingBox**</span><span class="sxs-lookup"><span data-stu-id="c53e4-111">**BoundingBox**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-112">Posición dentro del marco de la cámara de la parte del individuo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c53e4-112">The position within the camera frame of the face of the individual, in pixels.</span></span> <span data-ttu-id="c53e4-113">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="c53e4-113">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c53e4-114">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-114">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c53e4-115">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-115">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame .</span></span>

</dd> <dt>

<span data-ttu-id="c53e4-116">**Distancia**</span><span class="sxs-lookup"><span data-stu-id="c53e4-116">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-117">Distancia entre la ubicación real de la superficie y la distancia focal ideal para la superficie.</span><span class="sxs-lookup"><span data-stu-id="c53e4-117">The distance between the actual location of the face and the ideal focal distance for the face.</span></span> <span data-ttu-id="c53e4-118">Este valor va de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="c53e4-118">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c53e4-119">0 indica la distancia ideal, los valores positivos indican que la ubicación real de la superficie está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.</span><span class="sxs-lookup"><span data-stu-id="c53e4-119">0 indicates the ideal distance, positive values indicate that the actual location of the face is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c53e4-120">**Iris**</span><span class="sxs-lookup"><span data-stu-id="c53e4-120">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-121">Valores de la ubicación del iris que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.</span><span class="sxs-lookup"><span data-stu-id="c53e4-121">Values for iris location that the Windows Biometric Framework used to determine that an individual was present.</span></span>

<dl> <dt>

<span data-ttu-id="c53e4-122">**EyeBoundingBox \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c53e4-122">**EyeBoundingBox\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-123">Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c53e4-123">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c53e4-124">Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del iris del ojo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-124">If the iris-recognition system is only monitoring one eye, this position is of the iris of that eye.</span></span> <span data-ttu-id="c53e4-125">Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del iris del ojo del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-125">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the iris of the eye in the camera frame.</span></span> <span data-ttu-id="c53e4-126">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo adecuado del individuo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-126">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the iris of the right eye of the individual.</span></span>

<span data-ttu-id="c53e4-127">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="c53e4-127">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c53e4-128">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-128">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c53e4-129">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-129">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c53e4-130">**EyeBoundingBox \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c53e4-130">**EyeBoundingBox\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-131">Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c53e4-131">The position within the camera frame of one of the irises of the individual to enroll, in pixels.</span></span> <span data-ttu-id="c53e4-132">Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío.</span><span class="sxs-lookup"><span data-stu-id="c53e4-132">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c53e4-133">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo izquierdo del individuo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-133">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of iris of the left eye of the individual.</span></span>

<span data-ttu-id="c53e4-134">El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición.</span><span class="sxs-lookup"><span data-stu-id="c53e4-134">The size of the camera frame determines the upper limit on the number of pixels for this position.</span></span> <span data-ttu-id="c53e4-135">Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-135">Get the **WINBIO\_PROPERTY\_EXTENDED\_SENSOR\_INFO** property to determine the size of the camera frame.</span></span> <span data-ttu-id="c53e4-136">Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-136">A client that uses the presence monitor must perform the scaling operation to map the position to the camera frame.</span></span>

</dd> <dt>

<span data-ttu-id="c53e4-137">**PupilCenter \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c53e4-137">**PupilCenter\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-138">Posición del centro de uno de los alumnos del individuo que se va a inscribir.</span><span class="sxs-lookup"><span data-stu-id="c53e4-138">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c53e4-139">Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del centro del Pupil de ese ojo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-139">If the iris-recognition system is only monitoring one eye, this position is of the center of the pupil of that eye.</span></span> <span data-ttu-id="c53e4-140">Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del centro del Pupil del ojo del fotograma de la cámara.</span><span class="sxs-lookup"><span data-stu-id="c53e4-140">If the iris-recognition system is monitoring both eyes, but only one eye is in the camera frame, this position is of the center of the pupil of the eye in the camera frame.</span></span> <span data-ttu-id="c53e4-141">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la derecha del individuo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-141">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the right eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c53e4-142">**PupilCenter \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c53e4-142">**PupilCenter\_2**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-143">Posición del centro de uno de los alumnos del individuo que se va a inscribir.</span><span class="sxs-lookup"><span data-stu-id="c53e4-143">The position of the center of one of the pupils of the individual to enroll.</span></span> <span data-ttu-id="c53e4-144">Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío.</span><span class="sxs-lookup"><span data-stu-id="c53e4-144">If the iris-recognition system is only monitoring one eye, or if only one eye is in the camera frame, this value is empty.</span></span> <span data-ttu-id="c53e4-145">Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la parte izquierda del individuo.</span><span class="sxs-lookup"><span data-stu-id="c53e4-145">If the iris-recognition system is monitoring both eyes, and both eyes are in the camera frame, this position is probably of the center of the pupil of the left eye of the individual.</span></span>

</dd> <dt>

<span data-ttu-id="c53e4-146">**Distancia**</span><span class="sxs-lookup"><span data-stu-id="c53e4-146">**Distance**</span></span>
</dt> <dd>

<span data-ttu-id="c53e4-147">Distancia entre la ubicación real del iris y la distancia focal ideal para el iris.</span><span class="sxs-lookup"><span data-stu-id="c53e4-147">The distance between the actual location of the iris and the ideal focal distance for the iris.</span></span> <span data-ttu-id="c53e4-148">Este valor va de-100 a 100.</span><span class="sxs-lookup"><span data-stu-id="c53e4-148">This value ranges from -100 to 100.</span></span> <span data-ttu-id="c53e4-149">0 indica la distancia ideal, los valores positivos indican que la ubicación real del iris está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.</span><span class="sxs-lookup"><span data-stu-id="c53e4-149">0 indicates the ideal distance, positive values indicate that the actual location of the iris is too far away, and negative values indicate that the actual location is too close.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c53e4-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c53e4-150">Requirements</span></span>



| <span data-ttu-id="c53e4-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="c53e4-151">Requirement</span></span> | <span data-ttu-id="c53e4-152">Value</span><span class="sxs-lookup"><span data-stu-id="c53e4-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c53e4-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c53e4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c53e4-154">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c53e4-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c53e4-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c53e4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c53e4-156">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="c53e4-156">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c53e4-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c53e4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c53e4-158"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="c53e4-158"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





