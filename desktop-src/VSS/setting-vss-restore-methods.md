---
description: La configuración de las operaciones de restauración comienza realmente durante la copia de seguridad de datos, cuando los escritores especifican, en sus documentos de metadatos del escritor, cómo se deben restaurar sus datos.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Definición de los métodos de restauración de VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f7b0d138555b1e10dba55483c694c08a649e97e59cb66ed65c1a276187d3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751765"
---
# <a name="setting-vss-restore-methods"></a>Definición de los métodos de restauración de VSS

La configuración de las operaciones de restauración comienza realmente durante la copia de seguridad de datos, cuando los escritores especifican, en sus documentos de metadatos del escritor, cómo se deben restaurar sus datos.

Estas especificaciones, a [](vssgloss-r.md) las que se hace referencia como métodos de restauración o destinos de restauración [*originales,*](vssgloss-r.md)se pueden modificar durante la restauración mediante escritores que estableciendo nuevos destinos de restauración o por solicitantes que se restauran en nuevas ubicaciones (vea Ubicaciones de copia de seguridad y restauración no predeterminadas). [](non-default-backup-and-restore-locations.md)

Al llamar [**a IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), un escritor indica qué método de restauración se debe usar en su documento de metadatos del escritor. El método de restauración se establece en todo el sistema de escritura y se aplica a todos los archivos de todos los componentes que administra un escritor.

Un solicitante obtiene (y debe respetar) esta información mediante una llamada a [**IVssExbruWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

El método de restauración se define mediante una enumeración [**\_ \_ ENUM DE VSS RESTOREMETHOD,**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) que se pasa a [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) y se devuelve desde [**IVssExstoreWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

El documento de metadatos del escritor admite los siguientes métodos de restauración válidos (un método de restauración de VSS \_ RME \_ UNDEFINED indica un error de escritor). En las cifras se resume cómo se deben implementar los distintos métodos de restauración admitidos y definidos (VSS RME CUSTOM no tiene ninguna figura asociada, ya que por definición es específico del escritor y debe seguir las API de escritor y la documentación \_ \_ específicas):

-   RESTAURACIÓN \_ DE VSS RME \_ SI NO \_ \_ \_ EXISTE. Restaure los archivos de componente en el disco si ninguno de los archivos ya está en el disco. El estado del archivo de destino debe comprobarse después [**de un evento prerestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   RESTAURACIÓN \_ DE VSS RME \_ SI PUEDE \_ \_ \_ REEMPLAZAR. Restaure los archivos en el disco si se pueden reemplazar todos los archivos. El estado del archivo de destino debe comprobarse después [**de un evento prerestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   INICIO DE \_ LA RESTAURACIÓN DE DETENCIÓN DE VSS \_ RME. \_ \_ Un servicio se detendrán antes de restaurar los archivos.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   RESTAURACIÓN \_ DE VSS RME \_ EN UNA UBICACIÓN \_ \_ \_ ALTERNATIVA. Restaure los archivos en el disco en una ubicación alternativa. Las asignaciones de ubicación alternativas se especifican en el documento de metadatos del escritor.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   RESTAURACIÓN \_ DE VSS RME \_ EN EL \_ \_ REINICIO. Hacer que los archivos se restauran (sobrescriban) cuando se reinicie el equipo.
    ![Diagrama que muestra un árbol de solución de problemas para VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   RESTAURACIÓN \_ DE VSS RME \_ EN EL REINICIO SI NO SE PUEDE \_ \_ \_ \_ \_ REEMPLAZAR. Si un archivo no se pudo restaurar en el disco en un sistema en ejecución, se restaura (sobrescribe) cuando se reinicia el equipo.
    ![Diagrama que muestra un árbol de solución de problemas forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE. ](images/raricr.png)
-   VSS \_ RME \_ CUSTOM. Ninguno de los métodos predefinidos funcionará; la aplicación de copia de seguridad debe usar API especializadas para realizar la operación de restauración. Para este método de copia de seguridad, el solicitante debe comprender completamente el escritor en cuestión. Consulte [Casos de uso especiales de VSS](special-vss-usage-cases.md) para las instancias admitidas actualmente.

 

 



