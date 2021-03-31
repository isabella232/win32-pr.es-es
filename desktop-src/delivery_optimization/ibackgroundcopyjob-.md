---
title: Interfaz IBackgroundCopyJob (Deliveryoptimization. h)
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
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079282"
---
# <a name="ibackgroundcopyjob-interface"></a>Interfaz IBackgroundCopyJob

Use la interfaz [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) para agregar archivos al trabajo, establecer el nivel de prioridad del trabajo, determinar el estado del trabajo e iniciar y detener el trabajo.

Para crear un trabajo, llame al método [**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md) . Para obtener un puntero de interfaz [**IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) a un trabajo existente, llame al método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyJob** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyJob** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyJob** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancelar**](ibackgroundcopyjob-cancel.md)                             | Cancela el trabajo y quita los archivos temporales del cliente.<br/>                                                                                                                                                           |
| [**Completo**](ibackgroundcopyjob-complete.md)                         | Finaliza el trabajo y guarda los archivos transferidos en el cliente.<br/>                                                                                                                                                            |
| [**Enumfiles (**](ibackgroundcopyjob-enumfiles.md)                       | Devuelve un puntero de interfaz a un objeto de enumerador que se utiliza para enumerar los archivos del trabajo.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Recupera el nombre para mostrar que identifica el trabajo.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Recupera un puntero de interfaz al objeto de error después de que se produzca un error.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Recupera el identificador del trabajo en la cola.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Recupera la cantidad de tiempo que continúa intentando transferir el archivo después de encontrar una condición de error transitoria.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Recupera las marcas de notificación de eventos (devolución de llamada) que ha establecido para la aplicación.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Recupera un puntero a la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (devoluciones de llamada).<br/>                                                                                    |
| [**GetPriority (**](ibackgroundcopyjob-getpriority.md)                   | Recupera el nivel de prioridad que ha establecido para el trabajo.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Recupera información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos al cliente.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Recupera el estado del trabajo.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Recupera las marcas de tiempo de las actividades relacionadas con el trabajo, como la hora en que se creó el trabajo.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Recupera el tipo de transferencia que se realiza, por ejemplo, una descarga de archivos.<br/>                                                                                                                                               |
| [**Reanudar**](ibackgroundcopyjob-resume.md)                             | Inicia un nuevo trabajo o reinicia un trabajo suspendido.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Especifica la cantidad de tiempo que continúa intentando transferir el archivo después de encontrar una condición de error transitorio.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Especifica el tipo de notificación de eventos que se va a recibir.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Especifica un puntero a la implementación de la interfaz [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (devoluciones de llamada). La interfaz recibe una notificación basada en las marcas de notificación de eventos que establezca.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Especifica la prioridad del trabajo con respecto a otros trabajos de la cola de transferencia.<br/>                                                                                                                                        |
| [**Suspender**](ibackgroundcopyjob-suspend.md)                           | Pausa el trabajo.<br/>                                                                                                                                                                                                        |



 

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

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

