---
title: Estructura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (Winbio \_ Adapter. h)
description: Contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- Plataforma de biometría de Windows API de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Structure
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS de puntero de estructura Plataforma de biometría de Windows API
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
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489557"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>WINBIO \_ \_ estructura de parámetros de inscripción extendida \_

La estructura **WINBIO \_ Extended \_ ENROLLMENT \_ Parameters** contiene información adicional que un adaptador de motor necesita para crear una plantilla de inscripción.

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

Tamaño (en bytes) de la estructura **WINBIO \_ Extended \_ ENROLLMENT \_ Parameters** .

</dd> <dt>

**Subfactor**
</dt> <dd>

Uno de los [**valores \_ constantes del \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que proporciona información adicional sobre la inscripción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El Plataforma de biometría de Windows pasa esta estructura al método [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante una operación de inscripción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                                     |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Adapter. h (incluir Winbio \_ Adapter. h)</dt> </dl> |



 

 





