---
description: Rellenar colecciones com+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Rellenar colecciones com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990675"
---
# <a name="populating-com-collections"></a>Rellenar colecciones com+

Después de recuperar una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección mediante el [**método Populate.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) Esto captura los datos del contenido de la colección del catálogo de COM+.

Es importante comprender que cada vez que usa los objetos COMAdmin para manipular elementos o datos en colecciones, realmente está trabajando en datos almacenados en caché de forma transitoria. no está trabajando directamente con el catálogo persistente. Nada de lo que haga con una colección o cualquiera de sus elementos se reflejará en el catálogo hasta que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en la colección. Para obtener más información, vea [Guardar o descartar cambios.](saving-or-discarding-changes.md)

Las llamadas posteriores [**a Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), antes de llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), tienen el efecto de descartar los cambios pendientes en todos los elementos de la colección. **Rellenar** siempre rellena la memoria caché en la que está trabajando con los datos que se conservan en el almacén de datos del catálogo subyacente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegar por la jerarquía de colecciones com+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Consulta de colecciones relacionadas disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



