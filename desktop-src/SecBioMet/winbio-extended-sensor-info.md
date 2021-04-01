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
# <a name="winbio_extended_sensor_info-structure"></a>WINBIO \_ \_ estructura de información del sensor extendido \_

Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica.

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

Las capacidades genéricas del componente de sensor que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

El tipo de unidad biométrica para la que esta estructura contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor. Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información del sensor extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .

</dd> <dt>

**Cuestión**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con las características faciales.

<dl> <dt>

**Tramas**
</dt> <dd>

Tamaño del fotograma de la cámara, indicado como una longitud y un ancho en píxeles por los miembros **derecho** e **inferior** de la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . El punto (0,0) representa la esquina superior izquierda del marco.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Desplazamiento del fotograma de la cámara para la superficie de la cámara de vídeo, en píxeles. Un valor de (0,0) indica que el fotograma de la cámara para la superficie y la cámara de vídeo se superponen por completo.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientación preferida para la cámara.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con patrones de huellas digitales.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de iris.

<dl> <dt>

**Tramas**
</dt> <dd>

Tamaño del fotograma de la cámara, indicado como una longitud y un ancho en píxeles por los miembros **derecho** e **inferior** de la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . El punto (0,0) representa la esquina superior izquierda del marco.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Desplazamiento del fotograma de la cámara para el iris de la cámara de vídeo, en píxeles. Un valor de (0,0) indica que el fotograma de la cámara del iris y la cámara de vídeo se superponen por completo.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientación preferida para la cámara.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de sensor para una unidad biométrica relacionada con los patrones de voz.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes de capacidad de WINBIO \_**](winbio-capability-constants.md)
</dt> <dt>

[**WINBIO \_ constantes de \_ tipo biométrico**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes de orientación de WINBIO \_**](winbio-orientation-constants.md)
</dt> </dl>

 

