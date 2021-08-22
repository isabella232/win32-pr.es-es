---
description: Cada elemento de una colección expone propiedades.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Edición de propiedades en el catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ace2809fef4510a9c89b5faf31df555cb76426a06dd445aff9438c0d19e887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546248"
---
# <a name="editing-properties-in-the-com-catalog"></a>Edición de propiedades en el catálogo de COM+

Cada elemento de una colección expone propiedades. Estas propiedades sirven para contener datos de configuración para cualquier elemento que represente el elemento. En la herramienta administrativa Servicios de componentes, estas propiedades aparecen en una página de propiedades a la que se accede haciendo clic con el botón derecho en un elemento de una carpeta.

Dado que todos los elementos de una colección determinada representan el mismo tipo de cosas, esos elementos exponen un conjunto de propiedades coherentes en toda la colección. Por ejemplo, la [**colección Applications**](applications.md) expone una propiedad Name, una propiedad AppID, etc. Esto es análogo a cómo cada aplicación de la herramienta administrativa Servicios de componentes tiene una página de propiedades estructurada de forma coherente disponible para ella. Para obtener una lista de las propiedades disponibles para **la colección Aplicaciones,** vea **Aplicaciones**. Para obtener una lista de las propiedades disponibles para [**la colección Components,**](components.md) vea **Components**.

Para obtener una lista completa de las propiedades expuestas por los elementos de cada colección, vea [Colecciones de administración de COM+.](com--administration-collections.md)

Un elemento de una colección se representa mediante un objeto creado a partir de la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md) Este objeto permite establecer y obtener cualquiera de las propiedades expuestas por el elemento. Al establecer propiedades, también es posible que esté conteniendo con otro escritor en el catálogo de COM+. Para obtener más información, vea [Getting and Setting Properties](getting-and-setting-properties.md).

Una vez establecidas las propiedades, no se confirma ningún cambio hasta que se guarden explícitamente los cambios. Para obtener más información, vea [Guardar o descartar cambios.](saving-or-discarding-changes.md)

Al guardar los cambios, el catálogo de COM+ aplica alguna lógica de configuración para asegurarse de que no se establecen las cosas en configuraciones incompatibles. También cambia algunas propiedades automáticamente cuando se cambian explícitamente otras propiedades. Para obtener más información, vea [Interdependencies Between Properties](interdependencies-between-properties.md).

Además, COM+ tiene una instalación que le permite consultar dinámicamente para ver qué propiedades están disponibles para los elementos de una colección determinada. Para obtener más información, [vea Consulta de propiedades disponibles.](querying-for-available-properties.md)

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

[Recuperar colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



