---
title: Enumeración MPEXECUTION_STATUS (MpClient. h)
description: Posible estado de ejecución de la amenaza.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS enumeración características de entorno heredado de Windows
- PMPEXECUTION_STATUS el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905142"
---
# <a name="mpexecution_status-enumeration"></a>\_Enumeración de estado de MPEXECUTION

Posible estado de ejecución de la amenaza.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**Estado de ejecución del módulo de administración \_ \_ \_ desconocido**
</dt> <dd>

No se conoce el estado de ejecución.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**Estado de ejecución del módulo de administración \_ \_ \_ bloqueado**
</dt> <dd>

No se ha bloqueado la ejecución mediante el filtro Mini.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**Estado de ejecución de MP \_ \_ \_ permitido**
</dt> <dd>

Se permite que se ejecute mediante un filtro Mini.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**Estado de ejecución del módulo de administración en \_ \_ \_ ejecución**
</dt> <dd>

Se está ejecutando una amenaza.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**Estado de ejecución del módulo de administración \_ \_ no en \_ \_ ejecución**
</dt> <dd>

La amenaza no se está ejecutando y solo está disponible en el motor durante la corrección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





