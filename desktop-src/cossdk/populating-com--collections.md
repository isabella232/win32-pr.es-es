---
description: Rellenar colecciones de COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Rellenar colecciones de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360049"
---
# <a name="populating-com-collections"></a>Rellenar colecciones de COM+

Una vez que haya recuperado una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección mediante el método [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Obtiene datos para el contenido de la colección desde el catálogo de COM+.

Es importante comprender que cada vez que se usan los objetos COMAdmin para manipular elementos o datos en colecciones, está trabajando realmente en datos almacenados en caché de forma transitoria; no está trabajando directamente con el catálogo guardado. Nada que haga con una colección o con cualquiera de sus elementos se refleja en el catálogo hasta que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en la colección. Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).

Todas las llamadas subsiguientes que se [**rellenan**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), antes de llamar a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), tienen el efecto de descartar los cambios pendientes en todos los elementos de la colección. **Rellenar** siempre rellena la caché en la que se está trabajando con los datos que se conservan en el almacén de datos del catálogo subyacente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegar por la jerarquía de la colección de COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Consultar colecciones relacionadas disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



