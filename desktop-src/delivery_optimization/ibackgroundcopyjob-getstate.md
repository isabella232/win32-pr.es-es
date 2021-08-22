---
title: Método IBackgroundCopyJob GetState (Deliveryoptimization.h)
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
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755305"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>IBackgroundCopyJob::GetState (método)

Recupera el estado del trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobState* \[ out\]
</dt> <dd>

Estado del trabajo. Por ejemplo, el estado refleja si el trabajo está en error, transfiriendo datos o suspendido. Para obtener una lista de estados de trabajo, vea la [**enumeración BG_JOB_STATE**](bg-job-state-.md) trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | El estado del trabajo se recuperó correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Si desea saber cuándo se produce un error en un trabajo o si ha transferido todos los archivos del trabajo, puede usar este método para sondear el estado del trabajo o puede registrarse para recibir notificaciones cuando se produzcan eventos. Para más información sobre cómo registrarse para recibir notificaciones de eventos, consulte la [**interfaz IBackgroundCopyCallback.**](ibackgroundcopycallback.md)

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





