---
title: WINBIO_EXTENDED_ENGINE_INFO estructura (Winbio \_ types.h)
description: Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO estructura Windows API de marco biométrico
- PWINBIO_EXTENDED_ENGINE_INFO puntero de estructura Windows Biometric Framework API
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
ms.openlocfilehash: df59b10400729150a13f2a8a5476c46507867777f71641a01ea0c08e064b4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910521"
---
# <a name="winbio_extended_engine_info-structure"></a>Estructura DE \_ INFORMACIÓN DEL MOTOR EXTENDIDO DE \_ \_ WINBIO

Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica.

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

Funcionalidades genéricas del componente del motor que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

Tipo de unidad biométrica para la que esta estructura contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor. Por ejemplo, si el valor del miembro **Factor** es **WINBIO \_ TYPE \_ FINGERPRINT**, la estructura DE INFORMACIÓN DEL MOTOR EXTENDIDO DE **WINBIO \_ \_ \_** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **Specifc.Fingerprint.**

</dd> <dt>

**Específico**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**Características faciales**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica relacionada con las características faciales.

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

Información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica relacionada con los patrones de huella digital.

<dl> <dt>

**Capabilities**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

Número de buenos ejemplos necesarios para crear una nueva plantilla de huella digital.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Número total de ejemplos buenos necesarios para crear una nueva plantilla de huella digital.

</dd> <dt>

**Centro**
</dt> <dd>

Número de buenos ejemplos para el centro de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**Topedge**
</dt> <dd>

Número de buenos ejemplos para el borde superior de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Número de buenos ejemplos para el borde inferior de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Número de buenos ejemplos para el borde izquierdo de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> <dt>

**RightEdge**
</dt> <dd>

Número de buenos ejemplos para el borde derecho de la huella digital necesaria para crear una nueva plantilla de huella digital.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica relacionada con los patrones de iris.

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

Información sobre las funcionalidades y los requisitos de inscripción del adaptador del motor para una unidad biométrica relacionada con los patrones de voz.

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
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes DE FUNCIONALIDAD DE WINBIO \_**](winbio-capability-constants.md)
</dt> <dt>

[**Constantes DE \_ TIPO BIOMETRIC DE WINBIO \_**](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





