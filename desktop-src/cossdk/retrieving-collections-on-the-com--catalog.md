---
description: Recuperar recopilaciones en el catálogo de COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recuperar recopilaciones en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807172"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Recuperar recopilaciones en el catálogo de COM+

Los datos del catálogo de COM+ se almacenan en una jerarquía de colecciones. En la herramienta administrativa Servicios de componentes, muchas de estas colecciones aparecen como carpetas en el árbol de consola. Solo se puede tener acceso a las colecciones que no aparecen como carpetas mediante programación. Las colecciones sirven como contenedores para los elementos. Los elementos de una colección determinada son de un tipo coherente; es decir, todos representan el mismo tipo de elemento y puede haber un número arbitrario de elementos en una colección. Por ejemplo, la colección de [**aplicaciones**](applications.md) contiene un elemento para cada aplicación com+ instalada en la máquina. Esta colección aparece en la herramienta administrativa como la carpeta **aplicaciones com+** .

Las colecciones se producen en una estructura jerárquica porque los elementos que contienen siguen un orden INNATE de inclusión. Por ejemplo, dado que los componentes se instalan en una aplicación COM+, la colección de [**componentes**](components.md) se encuentra lógicamente en la colección de [**aplicaciones**](applications.md) . En particular, para contener los componentes instalados en esa aplicación concreta, existe una colección de **componentes** distintos para cada elemento de la colección de **aplicaciones** .

Debe obtener una colección en el catálogo siempre que desee recuperar un elemento y establecer sus propiedades. En el caso general, debe recorrer varias colecciones para llegar al elemento que desee. Para ver el procedimiento para hacerlo, consulte [navegación por la jerarquía de la colección de com+](navigating-the-com--collection-hierarchy.md).

Una vez que haya recuperado una colección y antes de poder trabajar directamente con los elementos que contiene, debe rellenar la colección, que captura los datos para el contenido de la colección desde el catálogo de COM+. Para obtener más información, vea [rellenar colecciones de com+](populating-com--collections.md).

Además, existe una utilidad que permite realizar consultas de forma dinámica para ver qué colecciones relacionadas están disponibles en una colección determinada que se está conteniendo. Para obtener más información, consulte [consultar las colecciones relacionadas disponibles](querying-for-available-related-collections.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Operaciones de administración de COM+ en transacciones](com--administration-operations-within-transactions.md)
</dt> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Establecer propiedades y guardar cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



