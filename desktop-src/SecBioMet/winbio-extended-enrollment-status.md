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
# <a name="winbio_extended_enrollment_status-structure"></a>WINBIO \_ \_ estructura de estado de inscripción extendida \_

Contiene información adicional sobre el estado de una inscripción que está en curso.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**TemplateStatus**
</dt> <dd>

El estado de la recopilación de ejemplo para la plantilla de inscripción. Los valores siguientes son posibles para este miembro.



| Value                                                                                                                                                                                                  | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ correcto**</dt> </dl>                                                                     | La inscripción está lista para guardarse.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ \_ operación no válida \_**</dt> </dl> | No hay ninguna inscripción en curso.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_ más \_ datos**</dt> </dl>                         | Se requieren más muestras para completar la plantilla.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ \_ captura incorrecta \_**</dt> </dl>                   | El ejemplo más reciente no se puede usar.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

La razón por la que el ejemplo más reciente no se puede usar, si el valor del miembro **TemplateStatus** es **WINBIO \_ E \_ mala \_ Capture**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

La mejor estimación del adaptador de motor para el porcentaje de la plantilla que se ha completado, como un valor de 0 a 100.

</dd> <dt>

**Factor**
</dt> <dd>

El tipo de unidad biométrica para la que esta estructura contiene información sobre las capacidades y los requisitos de inscripción del adaptador de motor. Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de [**\_ \_ \_ información del motor extendido WINBIO**](winbio-extended-engine-info.md) se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .

</dd> <dt>

**Subfactor**
</dt> <dd>

Un valor de **\_ \_ subtipo biométrico WINBIO** que proporciona información adicional sobre la inscripción.

</dd> <dt>

**Cuestión**
</dt> <dd>

Información sobre el estado de una inscripción en curso para un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para las características faciales.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posición en el marco de la cámara de la parte del individuo que se va a inscribir, en píxeles. El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición. Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara. Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real de la superficie y la distancia focal ideal para la superficie. Este valor va de-100 a 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real de la superficie está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para patrones de huellas digitales.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

El número total de ejemplos necesarios para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**Centro**
</dt> <dd>

El número de muestras para el centro de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**Borde**
</dt> <dd>

El número de muestras para el borde superior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**BottomEdge**
</dt> <dd>

El número de muestras del borde inferior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**LeftEdge**
</dt> <dd>

El número de muestras para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**RightEdge**
</dt> <dd>

El número de muestras para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para los patrones de iris.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles. Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del iris del ojo. Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del iris del ojo del fotograma de la cámara. Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo adecuado del individuo.

El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición. Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara. Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Posición en el marco de la cámara de uno de los irises del individuo que se va a inscribir, en píxeles. Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío. Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea del iris del ojo izquierdo del individuo.

El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición. Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara. Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

Posición del centro de uno de los alumnos del individuo que se va a inscribir. Si el sistema de reconocimiento de iris solo está supervisando un ojo, esta posición es del centro del Pupil de ese ojo. Si el sistema de reconocimiento de iris está supervisando ambos ojos, pero solo hay un ojo en el fotograma de la cámara, esta posición es del centro del Pupil del ojo del fotograma de la cámara. Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la derecha del individuo.

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

Posición del centro de uno de los alumnos del individuo que se va a inscribir. Si el sistema de reconocimiento de iris solo está supervisando un ojo, o si solo hay un ojo en el fotograma de la cámara, este valor está vacío. Si el sistema de reconocimiento de iris está supervisando ambos ojos y ambos ojos están en el fotograma de la cámara, es probable que esta posición sea el centro del Pupil de la vista de la parte izquierda del individuo.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real del iris y la distancia focal ideal para el iris. Este valor va de-100 a 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real del iris está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para modelos de voz.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



 

 





