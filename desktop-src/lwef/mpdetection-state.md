---
title: Enumeración MPDETECTION_STATE (MpClient. h)
description: El estado de la amenaza detectada actualmente.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeración características de entorno heredado de Windows
- PMPDETECTION_STATE el puntero de enumeración características de entorno heredado de Windows
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
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490006"
---
# <a name="mpdetection_state-enumeration"></a>\_Enumeración de estado de MPDETECTION

El estado de la amenaza detectada actualmente.

## <a name="syntax"></a>Sintaxis


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

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Estado de MPDETECTION \_ \_ desconocido**
</dt> <dd>

En un estado de error.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**Estado de MPDETECTION \_ \_ activo**
</dt> <dd>

Amenaza activa.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**Estado de MPDETECTION \_ \_ finalizado**
</dt> <dd>

Pendiente 24 horas hasta que se desactive el movimiento.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ acciones adicionales de estado de MPDETECTION \_**
</dt> <dd>

Acciones adicionales necesarias.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_error de estado de MPDETECTION \_**
</dt> <dd>

Error de corrección no crítico.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**Estado de MPDETECTION de \_ \_ \_ error crítico**
</dt> <dd>

Error crítico en la corrección.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**Estado de MPDETECTION \_ \_ desactivado**
</dt> <dd>

La amenaza no se muestra en la consulta de estado, solo en el historial.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





