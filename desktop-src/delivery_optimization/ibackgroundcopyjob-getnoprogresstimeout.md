---
title: Método IBackgroundCopyJob GetNoProgressTimeout (Deliveryoptimization.h)
description: Recupera el período de tiempo durante el que el servicio intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Método GetNoProgressTimeout
- Método GetNoProgressTimeout, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a80e4d89c510885372a92d2c373d5fb73e9bd8375dd712ec07c5f98be51f791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755435"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>IBackgroundCopyJob::GetNoProgressTimeout (método)

Recupera el período de tiempo durante el que el servicio intenta transferir el archivo después de que se produzca una condición de error transitorio. Si hay progreso, se restablece el temporizador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRetryPeriod* \[ En\]
</dt> <dd>

Tiempo, en segundos, durante el que el servicio intenta transferir el archivo después de que se produzca un error transitorio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | El tiempo de espera se recuperó correctamente.<br/> |



 

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

[**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





