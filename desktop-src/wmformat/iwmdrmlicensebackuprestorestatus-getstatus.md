---
title: Método GetStatus de IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: El método GetStatus recupera información de estado detallada sobre una operación de copia de seguridad o restauración de una licencia.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Método GetStatus formato de Windows Media
- Método GetStatus formato de Windows Media, interfaz IWMDRMLicenseBackupRestoreStatus
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media, método GetStatus
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709170"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>IWMDRMLicenseBackupRestoreStatus:: GetStatus (método)

El método **getStatus** recupera información de estado detallada sobre una operación de copia de seguridad o restauración de una licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStatus* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [**Estado de restauración de copia de seguridad de WM \_ \_ \_**](wm-backup-restore-status.md) que recibe la información de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





