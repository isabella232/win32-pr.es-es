---
title: Método IBackgroundCopyJob GetNotifyInterface (Deliveryoptimization.h)
description: Recupera el puntero de interfaz a la implementación de la interfaz IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Método GetNotifyInterface
- Método GetNotifyInterface, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970096"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>IBackgroundCopyJob::GetNotifyInterface (método)

Recupera el puntero de interfaz a la implementación de la [**interfaz IBackgroundCopyCallback.**](ibackgroundcopycallback.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppNotifyInterface* \[ out\]
</dt> <dd>

Puntero de interfaz a la implementación de la [**interfaz IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Cuando haya terminado, libere *ppNotifyInterface*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | El puntero de interfaz de notificación se recuperó correctamente.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





