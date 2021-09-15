---
title: Interfaz IBackgroundCopyCallback (Deliveryoptimization.h)
description: Implemente la interfaz IBackgroundCopyCallback para recibir una notificación de que un trabajo se ha completado, se ha modificado o está en error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- IBackgroundCopyCallback (interfaz)
- Interfaz IBackgroundCopyCallback, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566757"
---
# <a name="ibackgroundcopycallback-interface"></a>IBackgroundCopyCallback (interfaz)

Implemente **la interfaz IBackgroundCopyCallback** para recibir una notificación de que un trabajo se ha completado, se ha modificado o está en error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.

## <a name="members"></a>Members

La **interfaz IBackgroundCopyCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyCallback** tiene estos métodos.



| Método                                                                    | Descripción                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Se llama cuando se produce un error.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Se llama cuando se modifica un trabajo.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Se llama cuando todos los archivos del trabajo se han transferido correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Para recibir notificaciones, llame al método [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar el puntero de interfaz a la implementación **de IBackgroundCopyCallback.** Para especificar qué notificaciones desea recibir, llame al [**método IBackgroundCopyJob::SetNotifyFlags.**](ibackgroundcopyjob-setnotifyflags.md)

DO llamará a las devoluciones de llamada siempre que el puntero de interfaz sea válido. La interfaz de notificación ya no es válida cuando finaliza la aplicación; DO no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) en los trabajos existentes para los que desea recibir la notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback se define como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

