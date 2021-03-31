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
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/27/2021
ms.locfileid: "104083511"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>IBackgroundCopyManager:: CreateJob (método)

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

*pDisplayName* \[ de\]
</dt> <dd>

Cadena terminada en null que contiene un nombre para mostrar del trabajo. Normalmente, el nombre para mostrar se usa para identificar el trabajo en una interfaz de usuario. Tenga en cuenta que más de un trabajo puede tener el mismo nombre para mostrar. No debe ser **null**. El nombre está limitado a 256 caracteres, sin incluir el terminador nulo.

</dd> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Tipo de trabajo de transferencia, como BG_JOB_TYPE_DOWNLOAD. Para obtener una lista de tipos de transferencia, vea la enumeración [**BG_JOB_TYPE**](bg-job-type.md) .

</dd> <dt>

*pJobID* \[ enuncia\]
</dt> <dd>

Identifica de forma única el trabajo en la cola. Use este identificador al llamar al método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) para obtener un trabajo de la cola.

</dd> <dt>

*ppJob* \[ enuncia\]
</dt> <dd>

Puntero de interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) que se usa para modificar las propiedades del trabajo y especificar los archivos que se van a transferir. Para activar el trabajo en la cola, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) . Suelte *ppJob* cuando termine.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El nuevo trabajo se generó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo el usuario que crea el trabajo o un usuario con privilegios de administrador puede [Agregar archivos al trabajo](https://www.bing.com/search?q=add+files+to+the+job) y [cambiar las propiedades del trabajo](https://www.bing.com/search?q=change+the+job's+properties).

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

[**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
