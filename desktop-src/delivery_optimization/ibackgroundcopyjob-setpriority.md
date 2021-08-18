---
title: Método SetPriority de IBackgroundCopyJob (Deliveryoptimization.h)
description: Especifica el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Método SetPriority
- Método SetPriority, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542876"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>IBackgroundCopyJob::SetPriority (método)

Especifica el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ En\]
</dt> <dd>

Especifica el nivel de prioridad del trabajo con respecto a otros trabajos de la cola de transferencia. El valor predeterminado es BG_JOB_PRIORITY_NORMAL. Para obtener una lista de los niveles de prioridad, vea la [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeración .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | La prioridad del trabajo se estableció correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





