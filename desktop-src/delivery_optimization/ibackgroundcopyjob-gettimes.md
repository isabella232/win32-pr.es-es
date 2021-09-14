---
title: Método IBackgroundCopyJob GetTimes (Deliveryoptimization.h)
description: Recupera marcas de tiempo relacionadas con el trabajo, como la hora en que se creó o modificó por última vez el trabajo.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Método GetTimes
- Método GetTimes, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetTimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072980"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>IBackgroundCopyJob::GetTimes (método)

Recupera marcas de tiempo relacionadas con el trabajo, como la hora en que se creó o modificó por última vez el trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimes* \[ out\]
</dt> <dd>

Contiene marcas de tiempo relacionadas con el trabajo. Para obtener las marcas de tiempo disponibles, consulte [**la BG_JOB_TIMES**](bg-job-times.md) datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Las marcas de tiempo se recuperaron correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





