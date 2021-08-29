---
title: Método GetType de IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera el tipo de transferencia que se realiza, como una descarga o carga de archivos.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType (método)
- Método GetType, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7697891e3ff98acd7440d52fe7be2799e4a551e45326c82a00d370e39fc4f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755255"
---
# <a name="ibackgroundcopyjobgettype-method"></a>IBackgroundCopyJob::GetType (método)

Recupera el tipo de transferencia que se realiza, como una descarga o carga de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobType* \[ out\]
</dt> <dd>

Tipo de transferencia que se realiza. Para obtener una lista de tipos de transferencia, vea la [**enumeración BG_JOB_TYPE**](bg-job-type.md) datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | El tipo de transferencia se recuperó correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Especifique el tipo de transferencia al crear el trabajo.

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

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





