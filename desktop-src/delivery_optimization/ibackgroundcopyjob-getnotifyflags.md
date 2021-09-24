---
title: Método IBackgroundCopyJob GetNotifyFlags (Deliveryoptimization.h)
description: Recupera las marcas de notificación de eventos para el trabajo.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Método GetNotifyFlags
- Método GetNotifyFlags, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1dac1928a7f6811ccfa20902d50a4b1a47f5d123
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520710"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a>IBackgroundCopyJob::GetNotifyFlags (método)

Recupera las marcas de notificación de eventos para el trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNotifyFlags* \[ out\]
</dt> <dd>

Identifica los eventos que recibe la aplicación. En la tabla siguiente se enumeran los valores de la marca de notificación de eventos.



| Value                                                                                                                                                                                                  | Significado                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> </dl>    | Se han transferido todos los archivos del trabajo.<br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> </dl>                      | Se ha producido un error.<br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> </dl>                             | La notificación de eventos está deshabilitada. Si se establece, Optimización de distribución omite las otras marcas.<br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> </dl> | El trabajo se ha modificado.<br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Las marcas de notificación de eventos se recuperaron correctamente.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





