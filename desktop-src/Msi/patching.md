---
description: En estas secciones se describe la revisión de una instalación de Windows Installer.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Aplicación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3117723bda1699eeae341fc75db201421f6ae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669843"
---
# <a name="patching"></a>Aplicación de revisiones

Una aplicación que se ha instalado mediante el Microsoft Windows Installer se puede actualizar reinstalando un paquete de instalación actualizado (archivo. msi) o aplicando una revisión de Windows Installer (un archivo. msp) a la aplicación.

Una revisión de Windows Installer (archivo. msp) es un paquete independiente que contiene las actualizaciones de la aplicación y describe qué versiones de la aplicación pueden recibir la revisión. Las revisiones contienen como mínimo dos transformaciones de base de datos y pueden contener archivos de revisión que se almacenan en la secuencia de archivos. cab del paquete de revisión. Para obtener más información acerca de las partes de un paquete de revisión de Windows Installer, consulte [paquetes de revisiones](patch-packages.md).

Las aplicaciones de mantenimiento mediante la entrega de una revisión Windows Installer, en lugar de un paquete de instalación completo para el producto actualizado, pueden tener ventajas. Una revisión puede contener un archivo completo o solo los bits de archivo necesarios para actualizar parte del archivo. Esto puede permitir al usuario descargar una revisión de actualización que es mucho menor que el paquete de instalación para todo el producto. Una actualización que usa una revisión puede conservar la personalización de un usuario de la aplicación a través de la actualización.

* * Windows Installer 4,5 y versiones posteriores: * *

A partir de Windows Installer 4,5, los desarrolladores pueden marcar los componentes en una revisión con el valor **msidbComponentAttributesUninstallOnSupersedence** en la [tabla de componentes](component-table.md). Si se instala una revisión posterior, marcada con el valor **msidbPatchSequenceSupersedeEarlier** en su [tabla MsiPatchSequence](msipatchsequence-table.md) para sustituir la primera revisión, Windows Installer 4,5 y versiones posteriores pueden anular el registro y desinstalar componentes marcados como **msidbComponentAttributesUninstallOnSupersedence** para evitar que los componentes no usados se queden en el equipo. Si el componente no está marcado con este bit, la instalación de la revisión de sustitución puede dejar un componente sin usar en el equipo. Establecer la propiedad **MSIUNINSTALLSUPERSEDEDCOMPONENTS** tiene el mismo efecto que establecer este bit para todos los componentes.

* * Windows Installer 3,0 y versiones posteriores: * *

Los desarrolladores que usan Windows Installer 3,0 y los paquetes de revisión de autor que tienen la [tabla MsiPatchSequence](msipatchsequence-table.md) pueden crear paquetes de revisión que hagan lo siguiente:

-   Use la línea de base del producto almacenada en caché por el instalador para facilitar el servicio de las aplicaciones con revisiones Delta más pequeñas. Para obtener más información acerca del uso de la línea de base del producto, consulte [reducir el tamaño](reducing-patch-size.md)de la revisión.
-   Omitir acciones asociadas a tablas específicas que la revisión no modifica. Esto puede reducir significativamente el tiempo necesario para instalar la revisión. Para obtener más información sobre las tablas que se pueden omitir, vea [optimización de revisiones](patch-optimization.md).
-   Crear e instalar revisiones que se pueden desinstalar de forma individual y en cualquier orden, sin tener que desinstalar y volver a instalar toda la aplicación y otras revisiones. Para obtener más información acerca de la desinstalación de revisiones, consulte [quitar revisiones](removing-patches.md).
-   Aplique revisiones en un orden constante, independientemente del orden en el que se proporcionen las revisiones al sistema. Para obtener más información sobre cómo el Windows Installer determina la secuencia que se usa para aplicar las revisiones, consulte [secuenciación de revisiones](sequencing-patches.md).
-   Aplicar revisiones a una aplicación que se ha instalado en un contexto administrado por el usuario. Para obtener más información, consulte [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md).

* * Windows Installer 2,0: * *

No se admite la [tabla MsiPatchSequence](msipatchsequence-table.md) . A partir de Windows Installer 3,0, los paquetes de revisión pueden contener información que describe la secuencia de revisión de la revisión relativa a otras actualizaciones e información descriptiva adicional.

El método recomendado para crear un paquete de revisión es usar herramientas de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md). Los desarrolladores pueden generar un archivo de creación de revisiones como se describe en la sección [creación de un paquete de revisión](creating-a-patch-package.md). La creación de una revisión de actualización pequeña se describe en la sección: [un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md).

Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido de una revisión. Para obtener más información acerca de cómo instalar una revisión ubicada en un servidor Web, vea [Descargar e instalar una revisión desde Internet](downloading-and-installing-a-patch-from-the-internet.md).

Se puede aplicar una única revisión de Windows Installer (archivo. msp) al paquete de instalación al instalar una aplicación por primera vez. Para obtener más información, vea [aplicar revisiones a las instalaciones iniciales](patching-initial-installations.md).

No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original. Sin embargo, para minimizar la posibilidad de que la revisión requiera acceso al origen original, siga los puntos que se muestran en la sección siguiente: [evitar que una revisión requiera acceso al origen de la instalación original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Para minimizar la posibilidad de que la revisión no se interrumpa por una transformación de personalización posterior, normalmente se instala primero la revisión, seguida de la personalización. La instalación de las transformaciones de personalización primero y, a continuación, la revisión puede interrumpir la personalización. Para obtener más información acerca de la aplicación de revisiones a aplicaciones personalizadas, consulte [aplicación de revisiones a aplicaciones personalizadas](patching-customized-applications.md).

 

 



