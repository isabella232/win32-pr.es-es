---
title: Método IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization.h)
description: Identifica la implementación de la interfaz IBackgroundCopyCallback que se Optimización de distribución. Use la interfaz IBackgroundCopyCallback para recibir notificaciones de eventos relacionados con el trabajo.
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
ms.openlocfilehash: 66d7f8d10ff08bf95a9477f91dcc4e3f43469a6a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519846"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>IBackgroundCopyJob::SetNotifyInterface (método)

Identifica la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) que se Optimización de distribución. Use la **interfaz IBackgroundCopyCallback para** recibir notificaciones de eventos relacionados con el trabajo.

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

La interfaz de notificación deja de ser válida cuando finaliza la aplicación; Optimización de distribución no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método **SetNotifyInterface** en los trabajos existentes para los que desea recibir la notificación. Si necesita capturar información de estado y progreso que se produjo desde la última vez que se ha ejecutado la aplicación, sondee la información de estado y progreso durante la inicialización de la aplicación.

Solo el propietario o creador del trabajo o un administrador pueden registrarse para recibir notificaciones.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





