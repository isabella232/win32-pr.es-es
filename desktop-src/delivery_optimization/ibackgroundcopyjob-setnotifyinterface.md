---
title: Método IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization.h)
description: Identifica la implementación de la interfaz IBackgroundCopyCallback que se debe realizar. Use la interfaz IBackgroundCopyCallback para recibir notificaciones de eventos relacionados con el trabajo.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Método SetNotifyInterface
- Método SetNotifyInterface, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793415"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>IBackgroundCopyJob::SetNotifyInterface (método)

Identifica la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) que se debe realizar. Use la **interfaz IBackgroundCopyCallback para** recibir notificaciones de eventos relacionados con el trabajo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

Puntero [**de interfaz IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Para quitar el puntero de interfaz de devolución de llamada actual, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes **valores HRESULT,** así como otros.



| Código devuelto                                                                              | Descripción                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK**</dt> </dl> | El puntero de interfaz de notificación se estableció correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método solo si implementa la [**interfaz IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Use el **método SetNotifyInterface** junto con el método [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar el tipo de notificación que desea recibir.

La interfaz de notificación deja de ser válida cuando finaliza la aplicación; DO no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método **SetNotifyInterface** en los trabajos existentes para los que desea recibir la notificación. Si necesita capturar la información de estado y progreso que se ha producido desde la última vez que se ha ejecutado la aplicación, sondee la información de estado y progreso durante la inicialización de la aplicación.

Solo el propietario o creador del trabajo o un administrador pueden registrarse para recibir notificaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





