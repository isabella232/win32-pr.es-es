---
description: En las secciones siguientes se muestra un ejemplo de la creación de un paquete de actualización para la aplicación que se describe en un ejemplo de instalación.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Un ejemplo de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667045"
---
# <a name="an-upgrade-example"></a>Un ejemplo de actualización

En las secciones siguientes se muestra un ejemplo de la creación de un paquete de actualización para la aplicación que se describe en [un ejemplo de instalación](an-installation-example.md). Un ejemplo de una interfaz de usuario mínima para este ejemplo se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) como Uisample.msi de archivos. Si tiene el SDK de, tendrá acceso a todas las herramientas y los datos necesarios para reproducir el paquete de instalación de ejemplo, la interfaz de usuario y el paquete de actualización de ejemplo.

En este ejemplo se muestra cómo crear un paquete de Windows Installer que actualiza el MNP2000 de producto hipotético a un nuevo producto denominado MNP2001. El paquete de actualización de ejemplo aplica una actualización principal al producto que requiere cambiar el código de producto. Para obtener más información acerca de las actualizaciones principales, consulte el tema sobre las [actualizaciones principales](major-upgrades.md) en la sección [revisiones y actualizaciones](patching-and-upgrades.md) .

El paquete de actualización de ejemplo tiene las siguientes especificaciones:

-   Para calificar la recepción de esta actualización a MNP2001, un usuario debe haber instalado previamente las versiones 1,0 a 1,4 (incluido) del idioma inglés MNP2000 mediante Windows Installer.
-   Cuando un usuario intenta instalar el paquete de actualización, la funcionalidad de actualización de Windows Installer busca en el equipo del usuario los productos que son aptos para la actualización.
-   Windows Installer migra la configuración de las características del producto original al producto actualizado.
-   El instalador quita todas las características obsoletas del equipo del usuario.
-   El instalador instala todas las características nuevas que pertenecen a la actualización.
-   Una desinstalación del paquete de actualización quita el producto del equipo del usuario y no restaura la versión anterior del producto.
-   En el ejemplo se actualizan los accesos directos a nuevos archivos y características.

    [Planeación de una actualización importante](planning-a-major-upgrade.md)

    [Importar la base de datos de instalación original](importing-original-installation-database.md)

    [Actualización de la estructura de directorios para una actualización](updating-directory-structure-for-an-upgrade.md)

    [Actualizar archivos y atributos de archivo para una actualización](updating-files-and-file-attributes-for-an-upgrade.md)

    [Actualización de componentes para una actualización](updating-components-for-an-upgrade.md)

    [Actualizar características para una actualización](updating-features-for-an-upgrade.md)

    [Actualización de accesos directos para una actualización](updating-shortcuts-for-an-upgrade.md)

    [Actualizando la tabla de actualización para una actualización](updating-upgrade-table-for-an-upgrade.md)

    [Actualizar las propiedades de una actualización](updating-properties-for-an-upgrade.md)

    [Actualización de tablas de secuencia para una actualización](updating-sequence-tables-for-an-upgrade.md)

    [Actualización de la información de Resumen de una actualización](updating-summary-information-for-an-upgrade.md)

    [Validar una actualización de instalación](validating-an-installation-upgrade.md)

 

 



