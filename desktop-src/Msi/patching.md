---
description: En estas secciones se describe la aplicación de revisiones a Windows instalación del instalador.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Aplicación de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb90436c2a33495aaa818d0796c5d749e5d76286db4dbdc247ec4ee58c7ea6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926245"
---
# <a name="patching"></a>Aplicación de revisiones

Una aplicación que se ha instalado mediante microsoft Windows Installer se puede actualizar reinstalando un paquete de instalación actualizado (archivo .msi) o aplicando una revisión del instalador de Windows (un archivo .msp) a la aplicación.

Una Windows installer (archivo .msp) es un paquete independiente que contiene las actualizaciones de la aplicación y describe qué versiones de la aplicación pueden recibir la revisión. Las revisiones contienen como mínimo dos transformaciones de base de datos y pueden contener archivos de revisión que se almacenan en el flujo de archivos de archivado del paquete de revisión. Para obtener más información sobre las partes de un paquete de revisión Windows Installer, vea [Paquetes de revisión](patch-packages.md).

El mantenimiento de aplicaciones mediante la entrega de una Windows installer, en lugar de un paquete de instalación completo para el producto actualizado puede tener ventajas. Una revisión puede contener un archivo completo o solo los bits de archivo necesarios para actualizar parte del archivo. Esto puede permitir que el usuario descargue una revisión de actualización mucho menor que el paquete de instalación para todo el producto. Una actualización mediante una revisión puede conservar una personalización de usuario de la aplicación a través de la actualización.

**Windows Installer 4.5 y versiones posteriores: **

A partir de Windows Installer 4.5, los desarrolladores pueden marcar componentes en una revisión con el valor **msidbComponentAttributesUninstallOnSupersedence** de la [tabla Component](component-table.md). Si se instala una revisión posterior, marcada con el valor **msidbPatchSequenceSupersedeEarlier** en su [tabla MsiPatchSequence](msipatchsequence-table.md) para reemplazar la primera revisión, Windows Installer 4.5 y versiones posteriores pueden anular el registro y desinstalar los componentes **marcados como msidbComponentAttributesUninstallOnSupersedence** para evitar que se quepan los componentes no usados en el equipo. Si el componente no está marcado con con este bit, la instalación de la revisión superseding puede dejar un componente no utilizado en el equipo. Establecer la **propiedad MSIUNINSTALLSUPERSEDEDCOMPONENTS** tiene el mismo efecto que establecer este bit para todos los componentes.

**Windows Installer 3.0 y versiones posteriores: **

Los desarrolladores que usan Windows Installer 3.0 y crean paquetes de revisión que tienen la tabla [MsiPatchSequence](msipatchsequence-table.md) pueden crear paquetes de revisión que hagan lo siguiente:

-   Use la línea de base del producto almacenada en caché por el instalador para dar servicio más fácilmente a las aplicaciones con revisiones diferenciales más pequeñas. Para obtener más información sobre el uso de la línea de base del producto, vea [Reducción del tamaño de revisión.](reducing-patch-size.md)
-   Omita las acciones asociadas a tablas específicas que la revisión no ha modificar. Esto puede reducir significativamente el tiempo necesario para instalar la revisión. Para obtener más información sobre qué tablas se pueden omitir, vea [Optimización de revisiones.](patch-optimization.md)
-   Cree e instale revisiones que se puedan desinstalar por sí solos y en cualquier orden, sin tener que desinstalar y reinstalar toda la aplicación y otras revisiones. Para obtener más información sobre cómo desinstalar revisiones, vea [Quitar revisiones.](removing-patches.md)
-   Aplique revisiones en un orden constante independientemente del orden en que se proporcionan las revisiones al sistema. Para obtener más información sobre cómo el Windows determina la secuencia que se usa para aplicar revisiones, vea [Secuenciar revisiones.](sequencing-patches.md)
-   Aplique revisiones a una aplicación que se haya instalado en un contexto administrado por usuario. Para más información, consulte [Aplicación de revisiones Per-User aplicaciones administradas.](patching-per-user-managed-applications.md)

**Windows Installer 2.0: **

No se admite la tabla [MsiPatchSequence.](msipatchsequence-table.md) A partir de Windows Installer 3.0, los paquetes de revisión pueden contener información que describe la secuencia de aplicación de revisiones para la revisión en relación con otras actualizaciones e información descriptiva adicional.

El método recomendado para crear un paquete de revisión es usar herramientas de creación de revisiones [ comoMsimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md). Los desarrolladores pueden generar un archivo de creación de revisiones como se describe en la sección: [Creación de un paquete de revisión.](creating-a-patch-package.md) La creación de una revisión de actualización pequeña se describe en la sección: [A Small Update Patching Example](a-small-update-patching-example.md).

Microsoft Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una revisión. Para obtener más información sobre cómo instalar una revisión ubicada en un servidor web, vea Descargar e instalar una [revisión desde Internet.](downloading-and-installing-a-patch-from-the-internet.md)

Se puede Windows aplicación única del instalador (archivo .msp) al paquete de instalación al instalar una aplicación por primera vez. Para obtener más información, vea [Aplicar revisiones a las instalaciones iniciales.](patching-initial-installations.md)

No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original. Sin embargo, para minimizar la posibilidad de que la revisión requiera acceso al origen original, siga los puntos enumerados en la sección siguiente: Impedir que una revisión requiera acceso al origen de [instalación original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Para minimizar la posibilidad de que la revisión no se rompa con una transformación de personalización posterior, normalmente la revisión se instala primero, seguida de la personalización. La instalación de transformaciones de personalización en primer lugar y, a continuación, la revisión, pueden interrumpir la personalización. Para obtener más información sobre la aplicación de revisiones a aplicaciones personalizadas, vea [Aplicación de revisiones a aplicaciones personalizadas.](patching-customized-applications.md)

 

 



