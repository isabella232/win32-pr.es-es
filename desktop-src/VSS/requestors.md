---
description: Un solicitante es cualquier aplicación que usa la API de VSS (específicamente la interfaz IVssBackupComponents) para solicitar los servicios de Servicio de instantáneas de volumen para crear y administrar instantáneas y conjuntos de instantáneas de uno o varios volúmenes.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e7fa7b1718b0da278dabb164fbffee43c939cd688c150e202bfafc4731a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866385"
---
# <a name="requesters"></a>Solicitantes

Un [](vssgloss-r.md) solicitante es cualquier aplicación que usa la API de VSS (específicamente la interfaz [**IVssBackupComponents)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para solicitar los servicios de Servicio de instantáneas de volumen para crear y administrar instantáneas y conjuntos de instantáneas de uno o varios volúmenes.

El ejemplo más típico de un solicitante (y el único que se trata en esta documentación) es una aplicación de copia de seguridad y restauración que admite VSS, que usa datos copiados en la sombra como origen estable para sus operaciones de copia de seguridad.

Además de iniciar instantáneas, las aplicaciones solicitantes de copia de seguridad y recuperación se comunican con los productores de datos (escritores) para recopilar información sobre el sistema y para indicar a los escritores que preparen sus datos para la copia de seguridad.

## <a name="requester-state"></a>Estado del solicitante

Un solicitante mantiene su información de estado en un objeto de metadatos basado en XML denominado Documento de componentes de copia de seguridad. Los metadatos del solicitante son necesarios, pero no suficientes para permitir que un solicitante haga una copia de seguridad y, a continuación, restaure un sistema de archivos. Las razones son las siguientes:

-   Durante una operación de copia de seguridad, solo un subconjunto de todos los componentes implicados en la copia de [](vssgloss-e.md) [*seguridad,*](vssgloss-s.md) no seleccionables para los componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad y seleccionables para los componentes de copia de seguridad que se han incluido explícitamente en la copia de seguridad, han tenido su información agregada al documento componentes de copia de seguridad del solicitante.
-   La información incluso para los componentes agregados al documento Componentes de copia de seguridad está incompleta: no se incluyen las especificaciones de archivo y ruta de acceso.
-   Durante las operaciones [](vssgloss-i.md) de restauración, un [](vssgloss-s.md) componente incluido implícitamente en la copia de seguridad puede seleccionarse para la restauración y, por tanto, se puede incluir explícitamente en la restauración. Esto requerirá la actualización del documento componentes de copia de seguridad del solicitante con información de copias almacenadas del documento de metadatos del escritor.

Para permitir la especificación completa de una operación de copia de seguridad o restauración, la API de VSS permite al solicitante consultar los metadatos de los escritores en ejecución (durante las copias de seguridad) o examinar los metadatos almacenados del escritor (durante las restauraciones). Además, un escritor puede modificar la información de componentes en el documento Componentes de copia de seguridad en el transcurso de una operación de copia de seguridad o restauración.

Con la información sobre qué componentes se han seleccionado para la copia de [](definition-of-components-by-writers.md) seguridad y restauración y las reglas relativas a la selección de componentes (para obtener más información, vea Configurar la organización de componentes y Trabajar con la capacidad de selección y rutas de acceso lógicas), [](working-with-selectability-and-logical-paths.md)un solicitante puede determinar qué archivos de escritura necesita para realizar copias de seguridad o restaurar, y dónde puede encontrar esos archivos.

Como parte de una copia de seguridad, los metadatos del solicitante y del escritor deben almacenarse para que se puedan usar en la restauración. Por el contrario, las operaciones de restauración requieren la recuperación de los componentes de copia de seguridad antiguos y los documentos de metadatos del escritor para obtener instrucciones completas sobre la restauración de archivos.

## <a name="requester-interprocess-communication"></a>Comunicación entre procesos del solicitante

El solicitante mantiene el control sobre las operaciones de copia de seguridad y restauración de VSS mediante la generación de eventos COM a través de varias llamadas en la API del solicitante. Estas llamadas pueden hacer lo siguiente:

-   Realizar solicitudes de los proveedores, por ejemplo, [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) hace que el proveedor cree una instantánea del volumen seleccionado.
-   Desencadenar los escritores para devolver información, por ejemplo, [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) permite al solicitante obtener el documento de metadatos del escritor de cada escritor.
-   Requerir que los escritores se preparen o controlen varias fases de las operaciones de instantáneas y copia de seguridad, por ejemplo, [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) señala a los escritores que se deben configurar para la inmovilización de E/S.

Un solicitante recibe información de los escritores a través de los documentos de metadatos del escritor en directo o almacenados y mediante el uso de la [**interfaz IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que el escritor puede actualizar.

## <a name="life-cycle-of-a-requester-during-backup"></a>Ciclo de vida de un solicitante durante la copia de seguridad

A continuación se muestra un resumen del ciclo de vida del solicitante para la copia de seguridad:

1.  Cree instancias e inicialice interfaces de LA API de VSS.
2.  Póngase en contacto con los escritores y recupere su información.
3.  Elija los datos de los que desea hacer una copia de seguridad.
4.  Solicite una instantánea del proveedor.
5.  Copia de seguridad de los datos.
6.  Suelte la interfaz y la instantánea.

## <a name="life-cycle-of-a-requester-during-restore"></a>Ciclo de vida de un solicitante durante la restauración

El ciclo de vida de restauración no requiere una instantánea, pero todavía requiere la cooperación del escritor:

1.  Cree instancias de interfaces de LA API de VSS.
2.  Inicialice el solicitante para la operación de restauración cargando un documento de componentes de copia de seguridad almacenado.
3.  Recuperar los metadatos de escritor almacenados y los documentos de componentes de copia de seguridad.
4.  Póngase en contacto con los escritores para inicializar la cooperación.
5.  Compruebe si hay actualizaciones del sistema de escritura en el documento Componentes de copia de seguridad.
6.  Restaure los datos.

 

 



