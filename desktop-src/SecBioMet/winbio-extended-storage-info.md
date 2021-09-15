---
title: WINBIO_EXTENDED_STORAGE_INFO estructura (Winbio \_ types.h)
description: Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO estructura Windows Api de marco biométrico
- PWINBIO_EXTENDED_STORAGE_INFO puntero de estructura Windows BIOMETRIC Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476534"
---
# <a name="winbio_extended_storage_info-structure"></a>Estructura DE \_ INFORMACIÓN DE ALMACENAMIENTO EXTENDIDO \_ \_ DE WINBIO

Contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

Funcionalidades genéricas del componente de almacenamiento que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

Tipo de unidad biométrica para la que esta estructura contiene información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento. Por ejemplo, si el valor del miembro **Factor** es **WINBIO \_ TYPE \_ FINGERPRINT**, la estructura INFO de ALMACENAMIENTO EXTENDIDO de **WINBIO \_ \_ \_** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **Specifc.Fingerprint.**

</dd> <dt>

**Específico**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**Características faciales**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con las características faciales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funcionalidades de reconocimiento facial del componente de almacenamiento que está conectado a una unidad biométrica específica.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de huella digital.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funcionalidades de reconocimiento de huellas digitales del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funcionalidades de reconocimiento de iris del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información sobre las funcionalidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de voz.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funcionalidades de reconocimiento de voz del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluya Winbio.h para aplicaciones cliente o Adaptadores \_ de Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes DE \_ TIPO BIOMETRIC DE WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes DE CAPACIDAD DE WINBIO \_**](winbio-capability-constants.md)
</dt> </dl>

 

 





