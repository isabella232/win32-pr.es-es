---
title: Enumeración BG_JOB_STATE (Deliveryoptimization. h)
description: La enumeración BG_JOB_STATE define valores constantes para los distintos Estados de un trabajo.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumeración BG_JOB_STATE
- Enumeración BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714550"
---
# <a name="bg_job_state-enumeration"></a>Enumeración BG_JOB_STATE

La enumeración **BG_JOB_STATE** define valores constantes para los distintos Estados de un trabajo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Especifica que el trabajo está en la cola y en espera de ejecutarse. Si un usuario cierra la sesión mientras su trabajo está transfiriendo, el trabajo pasa al estado en cola.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

No se admite.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Especifica que es la transferencia de datos para el trabajo.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Especifica que el trabajo se ha suspendido (en pausa). Para suspender un trabajo, llame al método [**IBackgroundCopyJob:: Suspend**](ibackgroundcopyjob-suspend.md) . El trabajo permanece suspendido hasta que se llama al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md)o [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Especifica que se ha producido un error irrecuperable (el servicio no puede transferir el archivo). Si se puede corregir el error, como un error de acceso denegado, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) una vez corregido el error. Sin embargo, si el error no se puede corregir, llame al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo o llame al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para aceptar la parte de un trabajo de descarga que se transfirió correctamente.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Especifica que se ha producido un error recuperable. Se reintentarán los trabajos en el estado de error transitorio en función de la configuración interna de reintento. El estado del trabajo cambia a **BG_JOB_STATE_ERROR** si el trabajo no puede realizar el progreso (vea [**IBackgroundCopyJob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Especifica que el trabajo se ha procesado correctamente. Debe llamar al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar la finalización del trabajo y hacer que los archivos estén disponibles para el cliente.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Especifica que se llamó al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que el trabajo se completó correctamente.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Especifica que se llamó al método [**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo (quitar el trabajo de la cola de transferencia).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





