---
title: Método IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica la implementación de la interfaz IBackgroundCopyCallback que se va a realizar. Use la interfaz IBackgroundCopyCallback para recibir notificaciones de eventos relacionados con el trabajo.
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
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359722"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>IBackgroundCopyJob:: SetNotifyInterface (método)

Identifica la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) que se va a realizar. Use la interfaz **IBackgroundCopyCallback** para recibir notificaciones de eventos relacionados con el trabajo.

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

Puntero a la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Para quitar el puntero de interfaz de devolución de llamada actual, establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve los siguientes valores **HRESULT** , así como otros.



| Código devuelto                                                                              | Descripción                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | El puntero de la interfaz de notificación se estableció correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método solo si implementa la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Use el método **SetNotifyInterface** junto con el método [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar el tipo de notificación que desea recibir.

La interfaz de notificación deja de ser válida cuando finaliza la aplicación; No conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método **SetNotifyInterface** en los trabajos existentes para los que desea recibir la notificación. Si necesita capturar información sobre el estado y el progreso que se produjeron desde la última vez que se ejecutó la aplicación, sondee la información sobre el estado y el progreso durante la inicialización de la aplicación.

Solo el propietario o creador del trabajo o un administrador pueden registrarse para recibir notificaciones.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





