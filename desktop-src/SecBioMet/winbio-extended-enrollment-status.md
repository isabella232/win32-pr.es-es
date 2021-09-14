---
title: WINBIO_EXTENDED_ENROLLMENT_STATUS estructura (Winbio \_ types.h)
description: Contiene información adicional sobre el estado de una inscripción que está en curso.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS estructura Windows API de Marco biométrico
- PWINBIO_EXTENDED_ENROLLMENT_STATUS puntero de estructura Windows Biometric Framework API
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160763"
---
# <a name="winbio_extended_enrollment_status-structure"></a>ESTRUCTURA DE ESTADO \_ DE INSCRIPCIÓN \_ EXTENDIDA \_ DE WINBIO

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



## <a name="members"></a>Members

<dl> <dt>

**TemplateStatus**
</dt> <dd>

Estado de la colección de ejemplos para la plantilla de inscripción. Los siguientes valores son posibles para este miembro.



| Value                                                                                                                                                                                                  | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                     | La inscripción está lista para guardarse.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**OPERACIÓN WINBIO \_ E \_ INVALID \_**</dt> </dl> | No hay ninguna inscripción en curso.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> </dl>                         | Se requieren más ejemplos para completar la plantilla.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**CAPTURA DE \_ WINBIO E \_ \_ BAD**</dt> </dl>                   | El ejemplo más reciente no es utilizable.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

La razón por la que el ejemplo más reciente es inutilizable, si el valor del miembro **TemplateStatus** es **WINBIO \_ E BAD \_ \_ CAPTURE**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

La mejor estimación del adaptador del motor para el porcentaje de la plantilla que se ha completado, como un valor de 0 a 100.

</dd> <dt>

**Factor**
</dt> <dd>

Tipo de unidad biométrica para la que esta estructura contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor. Por ejemplo, si el valor del miembro **Factor** es **WINBIO \_ TYPE \_ FINGERPRINT**, la estructura DE INFORMACIÓN DEL MOTOR EXTENDIDO DE [**WINBIO \_ \_ \_**](winbio-extended-engine-info.md) se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **Specifc.Fingerprint.**

</dd> <dt>

**SubFactor**
</dt> <dd>

Valor **DE \_ \_ SUBTIPO BIOMÉTRICO DE WINBIO** que proporciona información adicional sobre la inscripción.

</dd> <dt>

**Específico**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**Características faciales**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para las características faciales.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posición dentro del marco de la cámara de la cara del individuo que se debe inscribir, en píxeles. El tamaño del marco de la cámara determina el límite superior en el número de píxeles para esta posición. Obtenga la **propiedad WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO** para determinar el tamaño del marco de la cámara. Un cliente que use el monitor de presencia debe realizar la operación de escalado para asignar la posición al marco de la cámara.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real de la cara y la distancia focal ideal para la cara. Este valor oscila entre -100 y 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real de la cara está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para los patrones de huella digital.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Número total de muestras necesarias para crear una nueva plantilla de huella digital.

</dd> <dt>

**Centro**
</dt> <dd>

Número de muestras para el centro de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**Topedge**
</dt> <dd>

Número de muestras para el borde superior de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Número de muestras para el borde inferior de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Número de muestras para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**RightEdge**
</dt> <dd>

Número de muestras para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para los patrones de iris.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Posición dentro del marco de la cámara de uno de los iris del individuo que se debe inscribir, en píxeles. Si el sistema de reconocimiento de iris solo supervisa un ojo, esta posición es del iris de ese ojo. Si el sistema de reconocimiento de iris supervisa ambos ojos, pero solo hay un ojo en el marco de la cámara, esta posición es del iris del ojo en el marco de la cámara. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea del iris del ojo derecho del individuo.

El tamaño del marco de la cámara determina el límite superior en el número de píxeles para esta posición. Obtenga la **propiedad WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO** para determinar el tamaño del marco de la cámara. Un cliente que use el monitor de presencia debe realizar la operación de escalado para asignar la posición al marco de la cámara.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Posición dentro del marco de la cámara de uno de los iris del individuo que se debe inscribir, en píxeles. Si el sistema de reconocimiento de iris solo supervisa un ojo o si solo hay un ojo en el marco de la cámara, este valor está vacío. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea de iris del ojo izquierdo del individuo.

El tamaño del marco de la cámara determina el límite superior en el número de píxeles para esta posición. Obtenga la **propiedad WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO** para determinar el tamaño del marco de la cámara. Un cliente que use el monitor de presencia debe realizar la operación de escalado para asignar la posición al marco de la cámara.

</dd> <dt>

**CenterCenter \_ 1**
</dt> <dd>

Posición del centro de una de las alumnos del individuo que se inscribirá. Si el sistema de reconocimiento de iris solo supervisa un ojo, esta posición es del centro de la alumno de ese ojo. Si el sistema de reconocimiento de iris supervisa ambos ojos, pero solo hay un ojo en el marco de la cámara, esta posición es del centro de la mirada del ojo en el marco de la cámara. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea del centro de la mirada del ojo derecho del individuo.

</dd> <dt>

**CenterCenter \_ 2**
</dt> <dd>

Posición del centro de una de las alumnos del individuo que se inscribirá. Si el sistema de reconocimiento de iris solo supervisa un ojo o si solo hay un ojo en el marco de la cámara, este valor está vacío. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea del centro de la afición del ojo izquierdo del individuo.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real del iris y la distancia focal ideal para el iris. Este valor oscila entre -100 y 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real del iris está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información sobre el estado de una inscripción que está en curso para los patrones de voz.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



 

 





