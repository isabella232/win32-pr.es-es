---
description: 'La Windows Server 2003 del Servicio de instantáneas de volumen contiene la siguiente funcionalidad nueva:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nueva funcionalidad disponible en Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc444a062fd2e1dae33af80feb88e1da52452064d8ed38c2db6fd5f7f3ae2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591396"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nueva funcionalidad disponible en Windows Server 2003

La Windows Server 2003 del Servicio de instantáneas de volumen contiene la siguiente funcionalidad nueva:

-   Compatibilidad con [*la capacidad de selección para la*](vssgloss-s.md) restauración además de y de forma igual a la capacidad de selección para la copia de seguridad (anteriormente se denominaba selectability). [](vssgloss-s.md) Consulte [Working with Selectability and Logical Paths (Trabajar con la capacidad de selección y las rutas de acceso lógicas)](working-with-selectability-and-logical-paths.md) para obtener más información.
-   Introducción de un [*evento BackupShutdown*](vssgloss-b.md) que indica que una aplicación de copia de seguridad compatible con VSS (solicitante) se ha apagado, tanto si el intento de copia de seguridad se ha completado correctamente como si no. Consulte [Control de eventos backupShutdown](handling-backupshutdown-events.md) para obtener más información.
-   Compatibilidad con dependencias explícitas de componentes de escritura. Un medio para describir y admitir las situaciones en las que un componente (y el conjunto de componentes que define) administrado por un escritor no se puede realizar una copia de seguridad o restaurar independientemente de los componentes administrados por otros escritores. Consulte [Dependencias entre componentes administrados por diferentes escritores](dependencies-between-components-managed-by-different-writers.md) para obtener más información.
-   Compatibilidad total con operaciones [*de archivos parciales.*](vssgloss-p.md) La copia de seguridad y restauración de segmentos de archivos por escritores y solicitantes ahora es totalmente compatible. Consulte [Trabajar con archivos parciales](working-with-partial-files.md) para obtener más información sobre las operaciones de archivos parciales.
-   Introducción de archivos [*diferenciados para admitir*](vssgloss-d.md) operaciones incrementales de copia de seguridad y restauración. Vea [Copias de seguridad incrementales y diferenciales](incremental-and-differential-backups.md) para obtener más información.
-   Introducción de esquemas de copia de seguridad como concepto que indica el nivel de compatibilidad del escritor con los tipos de operaciones de copia de seguridad. Vea [**ESQUEMA DE COPIA DE SEGURIDAD \_ \_ DE VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) para obtener más información.
-   Compatibilidad con la especificación del solicitante de nuevos destinos de restauración de archivos [*(nuevas ubicaciones de destino)*](vssgloss-n.md)durante las operaciones de restauración. Consulte [Trabajar con nuevos destinos durante la restauración](working-with-new-targets-during-restore.md) para obtener más información.
-   Compatibilidad con la restauración condicional en el momento del reinicio. Vea VSS \_ RME \_ RESTORE AT REBOOT IF CANNOT REPLACE ( \_ \_ \_ \_ \_ [**VSE \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)) para obtener más información.
-   Definición de un estado de restauración y un tipo de restauración. Vea [**VSS \_ RESTORE TYPE \_ y**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) [VSS Restore State](vss-restore-state.md) para obtener más información.
-   Compatibilidad con consultas de escritor sobre el estado de la instantánea. Vea [**CVssWriter::GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) y [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) para obtener más información.
-   Compatibilidad con instantáneas transportables en Windows Server 2003, Enterprise Edition y Windows Server 2003, Datacenter Edition. Para obtener más información, vea [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).

 

 



