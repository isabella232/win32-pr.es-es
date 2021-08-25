---
description: 'El documento de metadatos del escritor contiene tres conjuntos de datos: información de identificación y clasificación del escritor, especificaciones de nivel de escritor y datos de componentes.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Contenido del documento de metadatos del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdb8cf4c2313d17cfd9059626f97356f27ba9168f9e19e4a796fae8797728d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905055"
---
# <a name="writer-metadata-document-contents"></a>Contenido del documento de metadatos del escritor

El documento de metadatos del escritor contiene tres conjuntos de datos: información de identificación y clasificación del escritor, especificaciones de nivel de escritor y datos de componentes.

## <a name="writer-identification-information"></a>Información de identificación del escritor

La información de identificación y clasificación del escritor incluye lo siguiente:

-   Nombre del escritor
-   [*Identificador de clase de escritor*](vssgloss-w.md)
-   [*Instancia del escritor*](vssgloss-w.md)
-   Cómo se usan los datos administrados por el escritor en el sistema host (vea [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo de datos administrados por el escritor (vea [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

A excepción de la instancia de escritor, que es única y la genera el sistema cuando se inicializa un objeto [**CVssWriter,**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) todos estos valores los establece un escritor cuando llama a [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) y están disponibles para un solicitante mediante una llamada a [**IVssExerrorWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Dado que la instancia de escritor se genera de forma única, es probable que una instancia de escritor almacenada recuperada de un documento de metadatos del escritor almacenado no sea útil.

Al comprobar [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), una aplicación puede determinar si un escritor administra los datos generales de la aplicación o si los archivos con los que trabaja forman parte del estado de arranque del sistema o son utilizados por un servicio del sistema. Las aplicaciones de copia de seguridad y restauración deben respetar los tipos de uso para ayudar a mantener la estabilidad del sistema.

La [**marca VSS \_ SOURCE TYPE \_ indica**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) qué tipo de aplicación realiza el escritor que administra los datos de los que se va a realizar una copia de seguridad durante el funcionamiento normal.

Actualmente, la distinción se limita a especificar si el escritor genera archivos como parte de operaciones de base de datos transaccionales o no transaccionales, o si los archivos son el resultado de un tipo de actividad más general. Esta lista puede crecer con el tiempo. Esta información puede ser útil para determinar el nivel normal de actividad esperado en los archivos de un escritor.

## <a name="writer-level-specification"></a>Writer-Level especificación

Las especificaciones de nivel de escritor contienen información que es de todo el escritor en su ámbito, que se aplica a todos los datos independientemente de qué componente lo administra.

Un sistema de escritura siempre debe especificar [*métodos de restauración*](vssgloss-r.md).

Opcionalmente, puede especificar lo siguiente:

-   Excluir lista de archivos
-   [*Asignaciones de ubicación alternativas*](vssgloss-a.md) para la restauración

Las listas de archivos include y exclude contienen información de archivo más allá de la de los componentes, y su especificación reemplaza a la especificación del componente.

## <a name="restore-method-specification"></a>Especificación del método restore

[**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) establece el método de restauración en el documento de metadatos del escritor y lo recupera un solicitante [**con IVssExgvWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod). [](vssgloss-r.md)

Al establecer un método de restauración, un sistema de escritura indica la manera preferida de restauración de archivos, también conocida como destino de restauración original, para todos los archivos administrados por un escritor. Por ejemplo, el método de restauración especifica si se debe permitir que todos los archivos administrados por un escritor sobrescriban los archivos actualmente en disco. (Vea [Configuraciones de restauración de VSS](vss-restore-configurations.md) y [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) para obtener más información).

## <a name="exclude-file-list-specification"></a>Especificación de la lista de archivos de exclusión

La lista de exclusión permite ajustar las especificaciones de caracteres comodín en los componentes al impedir explícitamente que determinados archivos se incluyan en un conjunto de copia de seguridad.

Por ejemplo, un componente podría tener un conjunto [*de archivos*](vssgloss-f.md) que contenga una especificación de archivo de c: Base de \\ datos \\ \* \* . Aunque esta es una definición cómoda, en ocasiones puede haber archivos temporales generados (quizás con el formato .tmp) y el escritor siempre quiere impedir \* su copia de seguridad.

En este caso, un escritor agregaría .tmp a su lista de exclusión mediante \* [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Esta especificación podría ser recursiva.

Un solicitante consultaría esta información mediante [**IVssExwriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile).

La lista de archivos de exclusión tiene prioridad sobre las listas de archivos de componentes.

Por lo tanto, la lista de archivos especificados para la copia de [](vssgloss-e.md) seguridad en un [](vssgloss-i.md) documento de metadatos del escritor constaría de todos los archivos especificados en los componentes incluidos explícitamente y los componentes incluidos implícitamente, menos todos los archivos excluidos.

## <a name="alternate-location-mappings-specification"></a>Especificación de asignaciones de ubicación alternativas

Las asignaciones de ubicación alternativas se establecen inicialmente durante la creación de un documento de metadatos del escritor e indican una ubicación en el disco en la que se pueden restaurar los archivos si no es posible restaurar un archivo en la ubicación original.

La información se agrega como una cadena de caracteres anchos terminada en NULL con [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) y se recupera como un objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) de [**IVssExlocationWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

A pesar de que se especifican y examinan asignaciones de ubicación alternativas mediante las interfaces de nivel de escritor [**(IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExgvWriterMetadata),**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)se especifican en términos de conjuntos de archivos [*.*](vssgloss-f.md) El conjunto de archivos que se usa para especificar una asignación de ubicación alternativa (ruta de acceso, especificación de archivo y marca de recursividad) debe coincidir con uno de los conjuntos de archivos ya agregados a uno de los componentes del escritor (vea [Agregar](definition-of-components-by-writers.md)archivos a componentes).

Para obtener más información, vea [Ubicaciones de copia de seguridad y restauración no predeterminadas.](non-default-backup-and-restore-locations.md)

## <a name="component-level-information"></a>Component-Level información

[*Los*](vssgloss-c.md) componentes son colecciones de archivos que forman una unidad lógica con fines de copia de seguridad y restauración. Todos los archivos de un componente (excepto los excluidos explícitamente) deben realizarse y restaurarse como una unidad.

Los escritores agregan componentes [**mediante IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), especificando la siguiente información de componente:

-   Tipo
-   Nombre
-   Ruta de acceso lógica (si la hay)
-   Característica admitida
-   [*Capacidad de selección*](vssgloss-s.md)
-   Metadatos que usará el escritor durante la restauración
-   Mostrar información
-   Información de notificación

[*La capacidad*](vssgloss-s.md) de [](vssgloss-s.md) selección de la copia de seguridad y la capacidad de selección para la restauración son completamente independientes entre sí, y un escritor las usa junto con rutas de acceso lógicas para indicar las relaciones entre los distintos componentes que administra. Los escritores pueden indicar qué componentes son necesarios para incluir explícitamente [*(aquellos*](vssgloss-e.md) que se pueden incluir explícitamente a discreción de un solicitante) y aquellos que solo se pueden incluir [*implícitamente.*](vssgloss-i.md) (Vea [Trabajar con la capacidad de selección y las rutas de acceso lógicas).](working-with-selectability-and-logical-paths.md)

Los archivos se agregan a un componente determinado mediante [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). (Vea [Agregar archivos a componentes).](definition-of-components-by-writers.md)

Al agregar archivos a un componente durante la copia de seguridad, un escritor debe especificar un conjunto de archivos (una ruta de acceso, una especificación de archivo y una marca de recursividad) que defina los archivos de los que se va a realizar una copia de seguridad.

Los escritores también pueden especificar una ruta [*de acceso alternativa*](vssgloss-a.md) para la copia de seguridad, que no debe confundirse con las asignaciones de ubicación [*alternativas mencionadas*](vssgloss-a.md) anteriormente. Esta ruta de acceso alternativa indica una ubicación no predeterminada desde la que se copiarán los archivos cuando se hace una copia de seguridad de un volumen.

La información sobre un componente determinado en el documento de metadatos del escritor se puede obtener a través de una interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) devuelta por [**IVssExgvWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Los archivos y las rutas de acceso se devuelven [**en IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) como [**objetos IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

La información de componentes de un escritor se describe en detalle en [Definición de componentes por escritores.](definition-of-components-by-writers.md)

 

 



