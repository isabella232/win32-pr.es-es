---
description: Un solicitante es cualquier aplicación que use la API de VSS (específicamente la interfaz IVssBackupComponents) para solicitar los servicios de la Servicio de instantáneas de volumen para crear y administrar instantáneas y conjuntos de instantáneas de uno o más volúmenes.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276350"
---
# <a name="requesters"></a>Solicitantes

Un [*solicitante*](vssgloss-r.md) es cualquier aplicación que use la API de VSS (específicamente la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ) para solicitar los servicios de la servicio de instantáneas de volumen para crear y administrar instantáneas y conjuntos de instantáneas de uno o más volúmenes.

El ejemplo más típico de un solicitante (y el único que se trata en esta documentación) es una aplicación de copia de seguridad/restauración compatible con VSS, que usa datos de copia sombra como origen estable para sus operaciones de copia de seguridad.

Además de iniciar las instantáneas, las aplicaciones del solicitante de copias de seguridad y recuperación se comunican con los productores de datos (escritores) para recopilar información sobre el sistema y para indicar a los escritores que deben preparar sus datos para la copia de seguridad.

## <a name="requester-state"></a>Estado del solicitante

Un solicitante mantiene su información de estado en un objeto de metadatos basado en XML denominado documento de componentes de copia de seguridad. Los metadatos del solicitante son necesarios, pero no suficientes para permitir que un solicitante realice una copia de seguridad y, a continuación, restaure un sistema de archivos. Las razones para esto son las siguientes:

-   Durante una operación de copia de seguridad, solo un subconjunto de todos los componentes implicados en la copia de seguridad, que no se [*selecciona para*](vssgloss-s.md) los componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad y que se pueda seleccionar para los componentes de copia de seguridad que se han [*incluido explícitamente*](vssgloss-e.md) en la copia de seguridad, se han agregado al documento componentes de copia de seguridad del solicitante
-   La información incluso para los componentes agregados al documento componentes de copia de seguridad está incompleta: no se incluyen las especificaciones de archivos y rutas de acceso.
-   Durante las operaciones de restauración, un componente [*incluido implícitamente*](vssgloss-i.md) en la copia de seguridad puede [*seleccionarse para la restauración*](vssgloss-s.md) y, por tanto, se puede incluir explícitamente en la restauración. Esto requerirá la actualización del documento componentes de copia de seguridad del solicitante con información de copias almacenadas del documento de metadatos del escritor de un escritor.

Para permitir la especificación completa de una operación de copia de seguridad o restauración, la API de VSS permite al solicitante consultar los metadatos de los escritores en ejecución (durante las copias de seguridad) o examinar los metadatos del escritor almacenados (durante las restauraciones). Además, un escritor puede modificar la información del componente en el documento componentes de copia de seguridad en el transcurso de una operación de copia de seguridad o restauración.

Con la información sobre qué componentes se han seleccionado para copias de seguridad y restauración, y las reglas relativas a la selección de componentes (para obtener más información, consulte Configuración de la [organización de componentes](definition-of-components-by-writers.md) y [trabajar con selecciones y rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)), un solicitante puede determinar los archivos de los que el escritor necesita realizar copias de seguridad o restaurar, y dónde puede encontrar esos archivos.

Como parte de una copia de seguridad, los metadatos del solicitante y del escritor deben almacenarse para que se puedan usar en la restauración. Por el contrario, las operaciones de restauración requieren la recuperación de los componentes antiguos de copia de seguridad y los documentos de metadatos del escritor para obtener instrucciones completas sobre la restauración de archivos.

## <a name="requester-interprocess-communication"></a>Comunicación entre procesos del solicitante

El solicitante mantiene el control sobre las operaciones de copia de seguridad y restauración de VSS mediante la generación de eventos COM a través de varias llamadas en la API del solicitante. Estas llamadas pueden hacer lo siguiente:

-   Realice solicitudes de los proveedores, por ejemplo, [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) hace que el proveedor cree una instantánea del volumen seleccionado.
-   Desencadene que los escritores devuelvan información, por ejemplo, [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) permite al solicitante obtener el documento de metadatos del escritor de cada escritor.
-   Exigir a los escritores que se preparen o controlen varias fases de las operaciones de instantáneas y copia de seguridad, por ejemplo, [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) indica a los escritores que se configuren para la inmovilización de e/s.

Un solicitante recibe información de los escritores a través de documentos de metadatos de escritor en directo o almacenados y mediante el uso de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , que el escritor puede actualizar.

## <a name="life-cycle-of-a-requester-during-backup"></a>Ciclo de vida de un solicitante durante la copia de seguridad

A continuación se facilita un resumen del ciclo de vida del solicitante para la copia de seguridad:

1.  Crear instancias e inicializar interfaces de la API de VSS.
2.  Póngase en contacto con escritores y recupere su información.
3.  Elija los datos de los que desea hacer una copia de seguridad.
4.  Solicite una instantánea del proveedor.
5.  Realice una copia de seguridad de los datos.
6.  Libere la interfaz y la instantánea.

## <a name="life-cycle-of-a-requester-during-restore"></a>Ciclo de vida de un solicitante durante la restauración

El ciclo de vida de restauración no requiere una instantánea, pero todavía requiere la cooperación del escritor:

1.  Cree instancias de las interfaces de la API de VSS.
2.  Inicializa el solicitante para la operación de restauración mediante la carga de un documento almacenado de componentes de copia de seguridad.
3.  Recuperar documentos de componentes de copia de seguridad y metadatos del escritor almacenados.
4.  Póngase en contacto con los escritores para inicializar la cooperación.
5.  Compruebe si hay actualizaciones del escritor en el documento componentes de copia de seguridad.
6.  Restaure los datos.

 

 



