---
description: Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Información general de los objetos COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466105"
---
# <a name="overview-of-the-comadmin-objects"></a>Información general de los objetos COMAdmin

Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+. Al hacerlo, sirven para modelar toda la funcionalidad proporcionada por la herramienta administrativa Servicios de componentes. Siempre que realice cualquier tipo de administración de COM+, interactuará con el catálogo de COM+. Para obtener una descripción del catálogo, vea [Acceso al catálogo de COM+.](accessing-the-com--catalog.md)

La información que se obtiene de la herramienta administrativa Servicios de componentes o mediante los objetos COMAdmin se estructura de forma similar, y las acciones que se realizan en cualquier contexto son análogas. La correlación básica entre el uso del complemento Servicios de componentes y la administración mediante programación es que las carpetas del árbol de consola del complemento corresponden a colecciones del catálogo de COM+. Es decir, al igual que cada carpeta del complemento contiene elementos de todo un tipo; Por ejemplo, **APLICACIONES COM+** contiene aplicaciones COM+ instaladas: cada colección del catálogo de COM+ contiene elementos de un tipo uniforme. Además, al igual que cada elemento de una carpeta tiene propiedades que puede establecer en una hoja de propiedades, cada elemento de una colección expone las propiedades que puede establecer.

Para permitirle configurar objetos dentro de esta estructura, los objetos COMAdmin proporcionan los medios para hacer lo siguiente:

-   Acceso al catálogo de COM+
-   Acceso a colecciones en el catálogo
-   Acceso a elementos de colecciones
-   Propiedades de acceso en los elementos de las colecciones

Para admitir estas acciones, la biblioteca COMAdmin proporciona las tres clases siguientes:

-   [**COMAdminCatalog**](comadmincatalog.md), que representa el propio catálogo.
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md), que representa cualquier colección.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), que representa cualquier elemento de una colección.

Para obtener descripciones más detalladas de estas clases, vea [Resumen de la descripción de las clases COMAdmin](summary-description-of-the-comadmin-classes.md) en esta sección.

Para obtener una idea rápida de las acciones típicas que se realizan en la administración mediante programación, vea [Ejemplo introductorio con el catálogo de administración de COM+.](introductory-example-using-the-com--administration-catalog.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ dentro de transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



