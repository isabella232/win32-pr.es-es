---
title: Interfaz IBackgroundCopyCallback (Deliveryoptimization.h)
description: Implemente la interfaz IBackgroundCopyCallback para recibir la notificación de que un trabajo se ha completado, se ha modificado o está en error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interfaz IBackgroundCopyCallback
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
ms.openlocfilehash: 165a1edcdb6bd70de8fad379fcc89d5afc36776348fd7751277614229a23377e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953645"
---
# <a name="ibackgroundcopycallback-interface"></a>Interfaz IBackgroundCopyCallback

Implemente **la interfaz IBackgroundCopyCallback** para recibir la notificación de que un trabajo se ha completado, se ha modificado o está en error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyCallback** tiene estos métodos.



| Método                                                                    | Descripción                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Se llama cuando se produce un error.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Se llama cuando se modifica un trabajo.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Se llama cuando todos los archivos del trabajo se han transferido correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Para recibir notificaciones, llame al método [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar el puntero de interfaz a la implementación **de IBackgroundCopyCallback.** Para especificar qué notificaciones desea recibir, llame al método [**IBackgroundCopyJob::SetNotifyFlags.**](ibackgroundcopyjob-setnotifyflags.md)

DO llamará a las devoluciones de llamada siempre que el puntero de interfaz sea válido. La interfaz de notificación ya no es válida cuando finaliza la aplicación; DO no conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) en los trabajos existentes para los que desea recibir la notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
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

 

