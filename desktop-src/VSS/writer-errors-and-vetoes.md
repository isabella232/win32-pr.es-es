---
description: Un escritor puede producir un error por diversos motivos de programación.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Errores y vetos del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c24c15ad10766fc6ec395ed058ab3cb72a689d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275420"
---
# <a name="writer-errors-and-vetoes"></a>Errores y vetos del escritor

Un escritor puede producir un error por diversos motivos de programación. Cuando esto sucede, debe vetar la operación de copia de seguridad, restauración o instantánea en curso llamando al método [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) en uno de sus métodos de controlador (por ejemplo, [**CVssWriter:: alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) o [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) y devolviendo **true**. Opcionalmente, también puede establecer una cadena de mensaje de error en respuesta a una condición de error en ciertos métodos de controlador con los métodos [**IVssComponentEx:: SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx:: SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)y [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) . El solicitante puede aceptar la veto o continuar con la copia de seguridad, omitiendo la veto.

Un solicitante debe comprobar el estado del escritor (mediante [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) y [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) después de cada evento que genera.

En algunos casos, los mensajes de error se pueden recuperar de estos errores (mediante los métodos [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx:: GetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)y [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) ), o un escritor puede optar por establecer metadatos (mediante [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) y [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) con información de estado de error). Para ver un ejemplo de código que muestra cómo ver estos mensajes de error, consulte [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

En función del estado de error, un solicitante o su operador podría reiniciar la copia de seguridad y la instantánea con cualquier modificación necesaria en el estado del trabajo o sistema de copia de seguridad.

Por ejemplo, supongamos que [**GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) devuelve lo siguiente:

-   **VSS \_ E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** sugiere que un solicitante podría agregar volúmenes adicionales a la instantánea.
-   **VSS \_ E \_ WRITERERROR \_ retryme** indica que el reintento sin reconfiguración podría funcionar. Si el escritor continúa devolviendo el error después de varios reintentos, intente reiniciar el servicio que hospeda el escritor. Los escritores siguientes se hospedan en el servicio VSS: escritor del registro, escritor de base de datos de registro de clases COM+, escritor de optimización de instantáneas y escritor de recuperación automática del sistema (ASR). Si el escritor pertenece a una aplicación que hospeda el escritor en su propio proceso, intente reiniciar la aplicación.

    **Windows Server 2003 y Windows XP:** Los siguientes escritores se hospedan en el servicio VSS: escritor del registro, escritor de la base de datos de registro de clases COM+, escritor de registros de eventos de aplicación y Microsoft SQL Server 2000 Desktop Engine (MSDE) Writer.

-   \_ \_ El estado de VSS E Writer \_ \_ no \_ está disponible indica que un sistema de escritura puede haber alcanzado el número máximo de sesiones de copia de seguridad y restauración disponibles y el reintento podría funcionar cuando el sistema esté menos ocupado.
-   **VSS \_ E \_ WRITERERROR \_ OUTOFRESOURCES** o **VSS \_ e \_ WRITERERROR de \_ tiempo de espera** podrían sugerir que se reduzca la carga del sistema antes de volver a intentarlo
-   **VSS \_ E \_ WRITERERROR \_** que no se puede reintentar o que el **escritor de VSS \_ \_ \_ no \_ responde** podría indicar un error del escritor tan grave como para impedir el intento de realizar una copia de seguridad de sus datos con VSS.

En función del escritor y de los componentes que los generen, no siempre es necesario que una aplicación de copia de seguridad se anule tras una veto o un error.

Por ejemplo, un solicitante puede decidir que la intención de la instantánea es realizar una copia de seguridad de la aplicación A y que se ha recibido el veto del escritor para la aplicación de copia de seguridad B. En este caso, es absolutamente aceptable continuar con la copia de seguridad de la aplicación A mientras se omite la veto.

A continuación se muestran ejemplos de veto de escritor:

-   El escritor veta el proceso de creación de instantáneas cuando no pudo suspender sus actividades durante el tiempo de creación de la instantánea. Esto indica que hay una alta probabilidad de que la instantánea no sea válida porque se ha producido una operación de escritura durante el estado de inmovilización.
-   Una aplicación de copia de seguridad ha solicitado una instantánea del volumen C: y un escritor determina que una instantánea de C: y D: es realizar una copia de seguridad de sus datos. En este caso, el escritor será veto. La aplicación de copia de seguridad puede examinar los metadatos y determinar si se omitirá el escritor o se anulará el proceso de creación de instantáneas y se reiniciará más adelante.

 

 



