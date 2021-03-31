---
title: Método de reanudación de IBackgroundCopyJob (Deliveryoptimization. h)
description: Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Método Resume
- Método resume, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método resume
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
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150074"
---
# <a name="ibackgroundcopyjobresume-method"></a>IBackgroundCopyJob:: resume (método)

Activa un nuevo trabajo o reinicia un trabajo que se ha suspendido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                                          | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | El trabajo se ha reiniciado correctamente.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | No hay archivos para transferir.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Observaciones

Al crear un trabajo, el trabajo se suspende inicialmente. La llamada a **resume** mueve el trabajo al estado transfiriendo. Tenga en cuenta que el trabajo debe contener uno o más archivos antes de llamar a este método.

Si un trabajo se encuentra en el estado BG_JOB_STATE_TRANSIENT_ERROR o BG_JOB_STATE_ERROR, llame al método **resume** para reiniciar el trabajo después de corregir el error.

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

[**IBackgroundCopyJob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





