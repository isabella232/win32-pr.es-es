---
title: MPEXECUTION_STATUS enumeración (MpClient.h)
description: Posible estado de ejecución de amenazas.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS enumeración de características heredadas Windows entorno
- PMPEXECUTION_STATUS puntero de enumeración Heredados Windows Environment Features
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
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943915"
---
# <a name="mpexecution_status-enumeration"></a>Enumeración MPEXECUTION \_ STATUS

Posible estado de ejecución de amenazas.

## <a name="syntax"></a>Syntax


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

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**ESTADO DE \_ EJECUCIÓN \_ DEL MP \_ DESCONOCIDO**
</dt> <dd>

No se conoce el estado de ejecución.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**ESTADO DE \_ EJECUCIÓN \_ DEL MP \_ BLOQUEADO**
</dt> <dd>

Se ha bloqueado la ejecución mediante minifiltro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**ESTADO DE \_ EJECUCIÓN \_ DE MP \_ PERMITIDO**
</dt> <dd>

Se permite ejecutar mediante minifiltro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**ESTADO \_ DE EJECUCIÓN DEL MP EN \_ \_ EJECUCIÓN**
</dt> <dd>

Se está ejecutando la amenaza.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**ESTADO \_ DE EJECUCIÓN DEL MP NO EN \_ \_ \_ EJECUCIÓN**
</dt> <dd>

La amenaza no se está ejecutando y solo está disponible en el motor durante la corrección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





