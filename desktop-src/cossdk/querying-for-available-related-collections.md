---
description: Consulta de colecciones relacionadas disponibles
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Consulta de colecciones relacionadas disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366f7a2ad9bec1751549a2377140f6e6a75c4f2c8c822c358028ce2b7b80f0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812783"
---
# <a name="querying-for-available-related-collections"></a>Consulta de colecciones relacionadas disponibles

Si está escribiendo una herramienta de administración de uso general, es probable que tenga que escribir rutinas para navegar por toda la jerarquía de colecciones. Para admitir esto, COM+ tiene una instalación que le permite consultar dinámicamente las colecciones relacionadas que están disponibles en cualquier colección determinada.

La [**colección RelatedCollectionInfo**](relatedcollectioninfo.md) está disponible en cualquier colección que pueda contener y contiene un elemento para cada colección relacionada disponible. Puede enumerar a través de estos elementos para determinar si una colección determinada está disponible.

Puede obtener la colección [**RelatedCollectionInfo**](relatedcollectioninfo.md) de cualquier colección que esté manteniendo mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) dejando el segundo parámetro en blanco donde normalmente especificaría la propiedad Key de un elemento primario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegar por la jerarquía de colecciones com+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Rellenar colecciones com+](populating-com--collections.md)
</dt> <dt>

[Recuperación de colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



