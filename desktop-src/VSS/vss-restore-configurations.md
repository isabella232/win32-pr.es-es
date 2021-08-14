---
description: La restauración de archivos en un sistema en ejecución puede ser problemática. Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surgen dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configuraciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48b3486128c6a91f601a89d697a4db9d8ab27fe9d3ac4cbef28dc870928d37d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344217"
---
# <a name="vss-restore-configurations"></a>Configuraciones de restauración de VSS

La restauración de archivos en un sistema en ejecución puede ser problemática. Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surgen dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.

En VSS, los escritores tienen dos formas complementarias de administrar restauraciones: métodos [*de*](vssgloss-r.md) restauración y destinos [*de restauración.*](vssgloss-r.md)

Además, los solicitantes pueden elegir restaurar archivos en ubicaciones no especificadas previamente y notificar a los escritores (vea [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).

Un escritor especifica el método de restauración (también llamado destino de restauración original) en un momento de copia de seguridad y establece una definición de todo el escritor del método que se usará para restaurar todos sus componentes en el futuro. Todos los archivos y componentes administrados por un escritor comparten el mismo método de restauración.

Los destinos de restauración permiten a los escritores cambiar cómo se van a restaurar componentes específicos en el momento de la restauración. A diferencia de los métodos de restauración, los destinos de restauración se definen para un conjunto de componentes.

Encontrará una explicación detallada del uso de los métodos de restauración y los destinos de restauración en los temas que se enumeran a continuación:

-   [Estado de restauración de VSS](vss-restore-state.md)
-   [Definición de los métodos de restauración de VSS](setting-vss-restore-methods.md)
-   [Establecer destinos de restauración de VSS](setting-vss-restore-targets.md)
-   [Establecer las opciones de restauración de VSS](setting-vss-restore-options.md)

(Para obtener información sobre las restauraciones que no usan estos mecanismos, vea [Restauraciones sin participación del escritor).](restores-without-writer-participation.md)

 

 



