---
title: BG_JOB_STATE enumeración (Deliveryoptimization.h)
description: La BG_JOB_STATE enumeración define valores constantes para los distintos estados de un trabajo.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- BG_JOB_STATE enumeración
- BG_JOB_STATE enumeración
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
ms.openlocfilehash: 4f83f2b9ed799855b2ee1e9675a22cc1d2751583
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520464"
---
# <a name="bg_job_state-enumeration"></a>BG_JOB_STATE enumeración

La **BG_JOB_STATE** enumeración define valores constantes para los distintos estados de un trabajo.

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

Especifica que el trabajo está en la cola y en espera de ejecutarse. Si un usuario cierra la sesión mientras se transfiere su trabajo, el trabajo pasa al estado en cola.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Especifica que Optimización de distribución está transfiriendo datos para el trabajo.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Especifica que el trabajo está suspendido (en pausa). Para suspender un trabajo, llame al [**método IBackgroundCopyJob::Suspend.**](ibackgroundcopyjob-suspend.md) El trabajo permanece suspendido hasta que llame al método [**IBackgroundCopyJob::Resume,**](ibackgroundcopyjob-resume.md) [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)o [**IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Especifica que se ha producido un error irrecuperable (el servicio no puede transferir el archivo). Si el error, como un error de acceso denegado, se puede corregir, llame al método [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) una vez corregido el error. Sin embargo, si el error no se puede corregir, llame al método [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo o llame al método [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) para aceptar la parte de un trabajo de descarga que se ha transferido correctamente.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Especifica que se ha producido un error recuperable. Optimización de distribución los trabajos en estado de error transitorio en función de la configuración de reintento interno. El estado del trabajo cambia a **BG_JOB_STATE_ERROR** si el trabajo no puede avanzar (vea [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Especifica que el trabajo se procesó correctamente. Debe llamar al método [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) para confirmar la finalización del trabajo y para que los archivos estén disponibles para el cliente.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Especifica que llamó al método [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) para confirmar que el trabajo se completó correctamente.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Especifica que llamó al método [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) para cancelar el trabajo (quite el trabajo de la cola de transferencia).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





