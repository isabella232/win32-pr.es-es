---
description: Los administradores pueden utilizar COM+ para crear y configurar particiones COM+ mediante programación.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Crear y configurar particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538823"
---
# <a name="creating-and-configuring-com-partitions"></a>Crear y configurar particiones COM+

Los administradores pueden utilizar COM+ para crear y configurar particiones COM+ mediante programación. De hecho, todas las tareas de creación y configuración que puede realizar un administrador desde los servicios de componentes o las herramientas administrativas de Active Directory usuarios y equipos se pueden realizar mediante colecciones, objetos e interfaces COM+ o a través de la interfaz del sistema Active Directory (ADSI).

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición de COM+ disponible.

* * Windows 2000: * * el servicio de particiones COM+ no está disponible en Windows 2000.

> [!Note]  
> El servicio de particiones COM+ no está habilitado de forma predeterminada. Para usar el servicio de particiones de COM+, debe habilitarlo mediante la herramienta de administración de servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a true.

 

Para realizar tareas relacionadas con las particiones, COM+ proporciona los siguientes elementos de programación:

-   Métodos y propiedades de la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) en la clase [**COMAdminCatalog**](comadmincatalog.md) :
    -   Propiedad [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .
    -   Propiedad [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .
    -   Propiedad [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .
    -   Método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .
    -   Método [**GetPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .
    -   Método [**GetPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .
    -   Propiedad [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .
-   Un conjunto de objetos COM+ para crear y administrar particiones en Active Directory.
-   Una clave del registro de COM+, **PartitionCache**, para cambiar el tamaño de la memoria caché de la partición.
-   Un conjunto de colecciones de administración de [com+](com--administration-collections.md)relacionadas con las particiones:
    -   Colección de [**particiones**](partitions.md) .
    -   Colección [**PartitionUsers**](partitionusers.md) .
    -   Colección [**RolesForPartition**](rolesforpartition.md) .
    -   Colección [**UsersInPartitionRole**](usersinpartitionrole.md) .
-   Propiedades de otras [colecciones de administración de com+](com--administration-collections.md):
    -   Propiedad PartitionID de la colección [**ApplicationInstances**](applicationinstances.md) .
    -   Propiedad AppPartitionID en la colección [**Applications**](applications.md) .
    -   Propiedades PartitionDescription, PartitionID y PartitionName en la colección [**FilesForImport**](filesforimport.md) .
    -   Propiedades DSPartitionLookupEnabled, LocalPartitionLookupEnabled y PartitionsEnabled en la colección [**LocalComputer**](localcomputer.md) .
    -   Propiedades EventClassPartitionID y SubscriberPartitionID en la colección [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .
    -   Propiedades EventClassPartitionID y SubscriberPartitionID en la colección [**TransientSubscriptions**](transientsubscriptions.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la memoria caché de partición](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupar aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administrar particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administrar particiones en Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



