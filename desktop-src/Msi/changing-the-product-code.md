---
description: El código de producto es un GUID que es la identificación principal de una aplicación o producto. Consulte códigos de producto.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Cambiar el código de producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082542"
---
# <a name="changing-the-product-code"></a>Cambiar el código de producto

El código de producto es un GUID que es la identificación principal de una aplicación o producto. Consulte [códigos de producto](product-codes.md).

Una actualización que cumpla las siguientes directrices generalmente no requiere un cambio en el código de producto y se puede controlar como una [actualización pequeña](small-updates.md), o bien, si la versión va a cambiar, como una [actualización secundaria](minor-upgrades.md):

-   La actualización puede aumentar o reducir el árbol de componentes de características, pero no debe reorganizar la jerarquía existente de características y componentes descritos en las [tablas de características y](feature-table.md) [FeatureComponents](featurecomponents-table.md) . Puede Agregar una nueva característica al árbol de componentes de característica existente. Si quita una característica primaria, también debe quitar todas las características secundarias de la característica quitada.
-   La actualización puede Agregar un nuevo componente a una característica nueva o existente.
-   La actualización no debe cambiar el código de componente de ningún componente. Por lo tanto, una pequeña actualización o actualización secundaria nunca debe cambiar el nombre del archivo de clave de un componente, ya que esto requeriría cambiar el código del componente.
-   La actualización no debe cambiar el nombre del archivo. msi del paquete de instalación. En su lugar, dado que modifica el paquete, debe cambiar el código de paquete. Tenga en cuenta que esto significa que la actualización puede cambiar las tablas, las acciones personalizadas y los cuadros de diálogo del archivo. msi sin cambiar el nombre del archivo.
-   La actualización puede Agregar, quitar o modificar los archivos, las claves del registro o los métodos abreviados de componentes que no comparten dos o más características. Si la actualización modifica un archivo con versión, la versión de ese archivo se debe incrementar en la [tabla de archivos](file-table.md). Si la actualización quita recursos, también debe actualizar las tablas [RemoveFile](removefile-table.md) y [RemoveRegistry](removeregistry-table.md) para quitar los archivos no usados, las claves del registro o los accesos directos que ya se han instalado.
-   La actualización de un componente compartido por dos o más características debe ser compatible con versiones anteriores de todas las aplicaciones y características que usan el componente. La actualización puede modificar el recurso de un componente compartido, como archivos, entradas del registro y accesos directos, siempre y cuando los cambios sean compatibles con versiones anteriores. No se recomienda que actualice agregar o quitar archivos, entradas del registro o accesos directos de un componente compartido.
-   Se incluye una actualización pequeña como un [paquete de revisión](patch-packages.md)de Windows Installer. (Un CD-ROM completo del producto no se proporciona normalmente con una actualización pequeña).

El código de producto debe cambiarse si se cumple alguna de las siguientes condiciones para la actualización:

-   Las instalaciones coexistentes de productos originales y actualizados en el mismo sistema deben ser posibles.
-   Se ha cambiado el nombre del archivo. msi.
-   El código de componente de un componente existente ha cambiado.
-   Un componente se quita de una característica existente.
-   Una característica existente se ha convertido en un elemento secundario de una característica existente.
-   Una característica secundaria existente se ha quitado de su característica primaria.

Tenga en cuenta que la adición de una nueva característica secundaria, que consta exclusivamente de nuevos componentes, a una característica existente no requiere cambiar el código de producto.

Se pueden crear nuevas características secundarias incluyendo msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent en el campo atributos de la [tabla de características](feature-table.md). Si la actualización secundaria solo agrega nuevas características secundarias, REINSTALL = ALL es suficiente para forzar la instalación de las nuevas características secundarias. Para obtener más información, consulte [controlar los Estados de selección de características](controlling-feature-selection-states.md).

Una nueva característica secundaria puede estar oculta para el usuario. Para sincronizar el estado de instalación de una nueva característica secundaria con su característica primaria, establezca los bits msidbFeatureAttributesFollowParent y msidbFeatureAttributesUIDisallowAbsent para la característica secundaria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 



