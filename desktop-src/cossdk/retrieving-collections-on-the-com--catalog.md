---
description: Recuperar colecciones en el catálogo de COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperar colecciones en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf70f6fe6a7ab25ebed0338e56db1abfc0b869134725d52108b83473b9182d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812589"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Recuperar colecciones en el catálogo de COM+

Los datos del catálogo com+ se almacenan dentro de una jerarquía de colecciones. En la herramienta administrativa Servicios de componentes, muchas de estas colecciones aparecen como carpetas en el árbol de consola. Solo se puede acceder mediante programación a las colecciones que no aparecen como carpetas. Las colecciones sirven como contenedores para los elementos. Los elementos de una colección determinada son todos de un tipo coherente; Es decir, todos representan el mismo tipo de elemento y puede haber un número arbitrario de elementos en una colección. Por ejemplo, la [**colección Aplicaciones**](applications.md) contiene un elemento para cada aplicación COM+ instalada en la máquina. Esta colección aparece en la herramienta administrativa como la **carpeta Aplicaciones COM+.**

Las colecciones se producen en una estructura jerárquica porque los elementos que contienen siguen un orden innate de inclusión. Por ejemplo, dado que los componentes se instalan en una aplicación COM+, la colección [**Components**](components.md) se subsume lógicamente en la [**colección Aplicaciones.**](applications.md) Más concretamente, para contener los componentes instalados en esa aplicación determinada, hay una colección **de componentes** distintos para cada elemento de la **colección Aplicaciones.**

Debe obtener una colección en el catálogo siempre que desee recuperar un elemento y establecer propiedades en él. En el caso general, debe pasar por varias colecciones para llegar al elemento que desee. Para obtener el procedimiento para hacerlo, vea [Navegar por la jerarquía de colecciones de COM+.](navigating-the-com--collection-hierarchy.md)

Después de recuperar una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección, que captura los datos del contenido de la colección del catálogo de COM+. Para obtener más información, [vea Rellenar colecciones de COM+.](populating-com--collections.md)

Además, hay una instalación que puede usar que le permite consultar dinámicamente para ver qué colecciones relacionadas están disponibles en una colección determinada que está manteniendo. Para obtener más información, [vea Consulta de colecciones relacionadas disponibles.](querying-for-available-related-collections.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ dentro de transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



