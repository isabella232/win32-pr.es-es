---
description: La participación de un escritor en una operación de copia de seguridad o restauración, y cuál de sus datos se guardan, depende de cuáles de sus componentes se incluyen explícitamente como parte del documento componentes de copia de seguridad de un solicitante y la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Trabajar con la capacidad de selección y las rutas de acceso lógicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f008b086ea50a1695a76f8b7beecab473b767fb1e2835fd5686197bb1b583175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344258"
---
# <a name="working-with-selectability-and-logical-paths"></a>Trabajar con la capacidad de selección y las rutas de acceso lógicas

La participación de un escritor en una operación de copia de seguridad o [](vssgloss-e.md) restauración, y cuál de sus datos se guardan, depende de cuáles de sus componentes se incluyen explícitamente como parte del documento componentes de copia de seguridad de un solicitante y la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.

Los escritores sin componentes agregados al documento de componente de copia de seguridad de un solicitante antes de la generación de un evento [*PrepareForBackup*](vssgloss-p.md) (en el caso de las operaciones de copia de seguridad) o de un evento [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (en el caso de las operaciones de restauración) no reciben ningún evento después de este punto y no participarán en la operación de copia de seguridad o restauración.

Sin embargo, la libertad del solicitante para incluir o excluir cualquier componente determinado en una copia de seguridad o restauración se rige por lo siguiente:

-   Cualquier jerarquía que exista entre los componentes administrados por un escritor y expresados por [ *rutas de acceso lógicas*](vssgloss-l.md)
-   Si el componente se designa como [ *seleccionable para la copia de seguridad*](vssgloss-s.md)
-   Si se designa como [ *seleccionable para la restauración*](vssgloss-s.md)
-   Si existe una dependencia explícita entre un componente determinado de un sistema de escritura determinado y otros componentes de otros escritores

Encontrará más información sobre estos problemas en los temas siguientes:

-   [Ruta de acceso lógica de componentes](logical-pathing-of-components.md)
-   [Trabajar con selectability for Backup](working-with-selectability-for-backup.md)
-   [Trabajar con selectability for restore and subcomponents](working-with-selectability-for-restore-and-subcomponents.md)
-   [Capacidad de selección y trabajo con propiedades de componente](selectability-and-working-with-component-properties.md)
-   [Dependencias entre componentes administrados por diferentes escritores](dependencies-between-components-managed-by-different-writers.md)

 

 



