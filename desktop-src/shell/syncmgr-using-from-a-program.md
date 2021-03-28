---
description: Para permitir que la aplicación funcione con el administrador de sincronización, debe implementar un objeto de modelo de objetos componentes (COM) para controlar las notificaciones de sincronización que recibe de SyncMgr.
title: Usar el administrador de sincronización desde un programa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9bd5abdc382c82c6c1aafcda3a967337384dc807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546926"
---
# <a name="using-synchronization-manager-from-a-program"></a>Usar el administrador de sincronización desde un programa

Para permitir que la aplicación funcione con el administrador de sincronización, debe implementar un objeto de modelo de objetos componentes (COM) para controlar las notificaciones de sincronización que recibe de SyncMgr. El controlador de la aplicación realiza la sincronización de los elementos que controla. Se incluye en el controlador, debe implementar la interfaz [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Además, debe proporcionar un objeto de enumerador y [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para cualquier elemento independiente que la aplicación pueda sincronizar.

SyncMgr implementa [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) y [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

SyncMgr llama a los métodos de [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) para obtener información sobre los elementos que controla la aplicación e información sobre el controlador que se proporciona para sincronizar estos elementos.

En tiempo de ejecución, el proceso de sincronización sigue estos pasos.

1.  SyncMgr notifica a la aplicación que es el momento de que se produzca la sincronización de uno de los elementos que controla la aplicación llamando al método [**ISyncMgrSynchronize:: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) .
2.  SyncMgr llama a [**ISyncMgrSynchronize:: EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) para obtener la interfaz [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para los elementos administrados por la aplicación.
3.  SyncMgr llama a [**ISyncMgrSynchronize:: SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) para proporcionar al controlador el puntero de interfaz para la interfaz [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) . El controlador usa esta interfaz para devolver la llamada a SyncMgr durante la sincronización.
4.  A continuación, SyncMgr llama al método [**ISyncMgrSynchronize::P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) para dar a su controlador una oportunidad de mostrar cualquier elemento de la interfaz de usuario que sea necesario antes de comenzar la sincronización. Por ejemplo, una aplicación de correo electrónico puede mostrar un cuadro de diálogo de inicio de sesión de usuario.
5.  El controlador llama a [**ISyncMgrSynchronizeCallback:: EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) antes y después de mostrar los elementos de la interfaz de usuario. El controlador llama a [**ISyncMgrSynchronizeCallback::P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) cuando haya terminado.
6.  SyncMgr llama al método [**ISyncMgrSynchronize:: Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) para iniciar la sincronización.

Durante el proceso de sincronización, SyncMgr sigue llamando a los métodos de la interfaz [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Puede enviar los errores del controlador, el progreso y las notificaciones. También puede enumerar los elementos que controla la aplicación o permite a la aplicación mostrar las propiedades de los elementos.

El controlador llama a los métodos de [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) para determinar si se debe omitir un elemento, registrar errores y publicar información de progreso durante el proceso de sincronización.

Para obtener más información, consulte las páginas de referencia relacionadas de las interfaces implicadas.

Cuando se completa la sincronización, el controlador llama a [**ISyncMgrSynchronizeCallback:: SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 



