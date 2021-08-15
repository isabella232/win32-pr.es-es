---
description: El código de producto es un GUID que es la identificación principal de una aplicación o producto. Consulte Códigos de producto.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Cambiar el código del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4567cbb014fa2f2002f0433a8e42c3a261ccb1af350f9b4e592a3bb5ff8a0216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340015"
---
# <a name="changing-the-product-code"></a>Cambiar el código del producto

El código de producto es un GUID que es la identificación principal de una aplicación o producto. Vea [Códigos de producto](product-codes.md).

Por lo general, una actualización que cumpla las siguientes directrices no requiere un cambio del código de producto y se puede controlar como una actualización pequeña [o](small-updates.md)si la versión va a cambiar, como una actualización [secundaria](minor-upgrades.md):

-   La actualización puede ampliar o reducir el árbol de componentes de características, pero no debe reorganizar la jerarquía existente de características y componentes descrita por las tablas [Feature](feature-table.md) [y FeatureComponents.](featurecomponents-table.md) Puede agregar una nueva característica al árbol de componentes de características existente. Si quita una característica primaria, también debe quitar todas las características secundarias de la característica quitada.
-   La actualización puede agregar un nuevo componente a una característica nueva o existente.
-   La actualización no debe cambiar el código de componente de ningún componente. Por lo tanto, una actualización pequeña o una actualización secundaria nunca debe cambiar el nombre del archivo de clave de un componente, ya que esto requeriría cambiar el código del componente.
-   La actualización no debe cambiar el nombre del archivo .msi del paquete de instalación. En su lugar, dado que modifica el paquete, debe cambiar el código del paquete. Tenga en cuenta que esto significa que la actualización puede cambiar las tablas, las acciones personalizadas y los diálogos del archivo .msi sin cambiar el nombre del archivo.
-   La actualización puede agregar, quitar o modificar los archivos, las claves del Registro o los accesos directos de componentes que no comparten dos o más características. Si la actualización modifica un archivo con versión, la versión de ese archivo debe incrementarse en la [tabla File](file-table.md). Si la actualización quita recursos, también debe actualizar las tablas [RemoveFile](removefile-table.md) y [RemoveRegistry](removeregistry-table.md) para quitar los archivos, las claves del Registro o los accesos directos no usados que ya se hayan instalado.
-   La actualización de un componente compartido por dos o más características debe ser compatible con versiones anteriores con todas las aplicaciones y características que usan el componente. La actualización puede modificar el recurso de un componente compartido, como archivos, entradas del Registro y accesos directos, siempre que los cambios sean compatibles con versiones anteriores. No se recomienda que la actualización agregue o quite archivos, entradas del Registro o accesos directos de un componente compartido.
-   Una pequeña actualización se envía como un paquete de Windows de [revisión del instalador](patch-packages.md). (Normalmente, un CD-ROM de producto completo no se proporciona con una pequeña actualización).

El código del producto debe cambiarse si se cumple alguna de las condiciones siguientes para la actualización:

-   Deben ser posibles instalaciones coexistir de productos originales y actualizados en el mismo sistema.
-   Se ha cambiado el nombre .msi archivo.
-   El código de componente de un componente existente ha cambiado.
-   Se quita un componente de una característica existente.
-   Una característica existente se ha convertido en un elemento secundario de una característica existente.
-   Se ha quitado una característica secundaria existente de su característica primaria.

Tenga en cuenta que agregar una nueva característica secundaria, que consta completamente de componentes nuevos, a una característica existente no requiere cambiar el código del producto.

Se pueden crear nuevas características secundarias incluyendo msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent en el campo Atributos de la [tabla Característica](feature-table.md). Si la actualización secundaria solo agrega nuevas características secundarias, REINSTALL=ALL es suficiente para forzar la instalación de las nuevas características secundarias. Para obtener más información, vea [Controlar los estados de selección de características](controlling-feature-selection-states.md).

Una nueva característica secundaria puede estar oculta al usuario. Para sincronizar el estado de instalación de una nueva característica secundaria con su característica primaria, establezca los bits msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para la característica secundaria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedad](property-reference.md)
</dt> </dl>

 

 



