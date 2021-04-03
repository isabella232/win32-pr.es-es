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
# <a name="winbio_extended_engine_info-structure"></a>WINBIO \_ \_ estructura de información del motor extendido \_

Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**GenericEngineCapabilities**
</dt> <dd>

Las capacidades genéricas del componente del motor que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

El tipo de unidad biométrica para la que esta estructura contiene información sobre las capacidades y los requisitos de inscripción del adaptador de motor. Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información del motor extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .

</dd> <dt>

**Cuestión**
</dt> <dd>

Información sobre las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con las características faciales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con patrones de huellas digitales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

El número de buenos ejemplos necesarios para crear una nueva plantilla de huellas digitales.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

El número total de buenos ejemplos necesarios para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**Centro**
</dt> <dd>

El número de buenos ejemplos para el centro de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**Borde**
</dt> <dd>

El número de buenos ejemplos para el borde superior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**BottomEdge**
</dt> <dd>

El número de buenos ejemplos para el borde inferior de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**LeftEdge**
</dt> <dd>

El número de buenos ejemplos para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> <dt>

**RightEdge**
</dt> <dd>

El número de buenos ejemplos para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huellas digitales.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con los patrones de iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de motor para una unidad biométrica relacionada con los patrones de voz.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





