---
title: MPDETECTION_STATE enumeración (MpClient.h)
description: Estado de la amenaza detectada actualmente.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeración heredada de Windows environment
- PMPDETECTION_STATE puntero de enumeración heredado Windows environment
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883522"
---
# <a name="mpdetection_state-enumeration"></a>Enumeración MPDETECTION \_ STATE

Estado de la amenaza detectada actualmente.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**ESTADO DE MPDETECTION \_ \_ DESCONOCIDO**
</dt> <dd>

En un estado de error.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**ESTADO DE MPDETECTION \_ \_ ACTIVO**
</dt> <dd>

Amenaza activa.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**ESTADO DE MPDETECTION \_ \_ FINALIZADO**
</dt> <dd>

Pendiente de 24 horas a un traslado a borrado.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**ACCIONES ADICIONALES DE \_ ESTADO DE \_ MPDETECTION \_**
</dt> <dd>

Se requieren acciones adicionales.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**ERROR DE ESTADO \_ DE \_ MPDETECTION**
</dt> <dd>

Error de corrección no crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**ERROR CRÍTICO EN \_ EL ESTADO DE \_ MPDETECTION \_**
</dt> <dd>

Error de corrección crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**ESTADO DE MPDETECTION \_ \_ BORRADO**
</dt> <dd>

La amenaza no aparece en la consulta de estado, solo en el historial.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





