---
description: Contiene las colecciones de nivel superior en el catálogo.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Colección raíz
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696102"
---
# <a name="root-collection"></a>Colección raíz

Contiene las colecciones de nivel superior en el catálogo. No contiene ningún objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) ni admite ninguna propiedad.

La colección **raíz** no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

No se puede navegar a la colección **raíz** desde cualquier colección.

## <a name="members"></a>Miembros

La colección **raíz** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

A continuación se muestran las colecciones de nivel superior del catálogo:

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**APLICACIONES**](applications.md)
-   [**ComputerList**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServers**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**Particiones**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
