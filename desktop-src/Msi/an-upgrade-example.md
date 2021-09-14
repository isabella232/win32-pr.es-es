---
description: En las secciones siguientes se presenta un ejemplo de creación de un paquete de actualización para la aplicación que se describe en Un ejemplo de instalación.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Ejemplo de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159136"
---
# <a name="an-upgrade-example"></a>Ejemplo de actualización

En las secciones siguientes se muestra un ejemplo de creación de un paquete de actualización para la aplicación que se describe en [Un ejemplo de instalación](an-installation-example.md). Se proporciona un ejemplo de una interfaz de usuario mínima para este ejemplo en Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) como el archivo Uisample.msi. Si tiene el SDK, tiene acceso a todas las herramientas y datos necesarios para reproducir el paquete de instalación de ejemplo, la interfaz de usuario y el paquete de actualización de ejemplo.

En este ejemplo se muestra cómo crear un paquete Windows Installer que actualiza el producto hipotético MNP2000 a un nuevo producto denominado MNP2001. El paquete de actualización de ejemplo aplica una actualización principal al producto que requiere cambiar el código del producto. Para obtener más información sobre las actualizaciones principales, vea el tema actualizaciones [principales](major-upgrades.md) en la sección Revisiones [y actualizaciones.](patching-and-upgrades.md)

El paquete de actualización de ejemplo tiene las siguientes especificaciones:

-   Para recibir esta actualización a MNP2001, un usuario debe haber instalado previamente las versiones 1.0 a 1.4 (inclusive) del idioma inglés MNP2000 mediante Windows Installer.
-   Cuando un usuario intenta instalar el paquete de actualización, la funcionalidad de actualización de Windows Installer busca en el equipo del usuario los productos que son aptos para la actualización.
-   Windows El instalador migra toda la configuración de características del producto original al producto actualizado.
-   El instalador quita todas las características obsoletas del equipo del usuario.
-   El instalador instala todas las características nuevas que pertenecen a la actualización.
-   Una desinstalación del paquete de actualización quita el producto del equipo del usuario y no restaura la versión anterior del producto.
-   La actualización de ejemplo actualiza los accesos directos a nuevos archivos y características.

    [Planear una actualización principal](planning-a-major-upgrade.md)

    [Importar la base de datos de instalación original](importing-original-installation-database.md)

    [Actualizar la estructura de directorios para una actualización](updating-directory-structure-for-an-upgrade.md)

    [Actualizar archivos y atributos de archivo para una actualización](updating-files-and-file-attributes-for-an-upgrade.md)

    [Actualizar componentes para una actualización](updating-components-for-an-upgrade.md)

    [Actualizar características para una actualización](updating-features-for-an-upgrade.md)

    [Actualizar accesos directos para una actualización](updating-shortcuts-for-an-upgrade.md)

    [Actualizar la tabla de actualización para una actualización](updating-upgrade-table-for-an-upgrade.md)

    [Actualizar las propiedades de una actualización](updating-properties-for-an-upgrade.md)

    [Actualizar tablas de secuencia para una actualización](updating-sequence-tables-for-an-upgrade.md)

    [Actualizar la información de resumen de una actualización](updating-summary-information-for-an-upgrade.md)

    [Validación de una actualización de instalación](validating-an-installation-upgrade.md)

 

 



