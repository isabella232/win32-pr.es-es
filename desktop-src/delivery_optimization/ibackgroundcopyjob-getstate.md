---
title: Método IBackgroundCopyJob GetState (Deliveryoptimization. h)
description: Recupera el estado del trabajo.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Método GetState
- Método GetState, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802438"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>IBackgroundCopyJob:: GetState (método)

Recupera el estado del trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobState* \[ enuncia\]
</dt> <dd>

Estado del trabajo. Por ejemplo, el estado refleja si el trabajo es un error, si se transfieren datos o si se suspende. Para obtener una lista de Estados de trabajo, consulte la enumeración [**BG_JOB_STATE**](bg-job-state-.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El estado del trabajo se recuperó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Si desea saber cuándo se produce un error en un trabajo o si ha transferido todos los archivos en el trabajo, puede usar este método para sondear el estado del trabajo o puede registrarse para recibir notificaciones cuando se produzcan eventos. Para más información sobre el registro para recibir notificaciones de eventos, consulte la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





