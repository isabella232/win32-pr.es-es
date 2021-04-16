---
description: Los escritores son aplicaciones o servicios que almacenan información persistente en archivos en disco y que proporcionan los nombres y las ubicaciones de estos archivos a los solicitantes mediante la interfaz de instantáneas.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696420"
---
# <a name="writers"></a>Escritores

Los [*escritores*](vssgloss-w.md) son aplicaciones o servicios que almacenan información persistente en archivos en disco y que proporcionan los nombres y las ubicaciones de estos archivos a los solicitantes mediante la interfaz de instantáneas.

Durante las operaciones de copia de seguridad, los escritores aseguran que sus datos están inactivos y estables, adecuados para la instantánea y la copia de seguridad. Los escritores colaboran con las restauraciones desbloqueando los archivos cuando sea posible e indicando ubicaciones alternativas cuando sea necesario.

Si no hay ningún escritor presente durante una operación de copia de seguridad de VSS, todavía se puede crear una instantánea. En este caso, todos los datos del volumen de copia sombra estarán en estado de [*bloqueo coherente*](vssgloss-c.md).

## <a name="writer-state"></a>Estado del escritor

Los escritores mantienen su estado en un objeto de metadatos basado en XML, el [*documento de metadatos del escritor*](vssgloss-w.md).

Los metadatos del escritor son la única estructura de datos que contiene el [*conjunto de archivos*](vssgloss-f.md)(ruta de acceso, especificación de archivo y marca de recursividad) de los datos de los que se va a realizar la copia de seguridad y la restauración.

El documento de metadatos del escritor organiza los conjuntos de archivos del escritor en grupos o [*componentes*](vssgloss-c.md). La relación de uno de estos componentes durante las operaciones de copia de seguridad y restauración con los demás componentes administrados por el escritor se describe en el documento de metadatos del escritor según la selección del componente [*para la copia de seguridad*](vssgloss-s.md), su [*selección para restaurar*](vssgloss-s.md)y sus rutas de acceso [*lógicas*](vssgloss-l.md). (Para obtener más información, consulte Configuración de la [organización de componentes](definition-of-components-by-writers.md) y [trabajar con la selección y rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)).

En este documento también se incluye información adicional que rige la restauración de archivos y otros problemas.

El solicitante necesita los metadatos del escritor, junto con su propio documento de componentes de copia de seguridad, para procesar una copia de seguridad o una restauración.

A diferencia del documento componentes de copia de seguridad, el documento de metadatos del escritor debe considerarse como una estructura de solo lectura. Una vez que un escritor lo crea, el documento no se modifica.

## <a name="writer-event-handling"></a>Control de eventos del escritor

Las operaciones de VSS de un escritor se inician a través de la recepción de eventos COM.

Cuando no hay eventos presentes, un escritor no realiza operaciones VSS (como una copia de seguridad o restauración de VSS). En su lugar, realiza su trabajo normal, como responder a las consultas de base de datos, administrar los datos de usuario o proporcionar otros servicios.

Para asegurarse de que el control de errores para varias sesiones de copias de seguridad y restauración en paralelo se realiza correctamente y para asegurarse de que una sesión de copia de seguridad o restauración no dañe otra, debe hacer lo siguiente:

-   Si el controlador de eventos de un escritor (como [**CVssWriter:: alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) llama al método [**CVssWriterEx2:: GetSessionId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)o [**CVssWriterEx2:: SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) , el controlador de eventos debe llamar al método en el mismo subproceso que llamó al controlador de eventos.
-   La implementación del escritor de un controlador de eventos como [**alfreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) puede descargar el trabajo en los subprocesos de trabajo si se desea, siempre que cada subproceso de trabajo calcule las referencias de los informes de errores necesarios de nuevo en el subproceso del controlador de eventos original.

## <a name="handling-identify-events"></a>Control de eventos de identificación

Con la excepción del evento de identificación, el tipo y el orden de los eventos que recibe un escritor dependen de forma exclusiva del tipo de operaciones de VSS que están actualmente en curso.

El evento de identificación requiere que los escritores proporcionen información del sistema sobre su configuración y los archivos que administran a través de su [*documento de metadatos de escritura*](vssgloss-w.md). Un evento de identificación se genera por compatibilidad con casi cualquier operación de VSS, incluidas las consultas del sistema, así como las operaciones de instantáneas y copia de seguridad y restauración. Por lo tanto, la implementación de cualquier escritor del controlador de eventos [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) debe ser capaz de controlar un evento de identificación en cualquier momento, incluso en medio de procesar otra operación de VSS, como una copia de seguridad o una restauración. Un evento de identificación no debe considerarse nunca como parte del ciclo de vida de una operación de VSS, aunque su generación puede ser esperada y necesaria antes del inicio de esa operación.

Es especialmente importante que la información de estado sobre una operación de VSS no se modifique en [**CVssWriter:: he Identify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), ya que la recepción de un evento fuera de orden restablecería esa información.

## <a name="backup-and-restore-events"></a>Eventos de copia de seguridad y restauración

Dependiendo de si participa en una copia de seguridad o una restauración, un escritor recibirá entre dos y siete eventos, además de un evento de identificación inicial.

Controlar estos eventos constituye (desde el punto de vista de un escritor) el ciclo de vida de una operación de copia de seguridad o restauración.

En una operación de copia de seguridad típica (consulte [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md)), un escritor administraría los siguientes eventos (además de un evento de identificación inicial):

-   PrepareForBackup
-   PrepareForSnapshot
-   Freeze
-   Reanudar
-   Instantánea
-   BackupComplete
-   BackupShutdown

En una operación de restauración típica (consulte [información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md)), un escritor administraría los siguientes eventos:

-   Prerestauración
-   Postrestore

 

 



