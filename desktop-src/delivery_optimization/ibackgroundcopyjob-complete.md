---
title: Método complete IBackgroundCopyJob (Deliveryoptimization. h)
description: Finaliza el trabajo y guarda los archivos transferidos en el cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete (método)
- Método complete, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método complete
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
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150278"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>IBackgroundCopyJob:: Complete (método)

Finaliza el trabajo y guarda los archivos transferidos en el cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** . El método también puede devolver errores relacionados con el cambio de nombre de las copias temporales de los archivos transferidos a sus nombres determinados.



| Código devuelto                                                                                          | Descripción                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Todos los archivos se transfirieron correctamente.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | En el caso de las descargas, el estado del trabajo no puede ser BG_JOB_STATE_CANCELLED ni BG_JOB_STATE_ACKNOWLEDGED. <br/> En el caso de las cargas, el estado del trabajo debe ser BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Observaciones

Todos los archivos se transfirieron correctamente si el estado del trabajo es **BG_JOB_STATE_TRANSFERRED**. Para comprobar el estado del trabajo, llame al método [**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md) . También puede implementar la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para recibir notificaciones cuando todos los archivos se hayan transferido al cliente.

Conserva los trabajos que solo son inferiores a 30 días. Se quitarán todos los trabajos anteriores. No admite el directiva de grupo [valor jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) .

En el caso de los trabajos de descarga, puede llamar al método **Complete** en cualquier momento durante el proceso de transferencia; sin embargo, solo se guardan los archivos que se transfirieron correctamente al cliente antes de llamar a este método. Por ejemplo, si llama al método **Complete** mientras está procesando el tercer archivo, solo se guardan los dos primeros archivos. Para determinar qué archivos se han transferido, llame al método [**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) y compare el miembro **BytesTransferred** con el miembro **bytesTotal** de la estructura [**BG_FILE_PROGRESS**](bg-file-progress.md) .

En el caso de los trabajos de carga, puede llamar al método **Complete** solo cuando el estado del trabajo es **BG_JOB_STATE_TRANSFERRED**.

El propietario del archivo es el usuario que realizó la llamada. Por ejemplo, si un administrador completa el trabajo de otro usuario, el administrador no es el propietario del trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob:: CANCEL**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





