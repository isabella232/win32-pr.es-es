---
description: Los escritores son aplicaciones o servicios que almacenan información persistente en archivos en disco y que proporcionan los nombres y ubicaciones de estos archivos a los solicitantes mediante la interfaz de instantáneas.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf748d0c6c4533c81c0f8a8d0c0c5aa9125c92334a1c09d4ab40fad299067b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863795"
---
# <a name="writers"></a>Escritores

[*Los escritores*](vssgloss-w.md) son aplicaciones o servicios que almacenan información persistente en archivos en disco y que proporcionan los nombres y ubicaciones de estos archivos a los solicitantes mediante la interfaz de instantáneas.

Durante las operaciones de copia de seguridad, los escritores garantizan que sus datos están en reposo y son estables, adecuados para la instantánea y la copia de seguridad. Los escritores colaboran con restauraciones desbloqueando archivos cuando sea posible e indicando ubicaciones alternativas cuando sea necesario.

Si no hay escritores presentes durante una operación de copia de seguridad de VSS, todavía se puede crear una instantánea. En este caso, todos los datos del volumen de instantáneas estarán en el [*estado coherente con bloqueos*](vssgloss-c.md).

## <a name="writer-state"></a>Estado del escritor

Los escritores mantienen su estado en un objeto de metadatos basado en XML, el documento de metadatos [*del escritor*](vssgloss-w.md).

Estos metadatos de escritor son la única estructura de datos que contiene el conjunto de archivos [*(ruta*](vssgloss-f.md)de acceso, especificación de archivo y marca de recursividad) de los datos de los que se va a realizar una copia de seguridad y restaurarse.

El documento de metadatos del escritor organiza los conjuntos de archivos del escritor en grupos o [*componentes*](vssgloss-c.md). La relación de uno de estos componentes durante las operaciones de copia de seguridad y restauración con los demás [](vssgloss-s.md)componentes administrados por el escritor se describe en el documento de metadatos del escritor por la capacidad de selección del componente para la copia de seguridad [*,*](vssgloss-s.md)su capacidad de selección para la restauración y sus rutas de acceso lógicas [*.*](vssgloss-l.md) (Para obtener más información, vea [Configurar la organización de componentes](definition-of-components-by-writers.md) y Trabajar con la capacidad de selección y las [rutas de acceso lógicas).](working-with-selectability-and-logical-paths.md)

En este documento también se incluye información adicional que rige la restauración de archivos y otros problemas.

El solicitante necesita los metadatos del escritor, junto con su propio documento de componentes de copia de seguridad, para procesar una copia de seguridad o una restauración.

A diferencia del documento componentes de copia de seguridad, el documento de metadatos del escritor debe considerarse como una estructura de solo lectura. Una vez que un escritor lo crea, el documento no se modifica.

## <a name="writer-event-handling"></a>Control de eventos writer

Las operaciones VSS de un escritor se inician mediante la recepción de eventos COM.

Cuando no hay eventos presentes, un escritor no realiza operaciones de VSS (como una copia de seguridad o restauración de VSS). En su lugar, realiza su trabajo normal, como responder a consultas de base de datos, administrar datos de usuario o proporcionar otros servicios.

Para asegurarse de que el control de errores para varias sesiones de copia de seguridad y restauración en paralelo se realiza correctamente y para asegurarse de que una sesión de copia de seguridad o restauración no da error a otra, debe hacer lo siguiente:

-   Si el controlador de eventos de un escritor (como [**CVssWriter::OnFreeze)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)llama al método [**CVssWriterEx2::GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter::SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)o [**CVssWriterEx2::SetWriterFailureEx,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) el controlador de eventos debe llamar al método en el mismo subproceso que llamó al controlador de eventos.
-   La implementación del escritor de un controlador de eventos como [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) puede descargar el trabajo en subprocesos de trabajo si lo desea, siempre y cuando cada subproceso de trabajo serializa los errores necesarios para notificar al subproceso del controlador de eventos original.

## <a name="handling-identify-events"></a>Control de eventos de identificación

A excepción del evento Identify, el tipo y el orden de los eventos que recibe un escritor depende de forma exclusiva del tipo de operaciones de VSS que están en curso actualmente.

El evento Identify requiere que los escritores proporcionen la información del sistema sobre su configuración y los archivos que administran a través de su [*documento de metadatos del escritor*](vssgloss-w.md). Se genera un evento Identify para admitir casi cualquier operación de VSS, incluidas las consultas del sistema, así como las operaciones de instantáneas y copia de seguridad y restauración. Por lo tanto, la implementación de cualquier escritor del controlador de eventos Identify [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) debe ser capaz de controlar un evento Identify en cualquier momento, incluso en medio del procesamiento de otra operación de VSS, como una copia de seguridad o una restauración. Un evento Identify nunca debe considerarse como parte del ciclo de vida de una operación de VSS, aunque su generación puede ser esperada y necesaria antes del inicio de esa operación.

Es especialmente importante que la información de estado sobre una operación de VSS no se modifique en [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), porque la recepción de un evento fuera de servicio restablecería esa información.

## <a name="backup-and-restore-events"></a>Eventos de copia de seguridad y restauración

Dependiendo de si participa en una copia de seguridad o restauración, un escritor recibirá entre dos y siete eventos, además de un evento inicial de identificación.

El control de estos eventos constituye (desde el punto de vista de un escritor) el ciclo de vida de una operación de copia de seguridad o restauración.

En una operación de copia de seguridad típica (vea Información general sobre el procesamiento de una copia de seguridad en [VSS),](overview-of-processing-a-backup-under-vss.md)un escritor controlaría los siguientes eventos (además de un evento de identificación inicial):

-   PrepareForBackup
-   PrepareForSnapshot
-   Freeze
-   Reanudar
-   PostSnapshot
-   BackupComplete
-   BackupShutdown

En una operación de restauración típica (vea Información general sobre el procesamiento de una restauración [en VSS),](overview-of-processing-a-restore-under-vss.md)un escritor controlaría los eventos siguientes:

-   PreRestore
-   PostRestore

 

 



