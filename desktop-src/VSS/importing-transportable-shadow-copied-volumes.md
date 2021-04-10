---
description: A veces es conveniente crear una instantánea en un sistema, pero usar la instantánea en un segundo sistema.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importar volúmenes de instantáneas transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156125"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importar volúmenes de instantáneas transportables

A veces es conveniente crear una instantánea en un sistema, pero usar la instantánea en un segundo sistema.

Considere el caso en el que los datos de los que se va a realizar la copia de seguridad se administran normalmente mediante un sistema determinado (*systemOne*) durante las operaciones normales y que estos datos se almacenan físicamente en una matriz de almacenamiento o un dispositivo.

Para minimizar cualquier interrupción en *systemOne* (debido a que las operaciones de copia de seguridad pueden consumir muchos recursos), es conveniente realizar la copia de seguridad con *systemTwo*, un servidor de copia de seguridad, que tiene acceso a la misma matriz de almacenamiento que *systemOne*.

Para garantizar una instantánea adecuada, cooperando con los escritores en *systemOne* y conservando el estado adecuado para las tareas en curso: *systemOne* debe realizar la instantánea.

Por lo tanto, *systemOne* debe crear una [*instantánea transportable*](vssgloss-t.md), que a continuación se importará *systemTwo* .

**Windows server 2003, Standard Edition, Windows server 2003, Web Edition y Windows XP:** No se admiten los conjuntos de instantáneas transportables. Todas las ediciones de Windows Server 2003 con Service Pack 1 (SP1) admiten conjuntos de instantáneas transportables.

Un ejemplo típico de la importación de una instantánea transportable puede continuar de la siguiente manera:

1.  Inicialmente, la unidad lógica (LUN) proporcionada por la matriz de almacenamiento se monta como un volumen en *systemOne* (por ejemplo, F:).
2.  Un solicitante que se ejecuta en *systemOne* crea una instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y continúa como si se estuviera preparando para una copia de seguridad. (Consulte información general sobre la [inicialización de copias de seguridad](overview-of-backup-initialization.md), [información general de la fase de detección de copias](overview-of-the-backup-discovery-phase.md)de seguridad e información general sobre [las tareas de copia](overview-of-pre-backup-tasks.md) de seguridad para más información).
3.  El solicitante de *systemOne* modifica el contexto de instantáneas que se usa normalmente para la operación de copia de seguridad local (**VSS \_ CTX \_ App \_ backup**) para indicar que se creará una instantánea transportable (**VSS \_ VOLSNAP \_ ATTR \_ transportable**). También se puede Agregar el atributo transportable a otros contextos de instantánea.
4.  Con un contexto de instantáneas de VSS de solicitud de **\_ copia de \_ \_ seguridad de aplicaciones** de VSS \| , el solicitante que se encuentra en *systemOne* crea una instantánea mediante una llamada a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). **\_ \_ \_**
5.  *SystemOne* usa [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para guardar el estado actual del documento de componentes de copia de seguridad y [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para guardar los documentos de metadatos del escritor de cada escritor. Las cadenas XML que contienen estos documentos se ponen a disposición de un solicitante que se ejecuta en *systemTwo*.

    El solicitante transfiere el documento de componentes de copia de seguridad a *systemTwo*.

    Tenga en cuenta que el solicitante de *systemOne* no libera su instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en este momento si el propósito de la instantánea es para la copia de seguridad. La interfaz debe permanecer abierta hasta que *systemTwo* finalice correctamente las operaciones de copia de seguridad. Solo entonces el solicitante emitirá un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , ya que algunos escritores truncarán los registros y realizarán otro trabajo después de una copia de seguridad correcta. Si el objetivo de la instantánea es la minería de datos o cualquier otro propósito, la interfaz se puede cerrar en este paso.

6.  A continuación, el solicitante de *systemTwo* llama a [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) para obtener acceso a la instantánea creada por el solicitante en *systemOne*.
    > [!Note]  
    > El solicitante es responsable de serializar la operación de instantánea de importación. Además, si se produce un error en la llamada a [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) , VSS no limpiará los LUN de su propiedad. El solicitante tiene que iniciar la limpieza de LUN.

     

7.  El solicitante de *systemTwo* continúa con la copia de seguridad del material de copia sombra exactamente como si se tratara de una copia de seguridad de una instantánea creada por sí misma (consulte [información general sobre la copia de seguridad real de archivos](overview-of-actual-backup-of-files.md)).

    El solicitante de *systemTwo* obtiene el [*objeto de dispositivo*](vssgloss-d.md) de la instantánea mediante [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) en la instantánea importada y lo anexa al principio de las rutas de acceso de archivo originales obtenidas de los metadatos para acceder a los archivos de los que se va a hacer una copia de seguridad.

8.  Después de usar la instantánea, el solicitante de *systemTwo* debe eliminar la instantánea. Al igual que con las instantáneas no transportables, si el contexto de instantáneas indica instantáneas de versión automática (por ejemplo, la **\_ copia de \_ seguridad de VSS CTX**), la liberación de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en *systemTwo* hará que el servicio VSS elimine la instantánea. De lo contrario, si el contexto indica una instantánea persistente (por ejemplo, la **\_ \_ \_ reversión de la aplicación VSS CTX**), el solicitante de *systemTwo* debe eliminar explícitamente la instantánea.

    A continuación, el solicitante de *systemTwo* señalará al solicitante en *systemOne* que ha finalizado con la copia de seguridad de la instantánea transportable.

9.  Una vez que el solicitante de *systemOne* ha recibido la notificación de que el solicitante en *systemTwo* ha finalizado la copia de seguridad de la instantánea transportable, notifica a los escritores de su sistema mediante la generación de un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) con una llamada a **IVssBackupComponents:: BackupComplete**. En este momento, el solicitante de *systemOne* es gratuito para liberar su instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

**Instantáneas transportables en un clúster:** Las instantáneas transportables se deben importar desde fuera del clúster, siempre y cuando el volumen original esté montado en el clúster. Para obtener información sobre cómo implementar una recuperación rápida en un clúster, consulte [recuperación rápida mediante el uso de volúmenes de instantáneas transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



