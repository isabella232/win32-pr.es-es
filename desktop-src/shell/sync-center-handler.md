---
description: En este tema se proporciona un examen paso a paso de los requisitos para compilar un archivo DLL que implementa un controlador que se usará con Centro de sincronización. Esta información es válida a fecha de Windows Vista.
title: Desarrollar un controlador de Windows Centro de sincronización de datos
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252105"
---
# <a name="developing-a-windows-sync-center-handler"></a>Desarrollar un controlador de Windows Centro de sincronización de datos

En este tema se proporciona un examen paso a paso de los requisitos para compilar un archivo DLL que implementa un controlador que se usará con Centro de sincronización. Esta información es válida a fecha de Windows Vista.

-   [La experiencia Windows sincronización antes de Vista](#the-windows-synchronization-experience-before-vista)
-   [Centro de sincronización API](#sync-center-apis)
    -   [Interfaces esenciales](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>La experiencia Windows sincronización antes de Vista

Windows XP proporcionó un [Administrador de sincronización](syncmgr-start-page.md) (mobsync.exe). Muchos dispositivos, como reproductores mp3, teléfonos móviles y cámaras, también proporcionaban sus propias interfaces de sincronización en lugar de usar synchronization Manager. Esto dio lugar a una experiencia de usuario incoherente y no descentralizada.

La nueva Centro de sincronización que se proporciona en Windows Vista tiene varias ventajas con respecto al administrador de sincronización anterior.

-   Mejor detectabilidad
-   Menos necesidad de acción directa del usuario
-   No bloquea otras operaciones
-   Mejor visualización del progreso de la sincronización
-   Modelo de desarrollo más fácil de entender

## <a name="sync-center-apis"></a>Centro de sincronización API

Centro de sincronización se comunica con los controladores a través de varias interfaces de Modelo de objetos componentes (COM). No todas estas interfaces son necesarias para implementar un controlador Centro de sincronización usuario. Este tema se ha dividido en dos secciones. En la primera sección se explican las interfaces COM esenciales que todos los controladores deben admitir y en la segunda se examinan las interfaces COM opcionales y se examinan los motivos por los que un controlador las admitiría.

-   [Interfaces esenciales](#essential-interfaces)

### <a name="essential-interfaces"></a>Interfaces esenciales

Todos Centro de sincronización controladores deben admitir las interfaces siguientes:

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) se usan para describir un único elemento de sincronización implicado en la sincronización con el Centro de sincronización. Por lo general, un elemento de sincronización representa un tipo de datos determinado (como imágenes) o una ubicación de datos determinada.

Los elementos de sincronización que representan diferentes ubicaciones de datos permiten sincronizaciones muy específicas. La granularidad de la ubicación es del autor del controlador, pero se debe tener cuidado en el diseño. Si hay demasiados elementos de sincronización (ubicaciones), el usuario está restringido en su capacidad de sincronizar solo determinados datos. En el otro extremo, demasiada granularidad puede volverse no manejable.

Si un controlador admite más de un tipo de datos o varias ubicaciones de datos, debe admitir más de un objeto de elemento de sincronización. Un ejemplo podría ser un asistente de datos personales (PDA) que permite al usuario sincronizar contactos, elementos de calendario y documentos. Estos tres tipos de datos tendrían que representarse mediante tres objetos únicos que exponen las interfaces [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo.**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

La [**interfaz IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) proporciona un mecanismo para enumerar a través de los elementos de sincronización de un controlador. Para recuperar este enumerador, Centro de sincronización llama al método [**ISyncMgrSyncItemContainer::GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) expuesto por el controlador. [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) también contiene otros dos métodos que el Centro de sincronización puede usar para recuperar información sobre los elementos de sincronización del controlador:

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) devuelve un elemento de sincronización específico.
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) devuelve el número de elementos de sincronización admitidos por el controlador.

[**ISyncMgrHandler e**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) se usan para describir las propiedades del hander e iniciar la sincronización real. [**ISyncMgrHandler::Synchronize es**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) donde el código de controlador lleva a cabo la sincronización y proporciona comentarios sobre el progreso y los problemas que se producen.

Muchos de los métodos de interfaz no necesitan implementarse completamente. Centro de sincronización proporciona una cierta cantidad de información predeterminada. Las interfaces permiten a un controlador invalidar esta información y proporcionar información personalizada para mostrar, si es necesario.

 

 



