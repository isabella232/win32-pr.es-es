---
title: Método IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera un trabajo especificado de la cola de transferencia. Normalmente, la aplicación conserva el identificador del trabajo, por lo que posteriormente puede recuperar el trabajo de la cola.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Método GetJob
- Método GetJob, interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, método GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714595"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>IBackgroundCopyManager:: GetJob (método)

Recupera un trabajo especificado de la cola de transferencia. Normalmente, la aplicación conserva el identificador del trabajo, por lo que posteriormente puede recuperar el trabajo de la cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobID* \[ de\]
</dt> <dd>

Identifica el trabajo que se va a recuperar de la cola de transferencia. El método [**CreateJob**](ibackgroundcopymanager-createjob.md) devuelve el identificador del trabajo.

</dd> <dt>

*ppJob* \[ enuncia\]
</dt> <dd>

Un puntero de interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) al trabajo especificado por *JobID*. Cuando termine, libere *ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                                      | Descripción                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | El trabajo se recuperó correctamente de la cola de transferencia.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | No se encontró el trabajo en la cola.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | El usuario no tiene permiso para recuperar el trabajo.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





