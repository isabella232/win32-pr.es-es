---
description: Los administradores pueden usar COM+ para crear y configurar particiones COM+ mediante programación.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Creación y configuración de particiones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cc9623272d4aba345cc666deb5c63965584af94f42dbf869b00cf7d52a2f30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858995"
---
# <a name="creating-and-configuring-com-partitions"></a>Creación y configuración de particiones COM+

Los administradores pueden usar COM+ para crear y configurar particiones COM+ mediante programación. De hecho, todas las tareas de creación y configuración que un administrador puede realizar desde los Servicios de componentes o las herramientas administrativas de Usuarios y equipos de Active Directory se pueden realizar mediante colecciones, objetos e interfaces de COM+ o a través de la interfaz del sistema (ADSI) de Active Directory.

**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible. La partición global es la única partición COM+ disponible.

**Windows 2000: ** El servicio de particiones COM+ no está disponible en Windows 2000.

> [!Note]  
> El servicio de particiones COM+ no está habilitado de forma predeterminada. Para usar el servicio de particiones COM+, debe habilitarlo a través de la herramienta de administración servicios de componentes o cambiando la propiedad PartitionsEnabled de la colección [**LocalComputer**](localcomputer.md) a True.

 

Para realizar tareas relacionadas con particiones, COM+ proporciona los siguientes elementos de programación:

-   Métodos y propiedades de [**la interfaz ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) en la [**clase COMAdminCatalog:**](comadmincatalog.md)
    -   [**Propiedad CurrentPartition.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition)
    -   [**Propiedad CurrentPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid)
    -   [**Propiedad CurrentPartitionName.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname)
    -   [**Método FlushPartitionCache.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)
    -   [**Método GetPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid)
    -   [**Método GetPartitionName.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname)
    -   [**Propiedad GlobalPartitionID.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid)
-   Un conjunto de objetos COM+ para crear y administrar particiones en Active Directory.
-   Una clave del Registro COM+, **PartitionCache,** para cambiar el tamaño de la caché de particiones.
-   Un conjunto de colecciones de administración de COM+ relacionadas con [particiones:](com--administration-collections.md)
    -   [**Colección de particiones.**](partitions.md)
    -   [**Colección PartitionUsers.**](partitionusers.md)
    -   [**Colección RolesForPartition.**](rolesforpartition.md)
    -   [**Colección UsersInPartitionRole.**](usersinpartitionrole.md)
-   Propiedades de otras [colecciones de administración de COM+:](com--administration-collections.md)
    -   Propiedad PartitionID de la [**colección ApplicationInstances.**](applicationinstances.md)
    -   Propiedad AppPartitionID en la [**colección Applications.**](applications.md)
    -   Propiedades PartitionDescription, PartitionID y PartitionName de la [**colección FilesForImport.**](filesforimport.md)
    -   Las propiedades DSPartitionLookupEnabled, LocalPartitionLookupEnabled y PartitionsEnabled de la [**colección LocalComputer.**](localcomputer.md)
    -   Propiedades EventClassPartitionID y SubscriberPartitionID de la [**colección SubscriptionsForComponent.**](subscriptionsforcomponent.md)
    -   Propiedades EventClassPartitionID y SubscriberPartitionID de [**la colección TransientSubscriptions.**](transientsubscriptions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recopilación de métricas de partición](collecting-partition-metrics.md)
</dt> <dt>

[Configuración de la caché de particiones](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupación de aplicaciones en particiones](grouping-applications-into-partitions.md)
</dt> <dt>

[Administración de particiones locales](managing-local-partitions.md)
</dt> <dt>

[Administración de particiones dentro de Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Establecer derechos administrativos para una partición](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



