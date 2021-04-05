---
description: 'El documento de metadatos del escritor contiene tres conjuntos de datos: información de clasificación e identificación del escritor, especificaciones de nivel de escritor y datos de componentes.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Contenido del documento de metadatos de escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082130"
---
# <a name="writer-metadata-document-contents"></a>Contenido del documento de metadatos de escritor

El documento de metadatos del escritor contiene tres conjuntos de datos: información de clasificación e identificación del escritor, especificaciones de nivel de escritor y datos de componentes.

## <a name="writer-identification-information"></a>Información de identificación del escritor

La información de clasificación e identificación del escritor incluye lo siguiente:

-   Nombre del escritor
-   [*IDENTIFICADOR de clase del escritor*](vssgloss-w.md)
-   [*Instancia del escritor*](vssgloss-w.md)
-   Cómo se usan los datos administrados por el sistema de escritura en el sistema host (consulte [**\_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   El tipo de datos administrados por el escritor ( [**consulte \_ \_ tipo de origen de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Con la excepción de la instancia del sistema de escritura, que es única y la genera el sistema cuando se inicializa un objeto [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , todos estos valores los establece un escritor cuando llama a [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) y están disponibles para un solicitante llamando a [**IVssExamineWriterMetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Dado que la instancia del escritor se genera de forma única, no es probable que una instancia del escritor almacenada recuperada de un documento de metadatos del escritor almacenado sea útil.

Mediante la comprobación del [**\_ \_ tipo de uso de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), una aplicación puede determinar si un escritor está administrando los datos de aplicaciones generales o si los archivos con los que trabaja forman parte del estado de arranque del sistema o los utiliza un servicio de sistema. Las aplicaciones de copia de seguridad y restauración necesitan respetar los tipos de uso para ayudar a mantener la estabilidad del sistema.

La [**marca \_ \_ tipo de origen de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) indica el tipo de aplicación que el escritor que administra los datos de los que se va a realizar la copia de seguridad durante el funcionamiento normal.

Actualmente, la distinción se limita a especificar si el escritor genera archivos como parte de las operaciones de base de datos transaccionales o no transaccionales, o si los archivos son el resultado de un tipo de actividad más general. Esta lista puede crecer con el tiempo. Esta información puede ser útil para determinar el nivel de actividad normal esperado en los archivos de un escritor.

## <a name="writer-level-specification"></a>Especificación de Writer-Level

Las especificaciones de nivel de escritor contienen información que está en todo el ámbito de escritura, y se aplica a todos los datos independientes de los que un componente lo administra.

Un escritor siempre debe especificar [*los métodos de restauración*](vssgloss-r.md).

Opcionalmente, puede especificar lo siguiente:

-   Excluir lista de archivos
-   [*Asignaciones de ubicación alternativas*](vssgloss-a.md) para la restauración

Las listas de inclusión y exclusión de archivos contienen información de archivo más allá de la de los componentes, y su especificación sustituye a la especificación de componentes.

## <a name="restore-method-specification"></a>Especificación del método restore

El [*método restore*](vssgloss-r.md) se establece en el documento de metadatos del escritor por [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) y se recupera mediante un solicitante con [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Al establecer un método de restauración, un escritor indica la manera preferida de restaurar archivos, también conocido como destino de restauración original, para todos los archivos administrados por un escritor. Por ejemplo, el método restore especifica si se debe permitir que todos los archivos administrados por un escritor sobrescriban los archivos que se encuentran actualmente en el disco. (Consulte [configuración de restauración de VSS](vss-restore-configurations.md) y [**\_ \_ enumeración RESTOREMETHOD de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) para más información).

## <a name="exclude-file-list-specification"></a>Especificación de la lista de archivos excluidos

La lista de exclusión permite la optimización de las especificaciones de los caracteres comodín en los componentes, ya que impide explícitamente que se incluyan determinados archivos en un conjunto de copia de seguridad.

Por ejemplo, un componente puede tener un [*conjunto de archivos*](vssgloss-f.md) que contenga una especificación de archivo de c: \\ Database \\ \* . \* Aunque se trata de una definición adecuada, en ocasiones puede haber archivos temporales generados (quizás de Form \* . tmp) y el escritor siempre quiere impedir su copia de seguridad.

En este caso, un escritor agregaría \* . tmp a su lista de exclusión mediante [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Esta especificación puede ser recursiva.

Un solicitante consulta esta información mediante [**IVssExamineWriterMetadata:: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile).

La lista de archivos excluidos tiene prioridad sobre las listas de archivos de componentes.

Por lo tanto, la lista de archivos especificados para la copia de seguridad en un documento de metadatos de escritor consistiría en todos los archivos especificados en los componentes [*incluidos explícitamente*](vssgloss-e.md) y los componentes [*incluidos implícitamente*](vssgloss-i.md) , menos todos los archivos excluidos.

## <a name="alternate-location-mappings-specification"></a>Especificación de asignaciones de ubicación alternativas

Las asignaciones de ubicación alternativas se establecen inicialmente durante la creación de un documento de metadatos del escritor e indican una ubicación en el disco en la que se pueden restaurar los archivos si no es posible la restauración de un archivo en la ubicación original.

La información se agrega como una cadena de caracteres anchos terminada en NULL con [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) y se recupera como un objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

A pesar de que se especifican y se examinan las asignaciones de ubicaciones alternativas con las interfaces de nivel de escritor ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) y [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)), se especifican en términos de [*conjuntos de archivos*](vssgloss-f.md). El conjunto de archivos que se usa para especificar una asignación de ubicación alternativa (ruta de acceso, especificación de archivo y marca de recursividad) debe coincidir con uno de los conjuntos de archivos ya agregados a uno de los componentes del escritor (consulte [Agregar archivos a componentes](definition-of-components-by-writers.md)).

Para obtener más información, vea [ubicaciones de copia de seguridad y restauración no predeterminadas](non-default-backup-and-restore-locations.md).

## <a name="component-level-information"></a>Información de Component-Level

[*Los componentes*](vssgloss-c.md) son colecciones de archivos que forman una unidad lógica con fines de copia de seguridad y restauración. Se debe realizar una copia de seguridad de todos los archivos de un componente (excepto los excluidos explícitamente) y restaurarlos como una unidad.

Los escritores agregan componentes mediante [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), especificando la siguiente información de componente:

-   Tipo
-   Nombre
-   Ruta de acceso lógica (si existe)
-   Característica admitida
-   [*Selección*](vssgloss-s.md)
-   Metadatos que usará el escritor durante la restauración
-   Mostrar información
-   Información de notificación

[*La selección de la copia de seguridad*](vssgloss-s.md) y [*la selección de la restauración*](vssgloss-s.md) son completamente independientes entre sí, y un escritor las usa junto con las rutas de acceso lógicas para indicar las relaciones entre los distintos componentes que administra. Los escritores pueden indicar qué componentes son necesarios para [*incluirlos explícitamente*](vssgloss-e.md) (los que se pueden incluir explícitamente a discreción de un solicitante) y aquellos que solo se pueden [*incluir implícitamente*](vssgloss-i.md). (Vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)).

Los archivos se agregan a un componente determinado mediante [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). (Consulte [Agregar archivos a los componentes](definition-of-components-by-writers.md)).

Cuando se agregan archivos a un componente durante la copia de seguridad, un escritor debe especificar un conjunto de archivos (una ruta de acceso, una especificación de archivo y una marca de recursividad) que define los archivos de los que se va a hacer una copia de seguridad.

Los escritores también pueden especificar una [*ruta de acceso alternativa*](vssgloss-a.md) para la copia de seguridad, que no se debe confundir con las [*asignaciones de ubicación alternativas*](vssgloss-a.md) mencionadas previamente. Esta ruta de acceso alternativa indica una ubicación no predeterminada desde la que se copiarán los archivos cuando se realice una copia de seguridad de un volumen.

La información sobre un componente determinado en el documento de metadatos del escritor se puede obtener a través de una interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) devuelta por [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Los archivos y las rutas de acceso se devuelven en [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) como objetos [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

La información del componente del escritor se describe en detalle en la [definición de los componentes de escritores](definition-of-components-by-writers.md).

 

 



