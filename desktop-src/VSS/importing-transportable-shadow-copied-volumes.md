---
description: A veces es conveniente crear una instantánea en un sistema, pero usar la instantánea en un segundo sistema.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importar volúmenes de instantáneas transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73cee5d491cde59767a321094f0a7de2f34da97b29c6ed02e5cc490643b4dcd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510265"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importar volúmenes de instantáneas transportables

A veces es conveniente crear una instantánea en un sistema, pero usar la instantánea en un segundo sistema.

Tenga en cuenta el caso en el que un sistema determinado *(systemOne)* administra normalmente los datos de los que se va a realizar una copia de seguridad durante las operaciones normales, y que estos datos se almacenan físicamente en una matriz de almacenamiento o un dispositivo.

Para minimizar cualquier interrupción en *systemOne* (ya que las operaciones de copia de seguridad pueden realizar un uso intensivo de recursos), es conveniente realizar la copia de seguridad mediante *systemTwo*, un servidor de copia de seguridad, que tiene acceso a la misma matriz de almacenamiento que *systemOne*.

Para garantizar una instantánea adecuada (colaborando con los escritores en *systemOne* y conservando el estado adecuadamente para las tareas en curso), systemOne debe realizar la *instantánea.*

Por lo tanto, *systemOne* debe crear una instantánea [*transportable*](vssgloss-t.md), que *systemTwo* importará a continuación.

**Windows Server 2003, Standard Edition, Windows Server 2003, Web Edition y Windows XP:** No se admiten conjuntos de instantáneas transportables. Todas las ediciones de Windows Server 2003 con Service Pack 1 (SP1) admiten conjuntos de instantáneas transportables.

Un ejemplo típico de importación de una instantánea transportable puede continuar de la siguiente manera:

1.  Inicialmente, la unidad lógica (LUN) proporcionada por la matriz de almacenamiento se monta como un volumen en *systemOne* (por ejemplo, F:).
2.  Un solicitante que se ejecuta en *systemOne* crea una instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) y continúa como si estuviera preparando una copia de seguridad. (Vea [Información general sobre la inicialización de copia](overview-of-backup-initialization.md)de seguridad , Información general [de](overview-of-the-backup-discovery-phase.md)la fase de detección de copias de seguridad e Información general [de](overview-of-pre-backup-tasks.md) las tareas previas a la copia de seguridad para obtener más información).
3.  El solicitante en *systemOne* modifica el contexto de instantánea que se usa normalmente para la operación de copia de seguridad local **(VSS \_ CTX \_ APP \_ BACKUP**) para indicar que se creará una instantánea transportable **(VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE).** El atributo transportable también se puede agregar a otros contextos de instantáneas.
4.  Con un contexto de instantánea de **VSS \_ CTX \_ APP \_ BACKUP** VSS VOLSNAP ATTR TRANSPORTABLE , el solicitante que se encuentra en systemOne crea una instantánea mediante una llamada \| a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). **\_ \_ \_** 
5.  *SystemOne* usa [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para guardar el estado actual del documento de componentes de copia de seguridad e [**IVssExgvWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para guardar los documentos de metadatos del escritor de cada escritor. A continuación, las cadenas XML que contienen estos documentos están disponibles para un solicitante que se ejecuta en *systemTwo*.

    El solicitante transfiere el documento componentes de copia de seguridad al *sistemaTwo*.

    Tenga en cuenta que el solicitante en *systemOne* no libera su instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en este momento si el propósito de la instantánea es realizar una copia de seguridad. La interfaz debe permanecer abierta hasta que *systemTwo* finalice correctamente sus operaciones de copia de seguridad. Solo entonces debe el solicitante emitir un evento [**BackupComplete,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) ya que algunos escritores truncarán los registros y realizarán otro trabajo después de una copia de seguridad correcta. Si el objetivo de la instantánea es la minería de datos u otros propósitos, la interfaz se puede cerrar en este paso.

6.  A continuación, el solicitante en *systemTwo* llama a [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) para obtener acceso a la instantánea creada por el solicitante en *systemOne.*
    > [!Note]  
    > El solicitante es responsable de serializar la operación de importación de instantáneas. Además, si se produce un error en la llamada a [**IVssBackupComponents::ImportSnapshots,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) VSS no limpiará los LUN por su cuenta. El solicitante tiene que iniciar la limpieza de LUN.

     

7.  El solicitante en *systemTwo* continúa con la copia de seguridad del material copiado en la sombra exactamente como si estuviera haciendo una copia de seguridad de una instantánea que creó por sí mismo (consulte Información general sobre la copia de seguridad real de [archivos).](overview-of-actual-backup-of-files.md)

    El solicitante en *systemTwo* obtiene el [](vssgloss-d.md) objeto de dispositivo de la instantánea mediante [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) en la instantánea importada y lo anexa al principio de las rutas de acceso de archivo originales obtenidas de los metadatos para acceder a los archivos de los que se va a realizar una copia de seguridad.

8.  Después de usar la instantánea, el solicitante en *systemTwo* debe eliminar la instantánea. Al igual que con las instantáneas no transportables, si el contexto de la instantánea indica instantáneas de liberación automática (por ejemplo, **VSS \_ CTX \_ BACKUP),** la liberación de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) en *systemTwo* hará que el servicio VSS elimine la instantánea. De lo contrario, si el contexto indica una instantánea persistente (por ejemplo, **VSS \_ CTX \_ APP \_ ROLLBACK),** el solicitante en *systemTwo* debe eliminar explícitamente la instantánea.

    A continuación, el solicitante en *systemTwo* indica al solicitante en *systemOne* que ha terminado con la copia de seguridad de la instantánea transportable.

9.  Una vez que el solicitante en *systemOne* ha recibido la notificación de que el solicitante de *systemTwo* ha finalizado la copia de seguridad de la instantánea transportable, notifica a los escritores en su sistema mediante la generación de un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) con una llamada a **IVssBackupComponents::BackupComplete**. En este momento, el solicitante de *systemOne* puede liberar su instancia de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

**Instantáneas transportables en un clúster:** Las instantáneas transportables se deben importar desde fuera del clúster, siempre y cuando el volumen original se monte dentro del clúster. Para obtener información sobre cómo implementar una recuperación rápida en un clúster, vea Recuperación rápida mediante volúmenes [de instantáneas transportables.](fast-recovery-using-transportable-shadow-copied-volumes.md)

 

 



