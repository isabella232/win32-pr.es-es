---
title: Interfaz IBackgroundCopyJob (Deliveryoptimization.h)
description: Use la interfaz IBackgroundCopyJob para agregar archivos al trabajo, establecer el nivel de prioridad del trabajo, determinar el estado del trabajo e iniciar y detener el trabajo.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27febd08519a06f7ad452882cf0725fed209e0306182ba336343049936795acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543031"
---
# <a name="ibackgroundcopyjob-interface"></a>Interfaz IBackgroundCopyJob

Use la [**interfaz IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) para agregar archivos al trabajo, establecer el nivel de prioridad del trabajo, determinar el estado del trabajo e iniciar y detener el trabajo.

Para crear un trabajo, llame al [**método IBackgroundCopyManager::CreateJob.**](ibackgroundcopymanager-createjob.md) Para obtener un [**puntero de interfaz IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) a un trabajo existente, llame al [**método IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyJob** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyJob** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyJob** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancelar**](ibackgroundcopyjob-cancel.md)                             | Cancela el trabajo y quita los archivos temporales del cliente.<br/>                                                                                                                                                           |
| [**Completo**](ibackgroundcopyjob-complete.md)                         | Finaliza el trabajo y guarda los archivos transferidos en el cliente.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Devuelve un puntero de interfaz a un objeto enumerador que se usa para enumerar los archivos del trabajo.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Recupera el nombre para mostrar que identifica el trabajo.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Recupera un puntero de interfaz al objeto de error después de que se produzca un error.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Recupera el identificador del trabajo en la cola.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Recupera el período de tiempo que do sigue intentando transferir el archivo después de encontrar una condición de error transitorio.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Recupera las marcas de notificación de eventos (devolución de llamada) que ha establecido para la aplicación.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Recupera un puntero a la implementación de la [**interfaz IBackgroundCopyCallback**](ibackgroundcopycallback.md) (devoluciones de llamada).<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Recupera el nivel de prioridad que ha establecido para el trabajo.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Recupera información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos al cliente.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Recupera el estado del trabajo.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Recupera marcas de tiempo para las actividades relacionadas con el trabajo, como la hora en que se creó el trabajo.<br/>                                                                                                                         |
| [**Gettype**](ibackgroundcopyjob-gettype.md)                           | Recupera el tipo de transferencia que se realiza, como una descarga de archivos.<br/>                                                                                                                                               |
| [**Reanudar**](ibackgroundcopyjob-resume.md)                             | Inicia un nuevo trabajo o reinicia un trabajo suspendido.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Especifica el período de tiempo que do sigue intentando transferir el archivo después de encontrar una condición de error transitorio.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Especifica el tipo de notificación de eventos que se recibirá.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Especifica un puntero a la implementación de la [**interfaz IBackgroundCopyCallback**](ibackgroundcopycallback.md) (devoluciones de llamada). La interfaz recibe la notificación en función de las marcas de notificación de eventos que establezca.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Especifica la prioridad del trabajo con respecto a otros trabajos de la cola de transferencia.<br/>                                                                                                                                        |
| [**Suspender**](ibackgroundcopyjob-suspend.md)                           | Pausa el trabajo.<br/>                                                                                                                                                                                                        |



 

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

