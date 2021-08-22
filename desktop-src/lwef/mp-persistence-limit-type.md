---
title: MP_PERSISTENCE_LIMIT_TYPE enumeración (MpClient.h)
description: Tipo de límite de persistencia.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE enumeración de características de entorno Windows heredado
- PMP_PERSISTENCE_LIMIT_TYPE puntero de enumeración Heredados Windows Environment Features
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a56d4962467abe0ad338af257aca2581e612c100468fbdf2853aa4d71290ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609005"
---
# <a name="mp_persistence_limit_type-enumeration"></a>Enumeración LIMIT TYPE de MP \_ PERSISTENCE \_ \_

Tipo de límite de persistencia.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**PERSISTENCIA \_ DE MP \_ DESCONOCIDA**
</dt> <dd>

Desconocido.

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**PERSISTENCIA \_ DE MP SIN \_ \_ LÍMITE**
</dt> <dd>

Ilimitado.

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**DURACIÓN \_ DE PERSISTENCIA DEL \_ MP**
</dt> <dd>

Duración.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**VERSIÓN \_ DE \_ VDM DE PERSISTENCIA DE \_ MP**
</dt> <dd>

Versión de VDM.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MARCA DE \_ TIEMPO DE PERSISTENCIA DE \_ MP**
</dt> <dd>

Timestamp.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**PERSISTENCIA \_ DE MP \_ FORZADA**
</dt> <dd>

Forzado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





