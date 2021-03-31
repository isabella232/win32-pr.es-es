---
title: Estructura de WINBIO_EXTENDED_STORAGE_INFO (Winbio \_ Types. h)
description: Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_STORAGE_INFO Structure
- PWINBIO_EXTENDED_STORAGE_INFO de puntero de estructura Plataforma de biometría de Windows API
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996037"
---
# <a name="winbio_extended_storage_info-structure"></a>WINBIO \_ \_ estructura de información de almacenamiento extendido \_

Contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica.

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



## <a name="members"></a>Miembros

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

Las capacidades genéricas del componente de almacenamiento que está conectado a una unidad biométrica específica.

</dd> <dt>

**Factor**
</dt> <dd>

El tipo de unidad biométrica para la que esta estructura contiene información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento. Por ejemplo, si el valor del miembro **factor** es **WINBIO \_ Type \_ FINGERPRINT**, la estructura de **\_ \_ \_ información de almacenamiento extendido WINBIO** se aplica a un lector de huellas digitales y contiene la información pertinente en la estructura **específico. FINGERPRINT** .

</dd> <dt>

**Cuestión**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con un factor biométrico específico.

<dl> <dt>

**Null**
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con las características faciales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Las capacidades de reconocimiento facial del componente de almacenamiento que está conectado a una unidad biométrica específica.

</dd> </dl> </dd> <dt>

**Huella digital**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con patrones de huellas digitales.

<dl> <dt>

**Capabilities**
</dt> <dd>

Las funcionalidades de reconocimiento de huellas digitales del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Las capacidades de reconocimiento de iris del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Información acerca de las capacidades y los requisitos de inscripción del adaptador de almacenamiento para una unidad biométrica relacionada con los patrones de voz.

<dl> <dt>

**Capabilities**
</dt> <dd>

Las capacidades de reconocimiento de voz del componente de almacenamiento que está conectado a una unidad biométrica específica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WINBIO \_ constantes de \_ tipo biométrico**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes de capacidad de WINBIO \_**](winbio-capability-constants.md)
</dt> </dl>

 

 





