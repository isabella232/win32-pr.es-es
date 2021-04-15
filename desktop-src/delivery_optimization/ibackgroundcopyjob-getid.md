---
title: Método GetId IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el identificador usado para identificar el trabajo en la cola.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (método)
- Método GetId, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695934"
---
# <a name="ibackgroundcopyjobgetid-method"></a>IBackgroundCopyJob:: GetId (método)

Recupera el identificador usado para identificar el trabajo en la cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobID* \[ enuncia\]
</dt> <dd>

GUID que identifica el trabajo en la cola de tareas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.

## <a name="remarks"></a>Observaciones

El servicio genera el identificador al [crear](ibackgroundcopymanager-createjob.md) el trabajo. Para usar el identificador con el fin de recuperar un puntero de la interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) para el trabajo, llame al método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .

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

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





