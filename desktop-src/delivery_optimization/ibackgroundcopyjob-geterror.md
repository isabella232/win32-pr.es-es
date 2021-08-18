---
title: Método IBackgroundCopyJob GetError (Deliveryoptimization.h)
description: Recupera la interfaz de error después de que se produzca un error.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Método GetError
- Método GetError, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755515"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>IBackgroundCopyJob::GetError (método)

Recupera la interfaz de error después de que se produzca un error.

Optimización de distribución (DO) genera un objeto de error cuando el estado del trabajo es BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. El servicio no crea un objeto de error cuando se produce un error en una llamada a un método de interfaz **IBackgroundCopyXXXX.** El objeto de error está disponible hasta que DO comienza a transferir datos (el estado del trabajo cambia a BG_JOB_STATE_TRANSFERRING) para el trabajo o hasta que se cierra la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppError* \[ out\]
</dt> <dd>

Interfaz de error que proporciona el código de error, una descripción del error y el contexto en el que se produjo el error. Este parámetro también identifica el archivo que se transfiere en el momento en que se produjo el error. Libere *ppError* cuando haya terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                                           | Descripción                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>                              | Generó correctamente el objeto de error.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | La interfaz de error solo está disponible después de que se produzca un error (BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR) y antes de que DO comience a transferir datos (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Comentarios

El trabajo se coloca en un estado de error en caso de errores irreales. Use una de las siguientes opciones para determinar si el trabajo está en error:

-   Para sondear el estado del trabajo, llame al [**método IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) El trabajo está en error si el estado es BG_JOB_STATE_ERROR.
-   Para recibir una notificación cuando se produce un error, implemente la [**interfaz IBackgroundCopyCallback**](ibackgroundcopycallback.md) (en concreto, [**el método JobError).**](https://www.bing.com/search?q=**JobError**) A continuación, llame al método [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para registrar la devolución de llamada y el método [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para establecer la BG_NOTIFY_JOB_ERROR llamada.

La [**interfaz IBackgroundCopyError contiene**](ibackgroundcopyerror.md) información que se usa para determinar la causa del error y si el proceso de transferencia puede continuar. Después de determinar la causa del error, realice una de las siguientes opciones:

-   Para cancelar el trabajo, llame al [**método IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Para guardar los archivos transferidos correctamente antes de que se produjese el error, llame al [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md)
-   Para finalizar el procesamiento del trabajo, corrija el problema y, a continuación, llame al [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





