---
description: Dado que un paquete de instalación puede contener los archivos que componen una aplicación, así como la información necesaria para su instalación, se puede usar Windows Installer para actualizar la aplicación.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Revisiones y actualizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cee185461ac14c8eac336a5af0c1315eb5e027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002014"
---
# <a name="patching-and-upgrades"></a>Revisiones y actualizaciones

Dado que un paquete de instalación puede contener los archivos que componen una aplicación, así como la información necesaria para su instalación, se puede usar Windows Installer para actualizar la aplicación. El instalador puede actualizar la información de las siguientes partes del paquete de instalación:

-   El archivo. msi.
-   Archivos de la aplicación.
-   La información de registro de Windows Installer.

El tipo de actualización se puede caracterizar por los cambios que realiza la actualización en el código de producto, la versión del producto y el código del paquete de la aplicación. La versión del producto de la aplicación se almacena en la propiedad [**ProductVersion**](productversion.md) . El código de producto de la aplicación se almacena en la propiedad [**ProductCode**](productcode.md) . El código de [paquete](package-codes.md) de la aplicación se almacena en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) .

Se requiere una actualización que cambie la aplicación a otro producto para cambiar el [**ProductCode**](productcode.md) de la aplicación. Para obtener más información sobre las actualizaciones que requieren el cambio de **ProductCode** , consulte [cambiar el código de producto](changing-the-product-code.md). La actualización puede cambiar el [**ProductVersion**](productversion.md) y dejar el **ProductCode** sin cambios si las versiones futuras de la aplicación deben diferenciar entre las versiones actualizadas y no actualizadas del producto actual. El [código de paquete](package-codes.md) identifica de forma única el paquete de instalación y siempre debe cambiarse siempre que Update o upgrade cambie cualquier información en el paquete de instalación.

A la hora de decidir si desea cambiar la versión del producto, debe tener en cuenta si las versiones futuras de la aplicación deberán diferenciar entre las versiones actualizadas y no actualizadas del producto actual. Para garantizar la diferenciación en el futuro, se debe usar una [actualización secundaria](minor-upgrades.md) en lugar de una [pequeña](small-updates.md).

-   Si una actualización cambia el archivo. msi y los archivos de aplicación, pero no cambia la propiedad [**ProductCode**](productcode.md) o la propiedad [**ProductVersion**](productversion.md) , se denomina una [actualización pequeña](small-updates.md).
-   Si la actualización cambia el [**ProductVersion**](productversion.md), pero no cambia el [**ProductCode**](productcode.md), se denomina una [actualización menor](minor-upgrades.md).
-   Si la actualización cambia la instalación a un producto completamente distinto, el [**ProductCode**](productcode.md) debe cambiar y la actualización se denomina una [actualización principal](major-upgrades.md).

> [!Note]  
> Para garantizar la diferenciación de las versiones del producto actual en el futuro, se debe usar una [actualización mínima](minor-upgrades.md) en lugar de una [pequeña](small-updates.md).

 

En la tabla siguiente se resumen los distintos tipos de actualizaciones.



| Tipo de actualización                       | ProductCode | ProductVersion | Descripción                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Actualización pequeña](small-updates.md)    | Sin cambios   | Sin cambios      | Una actualización para uno o dos archivos que es demasiado pequeña para garantizar el cambio de [**ProductVersion**](productversion.md). El código de paquete de la propiedad de [**Resumen número de revisión**](revision-number-summary.md) cambia. Se puede enviar como un paquete de instalación completa o como un [paquete de revisión](patch-packages.md). |
| [Actualización secundaria](minor-upgrades.md)  | Sin cambios   | Cambiado        | Una actualización pequeña que realiza cambios lo suficientemente significativa como para garantizar el cambio de la propiedad [**ProductVersion**](productversion.md) . Se puede enviar como un paquete de instalación completa o como un [paquete de revisión](patch-packages.md).                                                                                                |
| [Actualizaciones principales](major-upgrades.md) | Cambiado     | Cambiado        | Una actualización completa del producto que garantiza un cambio en la propiedad [**ProductCode**](productcode.md) . Se distribuye como un [paquete de revisión](patch-packages.md) o como un paquete de instalación de producto completo.                                                                                                             |



 

> [!Note]  
> El Windows Installer puede instalar una aplicación, o una actualización, para todos los usuarios de un equipo (contexto por equipo) o para un usuario determinado (contexto por usuario) en función de los privilegios de acceso del usuario, el valor de la propiedad [**AllUsers**](allusers.md) y la versión del sistema operativo. Los desarrolladores de aplicaciones deben tener en cuenta en qué actualizaciones de contexto se instalarán. Si los contextos de la aplicación y la actualización son diferentes, puede que la aplicación no se actualice según lo esperado.

 

Los usuarios pueden actualizar a una aplicación reinstalando un paquete de Windows Installer para la aplicación. Tenga en cuenta que las actualizaciones [secundarias](minor-upgrades.md) se pueden aplicar de la misma manera que [las pequeñas](small-updates.md). Para obtener más información sobre la actualización de una aplicación mediante la reinstalación de la aplicación, consulte estas secciones:

-   [Aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)
-   [Aplicar las actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md)

Una actualización de una aplicación se puede proporcionar a los usuarios como un paquete de revisión de Windows Installer. Una revisión puede contener un archivo completo o solo los bits de archivo necesarios para actualizar parte de un archivo. Esto significa que el usuario puede descargar una revisión de actualización que es mucho menor que todo el producto y que conserva las personalizaciones del usuario a través de la actualización. Tenga en cuenta que las actualizaciones [secundarias](minor-upgrades.md) se pueden aplicar de la misma manera que [las pequeñas](small-updates.md). Para obtener más información sobre la actualización de una aplicación mediante una revisión, consulte estas secciones:

-   [Revisiones](patching.md)
-   [Crear una revisión de actualización pequeña](creating-a-small-update-patch.md)
-   [Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
-   [Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



