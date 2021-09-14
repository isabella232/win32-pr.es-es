---
title: MPDETECTION_STATE enumeración (MpClient.h)
description: Estado de la amenaza detectada actualmente.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeración de características heredadas Windows entorno
- PMPDETECTION_STATE puntero de enumeración Heredados Windows Environment Features
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252584"
---
# <a name="mpdetection_state-enumeration"></a>Enumeración MPDETECTION \_ STATE

Estado de la amenaza detectada actualmente.

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

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**ESTADO DE MPDETECTION \_ \_ DESCONOCIDO**
</dt> <dd>

En un estado de error.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**ESTADO DE \_ MPDETECTION \_ ACTIVO**
</dt> <dd>

Amenaza activa.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**ESTADO DE \_ MPDETECTION \_ FINALIZADO**
</dt> <dd>

Pendiente de 24 horas a un traslado a borrado.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**ACCIONES ADICIONALES DE \_ ESTADO DE MPDETECTION \_ \_**
</dt> <dd>

Se requieren acciones adicionales.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**ERROR EN EL ESTADO \_ DE MPDETECTION \_**
</dt> <dd>

Error de corrección no crítico.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**ERROR CRÍTICO EN \_ EL ESTADO DE MPDETECTION \_ \_**
</dt> <dd>

Error de corrección crítico.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**ESTADO DE MPDETECTION \_ \_ DESACTIVADO**
</dt> <dd>

La amenaza no aparece en la consulta de estado, solo en el historial.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





