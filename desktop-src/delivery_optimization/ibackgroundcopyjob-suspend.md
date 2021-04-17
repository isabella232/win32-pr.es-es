---
title: Método Suspend de IBackgroundCopyJob (Deliveryoptimization. h)
description: Suspende un trabajo. Los nuevos trabajos, los trabajos que tienen errores y los trabajos que han terminado de transferir archivos se suspenden automáticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Método Suspend
- Método Suspend, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422311"
---
# <a name="ibackgroundcopyjobsuspend-method"></a>IBackgroundCopyJob:: Suspend (método)

Suspende un trabajo. Los nuevos trabajos, los trabajos que tienen errores y los trabajos que han terminado de transferir archivos se suspenden automáticamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Suspend();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                                          | Descripción                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | El trabajo se suspendió correctamente.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | El estado del trabajo no puede ser BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

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

[**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





