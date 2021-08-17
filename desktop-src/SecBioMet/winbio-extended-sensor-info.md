---
title: WINBIO_EXTENDED_SENSOR_INFO estructura (Winbio \_ types.h)
description: Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO estructura Windows API de marco biométrico
- PWINBIO_EXTENDED_SENSOR_INFO puntero de estructura Windows API de marco biométrico
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
ms.openlocfilehash: dd8c323b4f4e3847c399e314da22048f658fb68c3b07ecf82f71ce0ed327c368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910423"
---
# <a name="winbio_extended_sensor_info-structure"></a>Estructura WINBIO \_ EXTENDED \_ SENSOR \_ INFO

Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**GenericSensorCapabilities**
</dt> <dd>

Funcionalidades genéricas del componente de sensor que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

Tipo de unidad biométrica para la que esta estructura contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador del sensor. Por ejemplo, si el valor del miembro **Factor** es **WINBIO \_ TYPE \_ FINGERPRINT**, la estructura **WINBIO EXTENDED SENSOR \_ \_ \_ INFO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **Specifc.Fingerprint.**

</dd> <dt>

**Específico**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**Características faciales**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con las características faciales.

<dl> <dt>

**FrameSize**
</dt> <dd>

Tamaño del marco de la cámara, indicado como longitud  y ancho en píxeles por los miembros derecho **e** inferior de la [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) El punto (0, 0) representa la esquina superior izquierda del marco.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Desplazamiento del marco de la cámara para la cara de la cámara de vídeo, en píxeles. Un valor de (0, 0) indica que el marco de la cámara para la cara y la cámara de vídeo se superponen completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientación preferida para la cámara.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de huella digital.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de iris.

<dl> <dt>

**FrameSize**
</dt> <dd>

Tamaño del marco de la cámara, indicado como longitud  y ancho en píxeles por los miembros derecho **e** inferior de la [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) El punto (0, 0) representa la esquina superior izquierda del marco.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Desplazamiento del marco de la cámara para el iris de la cámara de vídeo, en píxeles. Un valor de (0, 0) indica que el marco de la cámara para el iris y la cámara de vídeo se superponen completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientación preferida para la cámara.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de voz.

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
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluye Winbio.h para aplicaciones cliente o Adaptadores de \_ Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes DE FUNCIONALIDAD DE WINBIO \_**](winbio-capability-constants.md)
</dt> <dt>

[**Constantes DE \_ TIPO BIOMÉTRICO DE WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes DE ORIENTACIÓN DE WINBIO \_**](winbio-orientation-constants.md)
</dt> </dl>

 

