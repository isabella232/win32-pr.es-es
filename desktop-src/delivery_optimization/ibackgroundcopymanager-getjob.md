---
title: Método GetJob de IBackgroundCopyManager (Deliveryoptimization.h)
description: Recupera un trabajo especificado de la cola de transferencia. Normalmente, la aplicación conserva el identificador del trabajo, por lo que más adelante puede recuperar el trabajo de la cola.
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
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542293"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>IBackgroundCopyManager::GetJob (método)

Recupera un trabajo especificado de la cola de transferencia. Normalmente, la aplicación conserva el identificador del trabajo, por lo que más adelante puede recuperar el trabajo de la cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*JobID* \[ En\]
</dt> <dd>

Identifica el trabajo que se recupera de la cola de transferencia. El [**método CreateJob**](ibackgroundcopymanager-createjob.md) devuelve el identificador del trabajo.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Puntero [**de interfaz IBackgroundCopyJob**](ibackgroundcopyjob-.md) al trabajo especificado por *JobID.* Cuando haya terminado, libere *ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                                      | Descripción                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl>         | El trabajo se recuperó correctamente de la cola de transferencia.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | El trabajo no se encontró en la cola.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | El usuario no tiene permiso para recuperar el trabajo.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





