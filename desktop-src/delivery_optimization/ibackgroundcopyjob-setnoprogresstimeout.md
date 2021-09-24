---
title: Método IBackgroundCopyJob SetNoProgressTimeout (Deliveryoptimization.h)
description: Establece el período de tiempo durante el Optimización de distribución intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Método SetNoProgressTimeout
- Método SetNoProgressTimeout, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e2bc77cf8a5c560cdc8a7bc7dd819c1dbe7a286
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520082"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>IBackgroundCopyJob::SetNoProgressTimeout (método)

Establece el período de tiempo durante el Optimización de distribución intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RetryPeriod* \[ En\]
</dt> <dd>

Tiempo, en segundos, que Optimización de distribución intenta transferir el archivo después de que no se haya realizado ningún progreso. El período de reintento predeterminado para el trabajo de prioridad alta es de 3600 segundos (1 hora) y para el trabajo de prioridad baja es de 86 400 segundos (24 horas).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                          | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>             | Período de reintento establecido correctamente.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | El estado del trabajo no se puede BG_JOB_STATE_CANCELLED ni BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentarios

Si Optimización de distribución no progresa durante el período de reintento, mueve el estado del trabajo de BG_JOB_STATE_TRANSIENT_ERROR a BG_JOB_STATE_ERROR. Si solicita una notificación de error, Optimización de distribución llamada a la [**devolución de llamada JobError.**](https://www.bing.com/search?q=**JobError**)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





