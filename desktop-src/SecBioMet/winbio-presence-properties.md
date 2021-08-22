---
title: WINBIO_PRESENCE_PROPERTIES union (Winbio \_ types.h)
description: Contiene valores biométricos que el Windows Biometric Framework usó para determinar que había un individuo presente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES union Windows Biometric Framework API
- PWINBIO_PRESENCE_PROPERTIES puntero de unión Windows Biometric Framework API
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
ms.openlocfilehash: 6a3964883f5dcd5b00c6f3eb6929c9deec99e58db014d18e51a192180a4d11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909660"
---
# <a name="winbio_presence_properties-union"></a>UNIÓN DE PROPIEDADES \_ DE WINBIO PRESENCE \_

Contiene valores biométricos que el Windows Biometric Framework usó para determinar que había un individuo presente.

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

**Características faciales**
</dt> <dd>

Valores para la ubicación de las características faciales que el Windows Biometric Framework usó para determinar que había un individuo presente.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posición dentro del marco de la cámara de la cara del individuo, en píxeles. El tamaño del marco de la cámara determina el límite superior en el número de píxeles para esta posición. Obtenga la **propiedad WINBIO \_ PROPERTY EXTENDED \_ SENSOR \_ \_ INFO** para determinar el tamaño del marco de la cámara. Un cliente que usa el monitor de presencia debe realizar la operación de escalado para asignar la posición al marco de la cámara.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real de la cara y la distancia focal ideal para la cara. Este valor oscila entre -100 y 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real de la cara está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Valores para la ubicación de iris que Windows marco biométrico usado para determinar que un individuo estaba presente.

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

Posición del centro de una de las alumnos del individuo que se inscribirá. Si el sistema de reconocimiento de iris solo supervisa un ojo, esta posición es del centro de la alumno de ese ojo. Si el sistema de reconocimiento de iris supervisa ambos ojos, pero solo hay un ojo en el marco de la cámara, esta posición es del centro de la mirada del ojo en el marco de la cámara. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea del centro de la afición del ojo derecho del individuo.

</dd> <dt>

**CenterCenter \_ 2**
</dt> <dd>

Posición del centro de una de las alumnos del individuo que se inscribirá. Si el sistema de reconocimiento de iris solo supervisa un ojo o si solo hay un ojo en el marco de la cámara, este valor está vacío. Si el sistema de reconocimiento de iris supervisa ambos ojos y ambos están en el marco de la cámara, esta posición probablemente sea del centro de la afición del ojo izquierdo del individuo.

</dd> <dt>

**Distancia**
</dt> <dd>

Distancia entre la ubicación real del iris y la distancia focal ideal para el iris. Este valor oscila entre -100 y 100. 0 indica la distancia ideal, los valores positivos indican que la ubicación real del iris está demasiado lejos y los valores negativos indican que la ubicación real es demasiado cercana.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



 

 





