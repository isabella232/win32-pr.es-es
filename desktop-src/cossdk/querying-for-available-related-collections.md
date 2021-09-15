---
description: Consulta de colecciones relacionadas disponibles
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Consulta de colecciones relacionadas disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465441"
---
# <a name="querying-for-available-related-collections"></a>Consulta de colecciones relacionadas disponibles

Si está escribiendo una herramienta de administración de uso general, es probable que tenga que escribir rutinas para navegar por toda la jerarquía de colecciones. Para admitir esto, COM+ tiene una instalación que le permite consultar dinámicamente las colecciones relacionadas que están disponibles en cualquier colección determinada.

La [**colección RelatedCollectionInfo**](relatedcollectioninfo.md) está disponible en cualquier colección que pueda contener y contiene un elemento para cada colección relacionada disponible. Puede enumerar estos elementos para determinar si una colección determinada está disponible.

Puede obtener la colección [**RelatedCollectionInfo**](relatedcollectioninfo.md) de cualquier colección que esté manteniendo mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) dejando el segundo parámetro en blanco, donde normalmente especificaría la propiedad Key de un elemento primario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegar por la jerarquía de colecciones com+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Rellenar colecciones COM+](populating-com--collections.md)
</dt> <dt>

[Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



