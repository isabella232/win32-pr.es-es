---
title: Método CANCEL IBackgroundCopyJob (Deliveryoptimization. h)
description: Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y del servidor (cargas).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método CANCEL, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método CANCEL
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905186"
---
# <a name="ibackgroundcopyjobcancel-method"></a>IBackgroundCopyJob:: CANCEL (método)

Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y del servidor (cargas).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                                          | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | El trabajo se canceló correctamente.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | No se puede cancelar un trabajo cuyo estado sea BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Observaciones

Puede cancelar un trabajo en cualquier momento; sin embargo, el trabajo no se puede recuperar una vez cancelado.

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

[**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**IBackgroundCopyJob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





