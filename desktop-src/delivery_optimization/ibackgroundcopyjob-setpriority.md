---
title: Método SetPriority IBackgroundCopyJob (Deliveryoptimization. h)
description: Especifica el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority (método)
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
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802437"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>IBackgroundCopyJob:: SetPriority (método)

Especifica el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Prioridad* \[ de de\]
</dt> <dd>

Especifica el nivel de prioridad del trabajo en relación con otros trabajos de la cola de transferencia. El valor predeterminado es BG_JOB_PRIORITY_NORMAL. Para obtener una lista de los niveles de prioridad, vea la enumeración [**BG_JOB_PRIORITY**](bg-job-priority-.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | La prioridad del trabajo se estableció correctamente.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetPriority (**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





