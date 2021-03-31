---
title: Método GetType IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el tipo de transferencia que se realiza, por ejemplo, una descarga o carga de archivos.
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
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079017"
---
# <a name="ibackgroundcopyjobgettype-method"></a>IBackgroundCopyJob:: GetType (método)

Recupera el tipo de transferencia que se realiza, por ejemplo, una descarga o carga de archivos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobType* \[ enuncia\]
</dt> <dd>

Tipo de transferencia que se va a realizar. Para obtener una lista de tipos de transferencia, vea la enumeración [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El tipo de transferencia se recuperó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Especifique el tipo de transferencia al crear el trabajo.

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

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





