---
description: A partir de Windows Installer versión 3,0, los autores de revisiones pueden utilizar la línea de base del producto almacenada en caché por el instalador para facilitar el servicio de las aplicaciones con revisiones Delta más pequeñas.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Reducir el tamaño de la revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677764"
---
# <a name="reducing-patch-size"></a>Reducir el tamaño de la revisión

A partir de Windows Installer versión 3,0, los autores de revisiones pueden utilizar la línea de base del producto almacenada en caché por el instalador para facilitar el servicio de las aplicaciones con revisiones Delta más pequeñas. En muchos casos, una [*revisión diferencial*](d-gly.md) que proporciona información de servicio a una aplicación puede ser significativamente menor que una revisión de archivos completos o un paquete de instalación que proporciona la misma información.

**Windows Installer 2,0:** No compatible. A partir de Windows Installer 3,0, el instalador guarda selectivamente la información de línea de base de los archivos cuando se actualizan.

Windows Installer proporciona tres métodos para actualizar y dar servicio a las aplicaciones: [pequeñas actualizaciones](small-updates.md), [actualizaciones secundarias](minor-upgrades.md)y [actualizaciones importantes](major-upgrades.md). También se hace referencia a una actualización pequeña como una actualización de ingeniería de corrección rápida (QFE) y también se denomina actualización de Service Pack (SP). Una actualización importante típica quita una aplicación anterior e instala una nueva aplicación. Windows Installer puede proporcionar información de servicio a las aplicaciones como un [paquete de instalación](installation-package.md) (archivo. msi) o como un paquete de [revisión](patch-packages.md) (archivo. msp).

Un paquete de revisión de Windows Installer que proporciona información de mantenimiento para una pequeña actualización o una actualización secundaria suele ser mucho menor que el paquete de instalación equivalente que proporciona la misma información de servicio. Se recomienda usar paquetes de revisión para la distribución de actualizaciones pequeñas y secundarias. Se recomienda usar un paquete de instalación para la distribución de una actualización principal.

Las revisiones de Windows Installer (archivos. msp) pueden generarse a partir de archivos completos o de diferencias de archivo (también denominadas diferencias de archivo). Una revisión Windows Installer generada a partir de diferencias de archivo puede ser mucho menor que la revisión de archivos completos equivalente. Todas las versiones del Windows Installer pueden utilizar revisiones de archivos completos o de diferencias.

A partir de Windows Installer versión 3,0, el instalador guarda selectivamente la información de línea de base sobre los archivos cuando se actualizan. La información sobre la aplicación base original (la versión RTM) y la actualización secundaria más reciente (Service Pack) se guardan en una ubicación privada cuando la aplicación se instala o recibe una actualización secundaria.

El instalador hace lo siguiente para minimizar el tamaño de la memoria caché de línea base:

-   No se mantienen más de dos líneas base para cada aplicación: una línea base del archivo como se liberó originalmente (RTM) y una línea base del archivo en la actualización secundaria más reciente (Service Pack).
-   No se agrega un archivo a la memoria caché hasta que se revisan. La memoria caché de base de referencia es de copia en escritura.
-   Si la aplicación no se ha actualizado nunca, no habrá ningún archivo en la memoria caché de línea de base.
-   Cuando el último mantenimiento de la aplicación era una actualización secundaria (Service Pack), la aplicación se encuentra en un nivel de línea base y, como máximo, pueden estar presentes dos copias de un archivo en el equipo. Una copia del archivo se encuentra en el directorio de destino de la instalación. La otra copia puede estar en la caché de línea de base de RTM.
-   Cuando el último mantenimiento de la aplicación era una actualización pequeña (QFE), la aplicación no se encuentra en un nivel de línea base y, como máximo, pueden estar presentes tres copias de un archivo en el equipo. La primera copia del archivo se encuentra en el directorio de destino de la instalación. La segunda copia del archivo se encuentra en la caché de línea de base de RTM. La última copia del archivo se encuentra en la caché de línea de base más reciente.
-   La memoria caché de línea de base de la aplicación se quita cuando se desinstala el producto.

A partir de Windows Installer versión 3,0, el instalador puede usar la memoria caché de línea base cuando se aplican revisiones a la aplicación. La información de línea de base se puede usar para aplicar una revisión diferencial o revertir un archivo a una versión anterior durante la desinstalación de una revisión. Esto puede permitir que los autores de revisiones se beneficien de revisiones Delta más pequeñas. Si el instalador detecta que la revisión diferencial no se puede aplicar al archivo de destino, el instalador puede intentar usar un archivo guardado en la caché de línea de base como punto de partida. El instalador solo recurre a solicitar el origen de instalación original después de probar todas las posibilidades en la memoria caché.

El cumplimiento de las siguientes directrices puede ayudar a los autores de revisiones a usar Windows Installer revisiones de la versión 3,0 y la caché de línea de base para crear revisiones Delta más pequeñas:

-   Cree revisiones que incluyan la [tabla MsiPatchSequence](msipatchsequence-table.md). Esta tabla es necesaria para usar la caché de línea de base y está disponible a partir de Windows Installer versión 3,0.
-   No establezca una directiva que impida el almacenamiento en caché de línea de base. El valor de la directiva [MaxPatchCacheSize](maxpatchcachesize.md) especifica el porcentaje máximo de espacio en disco que se puede usar. Si la Directiva MaxPatchCacheSize se establece en 0, no se guarda ningún archivo adicional en la caché de línea de base. Si no se establece la Directiva, el valor predeterminado es que se puede usar un máximo del 10% del espacio en disco. Si el tamaño total de la memoria caché alcanza el porcentaje máximo de espacio en disco, no se guarda ningún archivo adicional. La Directiva no afecta a los archivos que ya se han guardado. Incluso cuando el almacenamiento en caché está deshabilitado, el instalador puede usar memorias caché de línea de base de producto existentes.
-   Si la primera revisión aplicada incluye la [tabla MsiPatchSequence](msipatchsequence-table.md), el almacenamiento en caché está habilitado para la aplicación.
-   Si alguna revisión de la transacción de servicio no incluye la [tabla MsiPatchSequence](msipatchsequence-table.md), el almacenamiento en caché solo está habilitado para la aplicación si una revisión de actualización secundaria (Service Pack) que incluye la tabla MsiPatchSequence se aplica correctamente al producto.
-   Genere el paquete de revisión mediante herramientas de creación de revisiones como [Msimsp.exe](msimsp-exe.md) y [PATCHWIZ.DLL](patchwiz-dll.md).
-   Siempre tienen como destino revisiones para la versión RTM de la aplicación o una versión de actualización secundaria (Service Pack) de la aplicación. Los destinos especificados en la [tabla TargetImages](targetimages-table-patchwiz-dll-.md) del archivo de propiedades de creación de revisiones (PCP) deben ser puntos de comprobación de producto definidos por los tres primeros campos de la propiedad [**ProductVersion**](productversion.md) .
-   Nunca se dirige a las revisiones en pequeñas imágenes de actualización. Los destinos para compilar la revisión no deben incluir imágenes de actualización de actualización pequeña anterior.

 

 



