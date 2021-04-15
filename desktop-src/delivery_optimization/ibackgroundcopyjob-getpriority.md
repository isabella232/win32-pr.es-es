---
title: Método IBackgroundCopyJob GetPriority ((Deliveryoptimization. h)
description: Recupera el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Método GetPriority (
- Método GetPriority (, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetPriority (
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695946"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a>IBackgroundCopyJob:: GetPriority ((método)

Recupera el nivel de prioridad del trabajo. El nivel de prioridad determina cuándo se procesa el trabajo en relación con otros trabajos de la cola de transferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPriority* \[ enuncia\]
</dt> <dd>

Prioridad del trabajo en relación con otros trabajos de la cola de transferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El nivel de prioridad se recuperó correctamente.<br/> |



 

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

[**IBackgroundCopyJob:: SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





