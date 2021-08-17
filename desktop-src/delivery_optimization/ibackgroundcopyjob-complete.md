---
title: Método IBackgroundCopyJob Complete (Deliveryoptimization.h)
description: Finaliza el trabajo y guarda los archivos transferidos en el cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Método Complete
- Método completo, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72ace8890e724e529e96c5292a439042f13bc2bfad77e6d990a6dbb2fa18f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736232"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>IBackgroundCopyJob::Complete (Método)

Finaliza el trabajo y guarda los archivos transferidos en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT.** El método también puede devolver errores relacionados con el cambio de nombre de las copias temporales de los archivos transferidos a sus nombres dados.



| Código devuelto                                                                                          | Descripción                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>             | Todos los archivos transferidos correctamente.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | En el caso de las descargas, el estado del trabajo no se puede BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED. <br/> Para las cargas, el estado del trabajo debe ser BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Comentarios

Todos los archivos se han transferido correctamente si el estado del trabajo es **BG_JOB_STATE_TRANSFERRED**. Para comprobar el estado del trabajo, llame al [**método IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) También puede implementar la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para recibir una notificación cuando todos los archivos se hayan transferido al cliente.

DO conserva los trabajos que son inferiores a 30 días. Se quitarán todos los trabajos anteriores. DO no admite el directiva de grupo [JobInactivityTimeout.](https://www.bing.com/search?q=JobInactivityTimeout)

Para los trabajos de descarga, puede llamar al **método Complete** en cualquier momento durante el proceso de transferencia. sin embargo, solo se guardan los archivos que se transfirieron correctamente al cliente antes de llamar a este método. Por ejemplo, si llama al método **Complete** mientras DO procesa el tercero de cinco archivos, solo se guardan los dos primeros archivos. Para determinar qué archivos se han transferido, llame al método [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) y compare el miembro **BytesTransferred** con el miembro **BytesTotal** de la [**BG_FILE_PROGRESS**](bg-file-progress.md) estructura.

Para los trabajos de carga, puede llamar al **método Complete** solo cuando el estado del trabajo **es BG_JOB_STATE_TRANSFERRED**.

El propietario del archivo es el usuario que realizó la llamada. Por ejemplo, si un administrador completa el trabajo de otra persona, el administrador no es el propietario del trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
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

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





