---
description: La restauración de archivos en un sistema en ejecución puede ser problemática. Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surjan dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configuraciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154334"
---
# <a name="vss-restore-configurations"></a>Configuraciones de restauración de VSS

La restauración de archivos en un sistema en ejecución puede ser problemática. Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surjan dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.

En VSS, los escritores tienen dos maneras complementarias de administrar restauraciones:[*métodos de restauración*](vssgloss-r.md) y destinos de [*restauración*](vssgloss-r.md).

Además, los solicitantes pueden optar por restaurar archivos en ubicaciones previamente no especificadas y notificar a los escritores (consulte [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

El método restore (también llama al destino de restauración original) se especifica mediante un escritor en el momento de la copia de seguridad y establece una definición para todo el escritor del método que se va a usar para restaurar todos sus componentes en el futuro. Todos los archivos y componentes administrados por un escritor comparten el mismo método de restauración.

Los destinos de restauración permiten a los escritores cambiar el modo en que se restaurarán los componentes específicos en el momento de la restauración. A diferencia de los métodos de restauración, los destinos de restauración se definen para un conjunto de componentes.

En los temas que se enumeran a continuación se muestra una explicación detallada del uso de los métodos de restauración y los destinos de restauración:

-   [Estado de restauración de VSS](vss-restore-state.md)
-   [Definición de los métodos de restauración de VSS](setting-vss-restore-methods.md)
-   [Establecimiento de destinos de restauración de VSS](setting-vss-restore-targets.md)
-   [Establecer opciones de restauración de VSS](setting-vss-restore-options.md)

(Para obtener información sobre las restauraciones que no usan estos mecanismos, vea [restauraciones sin participación del escritor](restores-without-writer-participation.md)).

 

 



