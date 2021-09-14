---
description: Recuperación de colecciones en el catálogo de COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperación de colecciones en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973514"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Recuperación de colecciones en el catálogo de COM+

Los datos del catálogo de COM+ se almacenan dentro de una jerarquía de colecciones. En la herramienta administrativa Servicios de componentes, muchas de estas colecciones aparecen como carpetas en el árbol de consola. Solo se puede acceder mediante programación a las colecciones que no aparecen como carpetas. Las colecciones sirven como contenedores para los elementos. Los elementos de una colección determinada son todos de un tipo coherente; Es decir, todos representan el mismo tipo de elemento y puede haber un número arbitrario de elementos en una colección. Por ejemplo, la [**colección Aplicaciones**](applications.md) contiene un elemento para cada aplicación COM+ instalada en la máquina. Esta colección aparece en la herramienta administrativa como la **carpeta Aplicaciones COM+.**

Las colecciones se producen en una estructura jerárquica porque los elementos que contienen siguen un orden innate de inclusión. Por ejemplo, dado que los componentes se instalan en una aplicación COM+, la colección [**Components**](components.md) se sume lógicamente en la [**colección Aplicaciones.**](applications.md) Más concretamente, para contener los componentes instalados en esa aplicación en particular, hay una colección **de componentes** distinta para cada elemento de la **colección Aplicaciones.**

Debe obtener una colección en el catálogo siempre que desee recuperar un elemento y establecer propiedades en él. En el caso general, debe pasar por varias colecciones para llegar al elemento que desee. Para obtener el procedimiento para hacerlo, vea Navegar por la jerarquía de [colecciones de COM+.](navigating-the-com--collection-hierarchy.md)

Después de recuperar una colección y de poder trabajar directamente con los elementos que contiene, debe rellenar la colección, que captura los datos del contenido de la colección del catálogo de COM+. Para obtener más información, [vea Rellenar colecciones com+](populating-com--collections.md).

Además, hay una instalación que puede usar que le permite consultar dinámicamente para ver qué colecciones relacionadas están disponibles en una recopilación determinada que está manteniendo. Para obtener más información, [vea Consulta de colecciones relacionadas disponibles.](querying-for-available-related-collections.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ dentro de transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio de uso del catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



