---
title: Método IBackgroundCopyJob Resume (Deliveryoptimization.h)
description: Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Método Resume
- Método Resume, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa4bd9a98626b7f26fc4ac9968d27d54604b5db56539eb383bb8aff696b2a561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543011"
---
# <a name="ibackgroundcopyjobresume-method"></a>IBackgroundCopyJob::Resume (método)

Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                          | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>             | El trabajo se reinició correctamente.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | No hay archivos para transferir.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | El estado del trabajo no se puede BG_JOB_STATE_CANCELLED ni BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Observaciones

Al crear un trabajo, el trabajo se suspende inicialmente. Al llamar **a Resume,** el trabajo pasa al estado Transferring (Transfiriendo). Tenga en cuenta que el trabajo debe contener uno o varios archivos antes de llamar a este método.

Si un trabajo que se encuentra en BG_JOB_STATE_TRANSIENT_ERROR estado BG_JOB_STATE_ERROR, llame al método **Resume** para reiniciar el trabajo después de corregir el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                           |
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

[**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





