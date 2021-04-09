---
description: 'La versión 2003 de Windows Server del Servicio de instantáneas de volumen contiene la siguiente funcionalidad nueva:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nueva funcionalidad disponible en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5782ef6b24f208f69e50cdb992e12ba3212c47f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156121"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nueva funcionalidad disponible en Windows Server 2003

La versión 2003 de Windows Server del Servicio de instantáneas de volumen contiene la siguiente funcionalidad nueva:

-   Compatibilidad con [*la selección de la restauración*](vssgloss-s.md) además de y en igualdad con [*la selección de la copia de seguridad*](vssgloss-s.md) (que anteriormente solo se conocía como selección). Vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md) para obtener más información.
-   Introducción de un evento [*BackupShutdown*](vssgloss-b.md) que indica que se ha cerrado una aplicación de copia de seguridad compatible con VSS (solicitante), si el intento de copia de seguridad se ha completado correctamente o no. Consulte [control de eventos BackupShutdown](handling-backupshutdown-events.md) para obtener más información.
-   Compatibilidad con dependencias de componentes de escritor explícitos. Un medio para describir y admitir las situaciones en las que no se puede realizar una copia de seguridad de un componente (y el conjunto de componentes que define) administrado por un escritor de forma independiente de los componentes administrados por otros escritores. Vea las [dependencias entre los componentes administrados por escritores diferentes](dependencies-between-components-managed-by-different-writers.md) para obtener más información.
-   Compatibilidad total con las operaciones de [*archivos parciales*](vssgloss-p.md) . La copia de seguridad y restauración de segmentos de archivos por escritores y solicitantes ahora es totalmente compatible. Consulte [trabajar con archivos parciales](working-with-partial-files.md) para obtener más información sobre las operaciones de archivos parciales.
-   Introducción de [*los archivos diferenciados*](vssgloss-d.md) para admitir operaciones de copia de seguridad y restauración incrementales. Para obtener más información [, vea copias de seguridad incrementales y diferenciales](incremental-and-differential-backups.md) .
-   Introducción de los esquemas de copia de seguridad como un concepto que indica el nivel de compatibilidad del escritor para tipos de operaciones de copia de seguridad. Para obtener más información, consulte [**\_ \_ esquema de copia de seguridad de VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) .
-   Compatibilidad con la especificación del solicitante de nuevos destinos de restauración de archivos ([*nuevas ubicaciones de destino*](vssgloss-n.md)) durante las operaciones de restauración. Consulte [trabajar con nuevos destinos durante la restauración](working-with-new-targets-during-restore.md) para obtener más información.
-   Compatibilidad con la restauración condicional en el momento del reinicio. Consulte restauración de RME de VSS \_ \_ en el \_ \_ reinicio \_ si \_ no se puede \_ reemplazar ([**VSE \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)) para obtener más información.
-   Definición de un estado de restauración y un tipo de restauración. Para obtener más información, vea [**VSS \_ restore \_ Type**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) y [VSS restore State](vss-restore-state.md) .
-   Compatibilidad con consultas del escritor sobre el estado de la instantánea. Vea [**CVssWriter:: getContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) y [**CVssWriter:: GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) para obtener más información.
-   Compatibilidad con las instantáneas transportables en Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition. Para obtener más información, vea [importar volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md).

 

 



