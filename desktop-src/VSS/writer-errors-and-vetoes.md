---
description: Un escritor puede producir un error por numerosas razones de programación.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Errores y vetos del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0835775aec21da9aa69e81b4f7af63f98d765b5c72763cb52af706c4e7a720e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124465"
---
# <a name="writer-errors-and-vetoes"></a>Errores y vetos del escritor

Un escritor puede producir un error por numerosas razones de programación. Cuando esto sucede, debe vetar la operación de copia de seguridad, restauración o instantánea en curso llamando al método [**CVssWriter::SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) en uno de sus métodos de controlador (por ejemplo, [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) o [**CVssWriter::OnPreRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)y devolviendo **TRUE**. También puede establecer opcionalmente una cadena de mensaje de error en respuesta a una condición de error en determinados métodos de controlador con los [**métodos IVssComponentEx::SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx::SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)e [**IVssComponent::SetPostRestoreFailureMsg.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) El solicitante puede aceptar el veto o continuar con la copia de seguridad, omitiendo el veto.

Un solicitante debe comprobar el estado del escritor (mediante [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)después de cada evento que genera.

En algunos casos, Los mensajes de error se pueden recuperar de estos errores (mediante [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx::GetPostSnapshotFail los métodosureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)y [**IVssComponent::GetPostRestoreFailureMsg),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) o bien un escritor puede optar por establecer metadatos (mediante [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) e [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) con información de estado de error). Para obtener código de ejemplo que muestra cómo ver estos mensajes de error, vea [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

En función del estado de error, un solicitante o su operador podrían reiniciar la copia de seguridad y la instantánea con cualquier modificación necesaria en el estado del trabajo o sistema de copia de seguridad.

Por ejemplo, suponga [**que GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) devolvió lo siguiente:

-   **VSS \_ E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** sugiere que un solicitante podría agregar volúmenes adicionales a la instantánea.
-   **VSS \_ E \_ WRITERERROR \_ RETRYABLE** indica que el reintento sin reconfiguración podría funcionar. Si el escritor sigue devolviendo el error después de varios reintentos, intente reiniciar el servicio que hospeda el escritor. Los siguientes escritores se hospedan en el servicio VSS: escritor de registro, escritor de base de datos de registro de clases COM+, escritor de optimización de instantáneas y escritor de Recuperación del sistema automatizado (ASR). Si el escritor pertenece a una aplicación que hospeda el escritor en su propio proceso, intente reiniciar la aplicación.

    **Windows Server 2003 y Windows XP:** Los siguientes escritores se hospedan en el servicio VSS: escritor del Registro, escritor de base de datos de registro de clases COM+, escritor de registro de eventos de aplicación y escritor de motor de escritorio de Microsoft SQL Server 2000 (MSDE).

-   VSS E WRITER STATUS NOT AVAILABLE (ESTADO DE VSS E WRITER NO DISPONIBLE) indica que un escritor puede haber alcanzado el número máximo de sesiones de copia de seguridad y restauración disponibles, y el reintento podría funcionar cuando el sistema está \_ \_ menos \_ \_ \_ ocupado.
-   **VSS \_ E \_ WRITERERROR \_ OUTOFRESOURCES** o **VSS \_ E \_ WRITERERROR \_ TIMEOUT** podrían sugerir que se reduzca la carga del sistema antes de volver a intentarlo.
-   **VSS \_ E \_ WRITERERROR \_ NONRETRYABLE** o **VSS \_ E WRITER NOT \_ \_ \_ RESPONDING** probablemente indicaría un error de escritor tan grave que impide intentar hacer una copia de seguridad de sus datos con VSS.

En función del sistema de escritura y los componentes que los generen, no siempre es necesario que una aplicación de copia de seguridad se anule después de un veto o error.

Por ejemplo, un solicitante puede decidir que la intención de la instantánea es hacer una copia de seguridad de la aplicación A y que el veto se ha recibido del escritor para la aplicación de copia de seguridad B. En este caso, es perfectamente aceptable seguir haciendo una copia de seguridad de la aplicación A mientras se ignora el veto.

A continuación se muestran ejemplos de un veto de escritor:

-   El escritor veta el proceso de creación de instantáneas cuando no pudo suspender sus actividades durante el tiempo en que se creó la instantánea. Esto indica que hay una alta probabilidad de que la instantánea no sea válida porque se ha producido una operación de escritura durante el estado Inmovilizar.
-   Una aplicación de copia de seguridad ha solicitado una instantánea solo del volumen C: y un escritor determina que una instantánea de C: y D: es para hacer una copia de seguridad de sus datos. En este caso, el escritor lo vetará. La aplicación de copia de seguridad puede examinar los metadatos y determinar si se omitirá el escritor o se anulará el proceso de creación de instantáneas y se reiniciará posteriormente.

 

 



