---
title: Método Cancel de IBackgroundCopyJob (Deliveryoptimization.h)
description: Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y el servidor (cargas).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método Cancel, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Cancel
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
ms.openlocfilehash: c30fa0d7dcc4aa6137fbfef8d40a91d4839bc59d624c8ba2c942fb6c2041fccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635855"
---
# <a name="ibackgroundcopyjobcancel-method"></a>IBackgroundCopyJob::Cancel (método)

Elimina el trabajo de la cola de transferencia y quita los archivos temporales relacionados del cliente (descargas) y el servidor (cargas).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                          | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>             | El trabajo se canceló correctamente.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | No se puede cancelar un trabajo cuyo estado BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Comentarios

Puede cancelar un trabajo en cualquier momento; sin embargo, el trabajo no se puede recuperar después de que se cancele.

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

[**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





