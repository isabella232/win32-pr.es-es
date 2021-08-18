---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS estructura (Winbio \_ adapter.h)
description: Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS estructura Windows API de Marco biométrico
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS puntero de estructura Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55173b5badfb8764cfc9c681f4ed92e2f0d1c50e5db09075185af9e5db2e6433
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910494"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>Estructura DE PARÁMETROS \_ DE \_ INSCRIPCIÓN EXTENDIDA \_ DE WINBIO

La **estructura DE PARÁMETROS DE INSCRIPCIÓN EXTENDIDA \_ \_ \_ DE WINBIO** contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tamaño (en bytes) de la **estructura DE PARÁMETROS DE INSCRIPCIÓN EXTENDIDA \_ \_ \_ DE WINBIO.**

</dd> <dt>

**SubFactor**
</dt> <dd>

Uno de los [**valores de constantes \_ \_ SUBTYPE BIOMETRIC de WINBIO**](winbio-biometric-subtype-constants.md) que proporciona información adicional sobre la inscripción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El Windows Biometric Framework pasa esta estructura al método [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante una operación de inscripción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ adapter.h (incluir Winbio \_ adapter.h)</dt> </dl> |



 

 





