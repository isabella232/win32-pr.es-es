---
description: Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+.
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: Información general de los objetos COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153582"
---
# <a name="overview-of-the-comadmin-objects"></a>Información general de los objetos COMAdmin

Los objetos COMAdmin ofrecen un modelo de objetos simple que proporciona acceso al catálogo de COM+. Al hacerlo, sirven para modelar toda la funcionalidad proporcionada por la herramienta administrativa Servicios de componentes. Siempre que realice cualquier tipo de administración de COM+, podrá interactuar con el catálogo de COM+. Para obtener una descripción del catálogo, vea [obtener acceso al catálogo de com+](accessing-the-com--catalog.md).

La información que se obtiene de la herramienta administrativa Servicios de componentes o mediante el uso de los objetos COMAdmin está estructurada de forma similar, y las acciones que se realizan en ambos contexto son análogas. La correlación básica entre el uso del complemento Servicios de componentes y la administración mediante programación es que las carpetas del árbol de consola del complemento se corresponden con las recopilaciones del catálogo COM+. Es decir, al igual que cada carpeta del complemento contiene elementos de todo tipo; por ejemplo, **las aplicaciones com+** retienen las aplicaciones com+ instaladas: cada colección del catálogo com+ contiene elementos de una clase uniforme. Además, al igual que cada elemento de una carpeta tiene propiedades que se pueden establecer en una hoja de propiedades, cada elemento de una colección expone propiedades que se pueden establecer.

Para que pueda configurar objetos dentro de esta estructura, los objetos COMAdmin proporcionan los medios para hacer lo siguiente:

-   Acceder al catálogo de COM+
-   Obtener acceso a las recopilaciones en el catálogo
-   Obtener acceso a los elementos de las colecciones
-   Obtener acceso a las propiedades de los elementos de las colecciones

Para admitir estas acciones, la biblioteca COMAdmin proporciona las tres clases siguientes:

-   [**COMAdminCatalog**](comadmincatalog.md), que representa el catálogo en sí.
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md), que representa cualquier colección.
-   [**COMAdminCatalogObject**](comadmincatalogobject.md), que representa cualquier elemento de una colección.

Para obtener descripciones más detalladas de estas clases, vea [la Descripción resumida de las clases COMAdmin](summary-description-of-the-comadmin-classes.md) en esta sección.

Para obtener una idea rápida de las acciones típicas que realiza en la administración mediante programación, consulte [el ejemplo de introducción al uso del catálogo de administración de com+](introductory-example-using-the-com--administration-catalog.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ en transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecer propiedades y guardar cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



