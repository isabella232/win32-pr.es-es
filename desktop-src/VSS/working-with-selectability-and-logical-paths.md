---
description: La participación de un escritor en una operación de copia de seguridad o restauración, y en la que se guardan los datos depende de qué componentes se incluyan explícitamente como parte del documento de componentes de copia de seguridad del solicitante y de la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Trabajar con la selección y las rutas de acceso lógicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696427"
---
# <a name="working-with-selectability-and-logical-paths"></a>Trabajar con la selección y las rutas de acceso lógicas

La participación de un escritor en una operación de copia de seguridad o restauración, y en la que se guardan los datos depende de qué componentes se [*incluyan explícitamente*](vssgloss-e.md) como parte del documento de componentes de copia de seguridad del solicitante y de la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.

Los escritores sin componentes agregados al documento de componentes de copia de seguridad de un solicitante antes de la generación de un evento [*PrepareForBackup*](vssgloss-p.md) (en el caso de las operaciones de copia de seguridad) o de un evento [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (en el caso de operaciones de restauración) no reciben ningún evento después de este punto y no participarán en la operación de copia de seguridad o restauración.

Sin embargo, la libertad del solicitante de incluir o excluir un componente determinado en una copia de seguridad o restauración se rige por lo siguiente:

-   Cualquier jerarquía que existe entre los componentes administrados por un escritor y que se expresan mediante rutas de acceso [ *lógicas*](vssgloss-l.md)
-   Si el componente se designa como [ *seleccionable para la copia de seguridad*](vssgloss-s.md)
-   Si se designa como [ *seleccionable para la restauración*](vssgloss-s.md)
-   Si existe una dependencia explícita entre un componente determinado de un escritor determinado y otros componentes de otros escritores

En los temas siguientes encontrará más información sobre estos problemas:

-   [Acciones lógicas de los componentes](logical-pathing-of-components.md)
-   [Trabajar con la selección para la copia de seguridad](working-with-selectability-for-backup.md)
-   [Trabajar con la selección para restaurar y subcomponentes](working-with-selectability-for-restore-and-subcomponents.md)
-   [Selección y trabajo con propiedades de componentes](selectability-and-working-with-component-properties.md)
-   [Dependencias entre los componentes administrados por escritores diferentes](dependencies-between-components-managed-by-different-writers.md)

 

 



