---
title: Método GetId de IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera el identificador utilizado para identificar el trabajo en la cola.
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
ms.openlocfilehash: 6987650f3a1339086241b444429857923eb77f76
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520236"
---
# <a name="ibackgroundcopyjobgetid-method"></a>IBackgroundCopyJob::GetId (método)

Recupera el identificador utilizado para identificar el trabajo en la cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pJobID* \[ out\]
</dt> <dd>

GUID que identifica el trabajo dentro de la Optimización de distribución de trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** correcto o uno de los valores **HRESULT COM** estándar en caso de error.

## <a name="remarks"></a>Comentarios

El servicio genera el identificador al [crear](ibackgroundcopymanager-createjob.md) el trabajo. Para usar el identificador para recuperar un puntero de interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) para el trabajo, llame al método [**IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

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

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





