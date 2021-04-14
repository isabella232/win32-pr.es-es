---
description: En este tema se proporciona un examen paso a paso de los requisitos para crear un archivo DLL que implementa un controlador que se va a usar con el centro de sincronización. Esta información es válida en Windows Vista.
title: Desarrollar un controlador del centro de sincronización de Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985559"
---
# <a name="developing-a-windows-sync-center-handler"></a>Desarrollar un controlador del centro de sincronización de Windows

En este tema se proporciona un examen paso a paso de los requisitos para crear un archivo DLL que implementa un controlador que se va a usar con el centro de sincronización. Esta información es válida en Windows Vista.

-   [La experiencia de sincronización de Windows antes de vista](#the-windows-synchronization-experience-before-vista)
-   [API del centro de sincronización](#sync-center-apis)
    -   [Interfaces esenciales](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>La experiencia de sincronización de Windows antes de vista

Windows XP proporcionó un [Administrador de sincronización](syncmgr-start-page.md) (mobsync.exe). Muchos dispositivos como reproductores MP3, teléfonos móviles y cámaras también proporcionan sus propias interfaces de sincronización en lugar de usar el administrador de sincronización. Esto dio lugar a una experiencia de usuario incoherente y no centralizada.

La nueva característica del centro de sincronización proporcionada en Windows Vista tiene varias ventajas con respecto a la versión anterior del administrador de sincronización.

-   Mejor capacidad de detección
-   Menos necesidad de acción directa del usuario
-   No bloquea otras operaciones
-   Mejor visualización del progreso de sincronización
-   Modelo de desarrollo más fácil de entender

## <a name="sync-center-apis"></a>API del centro de sincronización

El centro de sincronización se comunica con los controladores a través de una serie de interfaces COM (modelo de objetos componentes). No todas estas interfaces son necesarias para implementar un controlador del centro de sincronización. Este tema se ha dividido en dos secciones. En la primera sección se explican las interfaces COM esenciales que cada controlador debe admitir y en la segunda sección se examinan las interfaces COM opcionales y se analizan las razones por las que un controlador las admitiría.

-   [Interfaces esenciales](#essential-interfaces)

### <a name="essential-interfaces"></a>Interfaces esenciales

Todos los controladores del centro de sincronización deben admitir las siguientes interfaces:

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) y [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) se usan para describir un solo elemento de sincronización implicado en la sincronización con el centro de sincronización. Un elemento de sincronización generalmente representa un tipo de datos determinado (como imágenes) o una ubicación de datos determinada.

Los elementos de sincronización que representan diferentes ubicaciones de datos permiten sincronizaciones muy específicas. La granularidad de la ubicación depende del autor del controlador, pero se debe tener cuidado en el diseño. Si hay demasiados elementos de sincronización (ubicaciones), el usuario está restringido por su capacidad de sincronizar solo determinados datos. En el otro extremo, demasiada granularidad puede ser no administrable.

Si un controlador admite más de un tipo de datos o varias ubicaciones de datos, necesita admitir más de un objeto de elemento de sincronización. Un ejemplo podría ser un asistente de datos personales (PDA) que permite al usuario sincronizar contactos, elementos de calendario y documentos. Estos tres tipos de datos se deben representar mediante tres objetos únicos que exponen las interfaces [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) y [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) .

La interfaz [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) proporciona un mecanismo para enumerar a través de los elementos de sincronización de un controlador. Para recuperar este enumerador, el centro de sincronización llama al método [**ISyncMgrSyncItemContainer:: GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) expuesto por el controlador. [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) también contiene otros dos métodos que el centro de sincronización puede usar para recuperar información sobre los elementos de sincronización del controlador:

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) devuelve un elemento de sincronización específico.
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) devuelve el número de elementos de sincronización admitidos por el controlador.

[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) y [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) se usan para describir las propiedades del controlador y para iniciar la sincronización real. [**ISyncMgrHandler:: Synchronize**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) es donde el código del controlador lleva a cabo la sincronización y proporciona información sobre el progreso y los problemas que se producen.

No es necesario implementar completamente muchos de los métodos de interfaz. El centro de sincronización proporciona una determinada cantidad de información predeterminada. Las interfaces permiten que un controlador invalide esta información y proporcione la información personalizada que se va a mostrar, si es necesario.

 

 



