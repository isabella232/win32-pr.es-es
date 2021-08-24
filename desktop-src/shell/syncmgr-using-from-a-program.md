---
description: Para permitir que la aplicación funcione con el Administrador de sincronización, debe implementar un objeto del Modelo de objetos componentes (COM) para controlar las notificaciones de sincronización que recibe de SyncMgr.
title: Uso del Administrador de sincronización desde un programa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11e959399624d30e1e6d7ce87fb8bb247de7c9c420ef9b2427c7b9bdeb00e7f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709385"
---
# <a name="using-synchronization-manager-from-a-program"></a>Uso del Administrador de sincronización desde un programa

Para permitir que la aplicación funcione con el Administrador de sincronización, debe implementar un objeto del Modelo de objetos componentes (COM) para controlar las notificaciones de sincronización que recibe de SyncMgr. El controlador de la aplicación realiza la sincronización de los elementos que controla. Incluido en el controlador, debe implementar la [**interfaz ISyncMgrSynchronize.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) Además, debe proporcionar un objeto enumerador e [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para cualquier elemento independiente que la aplicación pueda sincronizar.

SyncMgr implementa [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) e [**ISyncMgrSynchronizeInvoke.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke)

SyncMgr llama a los métodos de [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) para obtener información sobre los elementos que controla la aplicación e información sobre el controlador que se proporciona para sincronizar estos elementos.

En tiempo de ejecución, el proceso de sincronización sigue estos pasos.

1.  SyncMgr notifica a la aplicación que es el momento de que se produzca la sincronización de uno de los elementos que controla la aplicación mediante una llamada al [**método ISyncMgrSynchronize::Initialize.**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize)
2.  SyncMgr llama [**a ISyncMgrSynchronize::EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) para obtener la interfaz [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para los elementos que controla la aplicación.
3.  SyncMgr llama [**a ISyncMgrSynchronize::SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) para proporcionar al controlador el puntero de interfaz para la [**interfaz ISyncMgrSynchronizeCallback.**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) El controlador usa esta interfaz para volver a llamar a SyncMgr durante la sincronización.
4.  A continuación, SyncMgr llama al método [**ISyncMgrSynchronize::P repareForSync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) para dar al controlador la oportunidad de mostrar cualquier elemento de interfaz de usuario necesario antes de que comience la sincronización. Por ejemplo, una aplicación de correo electrónico puede mostrar un cuadro de diálogo de inicio de sesión de usuario.
5.  El controlador llama a [**ISyncMgrSynchronizeCallback::EnableModeless antes**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) y después de mostrar los elementos de la interfaz de usuario. El controlador llama [**a ISyncMgrSynchronizeCallback::P repareForSyncCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) cuando haya terminado.
6.  SyncMgr llama al [**método ISyncMgrSynchronize::Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) para iniciar la sincronización.

Durante el proceso de sincronización, SyncMgr continúa llamada a métodos en la [**interfaz ISyncMgrSynchronize.**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) Puede enviar los errores, el progreso y las notificaciones del controlador. También puede enumerar los elementos que controla la aplicación o permitir que la aplicación muestre las propiedades de los elementos.

El controlador llama a métodos de [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) para determinar si se debe omitir un elemento, registrar errores y publicar información de progreso durante el proceso de sincronización.

Para más información, consulte las páginas de referencia relacionadas para las interfaces implicadas.

Cuando se completa la sincronización, el controlador llama a [**ISyncMgrSynchronizeCallback::SynchronizeCompleted.**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted)

 

 



