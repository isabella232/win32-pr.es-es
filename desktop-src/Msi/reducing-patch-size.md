---
description: A partir de Windows Installer versión 3.0, los autores de revisiones pueden usar la línea base del producto almacenada en caché por el instalador para dar servicio más fácilmente a las aplicaciones con revisiones diferenciales más pequeñas.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Reducción del tamaño de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9024307ecb0971b02c93036dd0de2aefbe797dcf5645f0f07045c4df8956a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534094"
---
# <a name="reducing-patch-size"></a>Reducción del tamaño de revisión

A partir de Windows Installer versión 3.0, los autores de revisiones pueden usar la línea base del producto almacenada en caché por el instalador para dar servicio más fácilmente a las aplicaciones con revisiones diferenciales más pequeñas. En muchos casos, una revisión [*diferencial*](d-gly.md) que entrega información de mantenimiento a una aplicación puede ser significativamente menor que una revisión de archivo completo o un paquete de instalación que entrega la misma información.

**Windows Installer 2.0:** No se admite. A partir Windows Installer 3.0, el instalador guarda selectivamente información de línea base sobre los archivos cuando se actualizan.

Windows El instalador proporciona tres métodos para actualizar y atender [aplicaciones:](small-updates.md)actualizaciones pequeñas, actualizaciones [secundarias](minor-upgrades.md)y [actualizaciones principales.](major-upgrades.md) Una actualización pequeña también se conoce como actualización de ingeniería de corrección rápida (QFE), y una actualización secundaria también se conoce como actualización de Service Pack (SP). Una actualización principal típica quita una aplicación anterior e instala una nueva aplicación. Windows El instalador puede entregar información de mantenimiento [a](patch-packages.md) las aplicaciones como un paquete de instalación [(.msi](installation-package.md) archivo) o como un paquete de revisión (archivo .msp).

Un paquete de revisión del instalador de Windows que proporciona información de mantenimiento para una actualización pequeña o una actualización secundaria suele ser mucho menor que el paquete de instalación equivalente que proporciona la misma información de mantenimiento. Se recomienda usar paquetes de revisión para la distribución de actualizaciones pequeñas y secundarias. Se recomienda usar un paquete de instalación para la distribución de una actualización principal.

Windows Las revisiones del instalador (archivos .msp) se pueden generar a partir de archivos completos o a partir de diferencias de archivo (también denominadas diferencias de archivo). Una Windows installer generada a partir de diferencias de archivo puede ser mucho menor que la revisión de archivo completo equivalente. Todas las versiones del instalador Windows pueden usar revisiones de archivos completos o revisiones diferenciales.

A partir Windows installer versión 3.0, el instalador guarda selectivamente la información de línea base sobre los archivos cuando se actualizan. La información sobre la aplicación base original (la versión RTM) y la actualización secundaria más reciente (Service Pack) se guardan en una ubicación privada cuando la aplicación está instalada o recibe una actualización secundaria.

El instalador hace lo siguiente para minimizar el tamaño de la memoria caché de línea base:

-   No se mantienen más de dos líneas base para cada aplicación: una línea base del archivo tal como se publicó originalmente (RTM) y una línea base del archivo en la actualización secundaria más reciente (Service Pack).
-   Un archivo no se agrega a la memoria caché hasta que se revisiones. La memoria caché de línea base es de copia en escritura.
-   Si la aplicación nunca se ha actualizado, no hay ningún archivo en la caché de línea base.
-   Cuando el último servicio de la aplicación fue una actualización secundaria (Service Pack), la aplicación está en un nivel de línea base y, como máximo, pueden estar presentes dos copias de un archivo en el equipo. Una copia del archivo está en el directorio de destino de la instalación. La otra copia puede estar en la memoria caché de línea base de RTM.
-   Cuando el último servicio de la aplicación fue una actualización pequeña (QFE), la aplicación no está en un nivel de línea base y, como máximo, tres copias de un archivo pueden estar presentes en el equipo. La primera copia del archivo se encuentra en el directorio de destino de la instalación. La segunda copia del archivo se encuentra en la memoria caché de línea base rtm. La última copia del archivo se encuentra en la caché de línea base más reciente.
-   La memoria caché de línea base de la aplicación se quita cuando se desinstala el producto.

A partir Windows installer versión 3.0, el instalador puede usar la caché de línea base cuando se aplican revisiones a la aplicación. La información de línea base se puede usar para aplicar una revisión diferencial o para revertir un archivo a una versión anterior durante una desinstalación de revisiones. Esto puede permitir que los autores de revisiones se beneficien de revisiones diferenciales más pequeñas. Si el instalador encuentra que la revisión diferencial no se puede aplicar al archivo de destino, el instalador puede intentar usar un archivo guardado en la caché de línea base como punto de partida. El instalador solo tiene que solicitar el origen de instalación original después de probar todas las posibilidades de la memoria caché.

El cumplimiento de las siguientes directrices puede ayudar a los autores de revisiones a usar las revisiones de Windows Installer versión 3.0 y la memoria caché de línea de base para crear revisiones diferenciales más pequeñas:

-   Cree revisiones que incluyan la [tabla MsiPatchSequence](msipatchsequence-table.md). Esta tabla es necesaria para usar la caché de línea base y está disponible a partir de Windows Installer versión 3.0.
-   No establezca una directiva que impida el almacenamiento en caché de línea base. El valor de la [directiva MaxPatchCacheSize](maxpatchcachesize.md) especifica el porcentaje máximo de espacio en disco que se puede usar. Si la directiva MaxPatchCacheSize está establecida en 0, no se guardarán archivos adicionales en la memoria caché de línea de base. Si no se establece la directiva, el valor predeterminado es que se puede usar un máximo del 10 % del espacio en disco. Si el tamaño total de la memoria caché alcanza el porcentaje máximo de espacio en disco, no se guardan archivos adicionales. La directiva no afecta a los archivos que ya se han guardado. Incluso cuando el almacenamiento en caché está deshabilitado, el instalador puede usar cachés de línea base de producto existentes.
-   Si la primera revisión aplicada incluye la [tabla MsiPatchSequence](msipatchsequence-table.md), el almacenamiento en caché está habilitado para la aplicación.
-   Si alguna revisión de la transacción de mantenimiento no incluye la tabla [MsiPatchSequence](msipatchsequence-table.md), el almacenamiento en caché solo se habilita para la aplicación si una revisión de actualización secundaria (Service Pack) que incluye la tabla MsiPatchSequence se aplica correctamente al producto.
-   Genere el paquete de revisión mediante herramientas de creación de [ revisiones, comoMsimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md).
-   Siempre debe tener como destino revisiones para la versión RTM de la aplicación o una versión de actualización secundaria (Service Pack) de la aplicación. Los destinos especificados en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md) del archivo properties de creación de revisiones (PATCH) deben ser puntos de comprobación de producto definidos por los tres primeros campos de la [**propiedad ProductVersion.**](productversion.md)
-   Nunca tiene como destino revisiones en imágenes de actualización pequeñas. Los destinos para compilar la revisión no deben incluir imágenes de actualización pequeñas anteriores.

 

 



