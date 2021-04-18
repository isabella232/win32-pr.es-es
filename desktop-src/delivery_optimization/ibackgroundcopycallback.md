---
title: Interfaz IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implemente la interfaz IBackgroundCopyCallback para recibir la notificación de que un trabajo se ha completado, se ha modificado o tiene un error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.
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
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714575"
---
# <a name="ibackgroundcopycallback-interface"></a>Interfaz IBackgroundCopyCallback

Implemente la interfaz **IBackgroundCopyCallback** para recibir la notificación de que un trabajo se ha completado, se ha modificado o tiene un error. Los clientes usan esta interfaz en lugar de sondear el estado del trabajo.

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyCallback** tiene estos métodos.



| Método                                                                    | Descripción                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Se le llama cuando se produce un error.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Se le llama cuando se modifica un trabajo.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Se le llama cuando todos los archivos del trabajo se han transferido correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Para recibir notificaciones, llame al método [**IBackgroundCopyJob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar el puntero de interfaz a la implementación de **IBackgroundCopyCallback** . Para especificar las notificaciones que desea recibir, llame al método [**IBackgroundCopyJob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .

Realizará llamadas a las devoluciones de llamada siempre que el puntero de interfaz sea válido. La interfaz de notificación ya no es válida cuando finaliza la aplicación; No conserva la interfaz de notificación. Como resultado, el proceso de inicialización de la aplicación debe llamar al método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) en los trabajos existentes para los que desea recibir la notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
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

 

