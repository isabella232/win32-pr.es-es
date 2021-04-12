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
# <a name="winbio_presence_properties-union"></a>WINBIO \_ Unión de propiedades de presencia \_

Contiene valores biométricos que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**FacialFeatures**
</dt> <dd>

Valores de la ubicación de las características faciales que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posición dentro del marco de la cámara de la parte del individuo, en píxeles. El tamaño del fotograma de la cámara determina el límite superior del número de píxeles para esta posición. Obtiene la propiedad de **\_ \_ \_ \_ información del sensor extendido de la propiedad WINBIO** para determinar el tamaño del fotograma de la cámara. Un cliente que utiliza el monitor de presencia debe realizar la operación de escalado para asignar la posición al fotograma de la cámara.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real de la superficie y la distancia focal ideal para la superficie. Este valor va de-100 a 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real de la superficie está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Valores de la ubicación del iris que el Plataforma de biometría de Windows utilizar para determinar que un individuo estaba presente.

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

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



 

 





