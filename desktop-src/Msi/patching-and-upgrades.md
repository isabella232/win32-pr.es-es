---
description: Dado que un paquete de instalación puede contener los archivos que son una aplicación, así como la información necesaria para su instalación, Windows Installer se puede usar para actualizar la aplicación.
ms.assetid: da946739-9efc-4bf0-8a9a-6f6ead3c4a34
title: Aplicación de revisiones y actualizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad2b5564309e2faaa43c322da93834d4c8fe174e373b61707a853b56b097e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042415"
---
# <a name="patching-and-upgrades"></a>Aplicación de revisiones y actualizaciones

Dado que un paquete de instalación puede contener los archivos que son una aplicación, así como la información necesaria para su instalación, Windows Installer se puede usar para actualizar la aplicación. El instalador puede actualizar la información de las siguientes partes del paquete de instalación:

-   El .msi archivo.
-   Archivos de la aplicación.
-   La información Windows registro del instalador.

El tipo de actualización puede caracterizarse por los cambios que realiza la actualización en el código de producto, la versión del producto y el código del paquete de la aplicación. La versión del producto de la aplicación se almacena en la [**propiedad ProductVersion.**](productversion.md) El código de producto de la aplicación se almacena en la [**propiedad ProductCode.**](productcode.md) El código del paquete [de la aplicación](package-codes.md) se almacena en la propiedad Resumen del número de [**revisión.**](revision-number-summary.md)

Se requiere una actualización que cambie la aplicación a otro producto para cambiar el [**ProductCode**](productcode.md) de la aplicación. Para obtener más información sobre qué actualizaciones requieren cambiar **ProductCode,** [vea Cambiar el código de producto](changing-the-product-code.md). La actualización puede cambiar [**ProductVersion**](productversion.md) y dejar **ProductCode** sin cambios si las versiones futuras de la aplicación tendrán que diferenciar entre las versiones actualizadas y no actualizadas del producto actual. El [código del paquete](package-codes.md) identifica de forma única el paquete de instalación y siempre debe cambiarse siempre que la actualización o actualización cambie cualquier información del paquete de instalación.

Al decidir si se debe cambiar la versión del producto, debe tener en cuenta si las versiones futuras de la aplicación tendrán que diferenciar entre las versiones actualizadas y no actualizadas del producto actual. Para garantizar la diferenciación en [](minor-upgrades.md) el futuro, se debe usar una actualización secundaria en lugar de una [actualización pequeña](small-updates.md).

-   Si una actualización cambia el archivo .msi archivos de aplicación, pero no cambia la propiedad [**ProductCode**](productcode.md) ni [**la propiedad ProductVersion,**](productversion.md) se denomina actualización [pequeña.](small-updates.md)
-   Si la actualización cambia [**ProductVersion**](productversion.md), pero no cambia [**ProductCode**](productcode.md), se denomina actualización [secundaria.](minor-upgrades.md)
-   Si la actualización cambia la instalación a un producto completamente diferente, [**productCode**](productcode.md) debe cambiar y la actualización se denomina actualización [principal.](major-upgrades.md)

> [!Note]  
> Para garantizar la diferenciación de las versiones del [](minor-upgrades.md) producto actual en el futuro, se debe usar una actualización secundaria en lugar de una [actualización pequeña](small-updates.md).

 

En la tabla siguiente se resumen los distintos tipos de actualizaciones.



| Tipo de actualización                       | Productcode | ProductVersion | Descripción                                                                                                                                                                                                                                                                                                           |
|--------------------------------------|-------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Actualización pequeña](small-updates.md)    | Sin cambios   | Sin cambios      | Actualización de uno o dos archivos que es demasiado pequeño para garantizar el cambio [**de ProductVersion.**](productversion.md) El código del paquete de [**la propiedad Resumen del número de revisión**](revision-number-summary.md) cambia. Se puede enviar como un paquete de instalación completa o como un paquete [de revisión](patch-packages.md). |
| [Actualización secundaria](minor-upgrades.md)  | Sin cambios   | Cambiado        | Una pequeña actualización que realiza cambios lo suficientemente significativos como para garantizar el cambio de [**la propiedad ProductVersion.**](productversion.md) Se puede enviar como un paquete de instalación completa o como un paquete [de revisión](patch-packages.md).                                                                                                |
| [Actualizaciones principales](major-upgrades.md) | Cambiado     | Cambiado        | Una actualización completa del producto que garantiza un cambio en la [**propiedad ProductCode.**](productcode.md) Se incluye como un [paquete de revisión](patch-packages.md) o como un paquete de instalación de producto completo.                                                                                                             |



 

> [!Note]  
> El instalador de Windows puede instalar una aplicación, o una actualización, para todos los usuarios de un equipo (contexto por equipo) o para un usuario determinado (contexto por usuario) en función de los privilegios de acceso del usuario, el valor de la propiedad [**ALLUSERS**](allusers.md) y la versión del sistema operativo. Los desarrolladores de aplicaciones deben tener en cuenta en qué contexto se instalarán las actualizaciones. Si los contextos de la aplicación y la actualización son diferentes, es posible que la aplicación no se actualice según lo previsto.

 

Los usuarios pueden actualizar a una aplicación mediante la reinstalación de un Windows installer para la aplicación. Tenga en [cuenta que las actualizaciones secundarias](minor-upgrades.md) se pueden aplicar de la misma manera que las actualizaciones [pequeñas](small-updates.md). Para obtener más información sobre cómo actualizar una aplicación mediante la reinstalación de la aplicación, consulte estas secciones:

-   [Aplicación de actualizaciones pequeñas mediante la reinstalación del producto](applying-small-updates-by-reinstalling-the-product.md)
-   [Aplicación de actualizaciones principales mediante la instalación del producto](applying-major-upgrades-by-installing-the-product.md)

Una actualización de una aplicación se puede proporcionar a los usuarios como un paquete Windows de revisión del instalador. Una revisión puede contener un archivo completo o solo los bits de archivo necesarios para actualizar parte de un archivo. Esto significa que el usuario puede descargar una revisión de actualización mucho más pequeña que todo el producto y que conserva las personalizaciones del usuario a través de la actualización. Tenga en [cuenta que las actualizaciones secundarias](minor-upgrades.md) se pueden aplicar de la misma manera que las actualizaciones [pequeñas](small-updates.md). Para obtener más información sobre cómo actualizar una aplicación mediante una revisión, consulte estas secciones:

-   [Aplicación de revisiones](patching.md)
-   [Crear una revisión de actualización pequeña](creating-a-small-update-patch.md)
-   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
-   [Aplicación de actualizaciones principales mediante la aplicación de revisiones a la instalación local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)

 

 



