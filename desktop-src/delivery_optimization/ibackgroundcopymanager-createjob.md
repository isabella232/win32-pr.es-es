---
title: Método IBackgroundCopyManager::CreateJob (Deliveryoptimization.h)
description: Crea un trabajo.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Método CreateJob
- Método CreateJob, interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, método CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165b0a74f71ee5267fb3bd300baec4e48c51662b33c83203ebae1ba462f10a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953565"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>IBackgroundCopyManager::CreateJob (método)

Crea un trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDisplayName* \[ En\]
</dt> <dd>

Cadena terminada en NULL que contiene un nombre para mostrar para el trabajo. Normalmente, el nombre para mostrar se usa para identificar el trabajo en una interfaz de usuario. Tenga en cuenta que más de un trabajo puede tener el mismo nombre para mostrar. No debe ser **NULL.** El nombre está limitado a 256 caracteres, sin incluir el terminador null.

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo de trabajo de transferencia, como BG_JOB_TYPE_DOWNLOAD. Para obtener una lista de tipos de transferencia, vea la [**enumeración BG_JOB_TYPE**](bg-job-type.md) datos.

</dd> <dt>

*pJobID* \[ out\]
</dt> <dd>

Identifica de forma única el trabajo en la cola. Use este identificador cuando llame al método [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) para obtener un trabajo de la cola.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Puntero [**de interfaz IBackgroundCopyJob**](ibackgroundcopyjob-.md) que se usa para modificar las propiedades del trabajo y especificar los archivos que se transferirán. Para activar el trabajo en la cola, llame al [**método IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md) Libere *ppJob* cuando haya terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | Generó correctamente el nuevo trabajo.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo el usuario que crea el trabajo o [](https://www.bing.com/search?q=add+files+to+the+job) un usuario con privilegios de administrador pueden agregar archivos al trabajo y cambiar las propiedades [del trabajo.](https://www.bing.com/search?q=change+the+job's+properties)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                           |
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

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
