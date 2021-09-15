---
title: Método IWMDRMLicenseBackupRestoreStatus GetStatus (Wmdrmsdk.h)
description: El método GetStatus recupera información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Formato multimedia de windows del método GetStatus
- Método GetStatus windows Media Format , interfaz IWMDRMLicenseBackupRestoreStatus
- IWMDRMLicenseBackupRestoreStatus de la interfaz windows Media Format , método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466481"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>IWMDRMLicenseBackupRestoreStatus::GetStatus (método)

El **método GetStatus** recupera información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStatus* \[ out\]
</dt> <dd>

Puntero a una [**estructura WM BACKUP RESTORE \_ \_ \_ STATUS**](wm-backup-restore-status.md) que recibe la información de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





