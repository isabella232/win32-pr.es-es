---
description: La configuración de las operaciones de restauración comienza realmente durante la copia de seguridad de datos, cuando los escritores especifican, en los documentos de metadatos del escritor, cómo se deben restaurar sus datos.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Definición de los métodos de restauración de VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412cb699fb791a973e280f63fec03bd2854ccd1d
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279717"
---
# <a name="setting-vss-restore-methods"></a>Definición de los métodos de restauración de VSS

La configuración de las operaciones de restauración comienza realmente durante la copia de seguridad de datos, cuando los escritores especifican, en los documentos de metadatos del escritor, cómo se deben restaurar sus datos.

Estas especificaciones, a las que se hace referencia como [*métodos de restauración*](vssgloss-r.md) o [*destinos de restauración*](vssgloss-r.md)originales, se pueden modificar durante la restauración mediante la configuración de nuevos destinos de restauración o solicitantes que se restauran en nuevas ubicaciones (vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md)).

Al llamar a [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), un escritor indica qué método de restauración debe usarse en su documento de metadatos del escritor. El método restore es Set Writer Wide y se aplica a todos los archivos de todos los componentes que un escritor administra.

Un solicitante obtiene (y debe respetar) esta información mediante una llamada a [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

El método restore se define mediante una enumeración de enumeración [**\_ \_ RESTOREMETHOD de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) , que se pasa a [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) y se devuelve desde [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

El documento de metadatos del escritor admite los siguientes métodos de restauración válidos (un método de restauración de VSS \_ RME \_ sin definir indica un error de escritura). En las figuras se resume cómo se deben implementar los distintos métodos de restauración admitidos y definidos (VSS \_ RME \_ personalizado no tiene ninguna figura asociada, porque por definición es específico del escritor y debe seguir las API y la documentación específicas del escritor):

-   la restauración de RME de VSS, \_ \_ \_ si \_ no \_ existe. Restaure los archivos de componentes en el disco si no hay ninguno de los archivos en el disco. El estado del archivo de destino debe comprobarse después de un evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   la \_ restauración de RME de VSS \_ \_ si \_ puede \_ reemplazar. Restaure los archivos en el disco si se pueden reemplazar todos los archivos. El estado del archivo de destino debe comprobarse después de un evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   Inicio de la restauración de la detención de VSS de VSS \_ \_ \_ \_ . Un servicio se detendrá antes de restaurar los archivos.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   la \_ \_ restauración \_ de RME de VSS en una \_ \_ ubicación alternativa. Restaure los archivos en el disco en una ubicación alternativa. Las asignaciones de ubicación alternativas se especifican en el documento de metadatos del escritor.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   \_ \_ restauración de RME \_ de VSS en el \_ reinicio. Provocar que los archivos se restauren (se sobrescriban) cuando se reinicie el equipo.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   la \_ \_ restauración \_ de RME de VSS en el \_ reinicio \_ si \_ no se puede \_ reemplazar. Si un archivo no se pudo restaurar en el disco en un sistema en ejecución, se restaurará (se sobrescribirá) cuando se reinicie el equipo.
    ![Diagrama que muestra una forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE de árbol de solución de problemas. ](images/raricr.png)
-   RME de VSS \_ \_ personalizado. Ninguno de los métodos predefinidos funcionará; la aplicación de copia de seguridad debe usar las API especializadas para realizar la operación de restauración. Para este método de copia de seguridad, el solicitante debe comprender por completo el escritor en cuestión. Consulte [casos de uso de VSS especiales](special-vss-usage-cases.md) para instancias admitidas actualmente.

 

 



