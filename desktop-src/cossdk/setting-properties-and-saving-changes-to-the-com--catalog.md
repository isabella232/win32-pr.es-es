---
description: Cada elemento de una colección expone propiedades.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Editar propiedades en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807357"
---
# <a name="editing-properties-in-the-com-catalog"></a>Editar propiedades en el catálogo de COM+

Cada elemento de una colección expone propiedades. Estas propiedades sirven para almacenar los datos de configuración para cualquier elemento que represente el elemento. En la herramienta administrativa Servicios de componentes, estas propiedades aparecen en una página de propiedades a la que se tiene acceso haciendo clic con el botón secundario en un elemento de una carpeta.

Dado que todos los elementos de una colección determinada representan el mismo tipo de elemento, esos elementos exponen un conjunto de propiedades que es coherente en toda la colección. Por ejemplo, la colección de [**aplicaciones**](applications.md) expone una propiedad Name, una propiedad AppID, etc. Esto es análogo a la forma en que cada aplicación de la herramienta administrativa Servicios de componentes tiene una página de propiedades estructurada coherente. Para obtener una lista de las propiedades disponibles para la colección de **aplicaciones** , vea **aplicaciones**. Para obtener una lista de las propiedades disponibles para la colección de [**componentes**](components.md) , vea **componentes**.

Para obtener una lista completa de las propiedades expuestas por los elementos de cada colección, consulte [colecciones de administración de com+](com--administration-collections.md).

Un elemento de una colección se representa mediante un objeto creado a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) . Este objeto le permite establecer y obtener cualquiera de las propiedades expuestas por el elemento. Al establecer las propiedades, también es posible que esté intentando usar otro escritor en el catálogo de COM+. Para obtener más información, vea [obtener y establecer propiedades](getting-and-setting-properties.md).

Una vez que haya establecido las propiedades, no se confirmarán realmente los cambios hasta que guarde los cambios explícitamente. Para obtener más información, consulte [Guardar o descartar cambios](saving-or-discarding-changes.md).

Cuando se guardan los cambios, el catálogo de COM+ exige cierta lógica de configuración para asegurarse de que no se establece nada en configuraciones incompatibles. También cambia algunas propiedades cuando se cambian explícitamente ciertas otras propiedades. Para obtener más información, vea [interdependencias entre propiedades](interdependencies-between-properties.md).

Además, COM+ tiene una utilidad que permite realizar consultas de forma dinámica para ver qué propiedades están disponibles para los elementos de una colección determinada. Para obtener más información, consulte [consultar las propiedades disponibles](querying-for-available-properties.md).

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

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



