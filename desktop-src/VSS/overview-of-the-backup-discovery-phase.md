---
description: 'Después de llamar a IVssBackupComponents:: GatherWriterMetadata, un solicitante utiliza la instancia de la interfaz IVssAsync devuelta desde esta llamada para determinar cuándo todos los escritores del sistema han terminado de crear los documentos de metadatos del escritor.'
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Información general de la fase de detección de copias de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d2a2d05220ecf3e25c77c18cc62b07726964f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696985"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Información general de la fase de detección de copias de seguridad

Después de llamar a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un solicitante utiliza la instancia de la interfaz [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) devuelta desde esta llamada para determinar cuándo todos los escritores del sistema han terminado de crear los documentos de metadatos del escritor. Para obtener más información, vea [información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md).

En este momento, el solicitante puede comenzar una fase de detección, examinando los metadatos para determinar qué aplicaciones se están ejecutando y a qué volúmenes se deben crear instantáneas para obtener una copia de seguridad completa. En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para la fase de detección de copias de seguridad.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Evento | Acción del escritor                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Recuperar documentos de metadatos del escritor (vea [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | None  | Durante este período, los escritores pueden continuar con sus operaciones normales. |
| Use la lista de componentes y sus [*conjuntos de archivos*](vssgloss-f.md), así como archivos excluidos, para obtener una lista de los volúmenes y archivos implicados en la copia de seguridad (vea [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | None  | None                                                                              |
| Elija los componentes del documento de metadatos del escritor del escritor de los que desea realizar copias de seguridad. Llame a [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para cada componente para agregarlo al documento componentes de copia de seguridad. (Vea [trabajar con la selección para realizar copias de seguridad](working-with-selectability-for-backup.md) y [trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)).                                                                                                                      | None  | None                                                                              |
| Inicialice el conjunto de instantáneas, el contexto y compruebe los volúmenes admitidos (consulte [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)).                                                                                                                                                                                                                                                                                   | None  | None                                                                              |
| Si realiza una copia de seguridad que no sea un componente, agregue los volúmenes de destino deseados del documento de metadatos del escritor al conjunto de instantáneas llamando a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para cada volumen. De lo contrario, para los componentes del documento de metadatos del escritor que ya se agregaron al documento componentes de copia de seguridad (llamando a [**AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), el solicitante también debe llamar a **IVssBackupComponents:: AddToSnapshotSet** para cada volumen afectado. | None  | None                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Acciones del escritor durante la fase de detección

Dado que la fase de detección de una copia de seguridad se compone principalmente de un solicitante que procesa la información que ha recuperado de los documentos de metadatos del escritor, existen pocos requisitos en un escritor.

En teoría, un escritor podría continuar ejecutándose normalmente en este momento. Sin embargo, puede ser conveniente que los escritores inicien los preparativos de las operaciones de copia de seguridad y de instantáneas.

## <a name="requester-actions-during-the-discovery-phase"></a>Acciones del solicitante durante la fase de detección

Un solicitante usa los objetos [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenidos a través de [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para recorrer en iteración todos los metadatos de los escritores y seleccionar aquellos escritores cuyos datos se van a copiar.

En este momento, el solicitante tendrá que generar una lista inicial de los candidatos de copia de seguridad de cada escritor mediante la iteración de los componentes del escritor mediante [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Esto proporciona al solicitante los objetos [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) , desde los que puede obtener las especificaciones de los archivos de los que se va a realizar una copia de seguridad mediante [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)y [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).

Dado que el objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) puede usar caracteres comodín para almacenar información de ubicación de archivos, puede que sea necesario usar funciones como [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)y [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea).

Hasta que se haya completado la instantánea, aún es posible que los escritores agreguen o quiten archivos del disco en el curso normal de su trabajo, por lo que no debe generar la lista real de archivos de los que se va a realizar la copia de seguridad en este momento.

En su lugar, se puede encontrar la lista inicial de archivos y volúmenes de los que se va a hacer una copia de seguridad en este momento; para ello, haga lo siguiente:

1.  Examinar todos los elementos seleccionables para la copia de seguridad y los componentes no seleccionables en el documento de metadatos del escritor de cada escritor (mediante [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) y organizarlos en [*conjuntos de componentes*](vssgloss-c.md) usar la [*ruta de acceso lógica*](vssgloss-l.md) (vea [trabajar con rutas de acceso lógicas y de selección](working-with-selectability-and-logical-paths.md))
2.  [*Inclusión explícita*](vssgloss-e.md) de todos los componentes necesarios (no seleccionables para componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad) en el documento componentes de copia de seguridad mediante [ **IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  Elegir incluir explícitamente opcionalmente seleccionable para componentes de copia de seguridad que no definen un conjunto de componentes (mediante [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Al [*seleccionar conjuntos de componentes*](vssgloss-c.md) para participar en una copia de seguridad, se agrega explícitamente su definición seleccionable para el componente de copia de seguridad (mediante [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), que [*incluye implícitamente*](vssgloss-i.md) los [*subcomponentes*](vssgloss-s.md)del conjunto de componentes.
5.  El uso de información de [*conjunto de archivos*](vssgloss-f.md) en las funciones de administración de volúmenes y de documentos de metadatos del escritor de escritores seleccionados, un solicitante determina las rutas de acceso de los archivos de los que se va a realizar la copia de seguridad y los volúmenes en los que será necesario realizar instantáneas.

Tenga en cuenta que solo los componentes incluidos explícitamente (mediante [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) en la copia de seguridad y en el documento componentes de copia de seguridad tendrán instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) agregada a ese documento. Estas instancias se utilizarán para examinar y modificar la configuración de componentes para los componentes incluidos explícitamente y cualquiera de sus subcomponentes incluidos implícitamente (consulte [selección y trabajo con propiedades de componentes](selectability-and-working-with-component-properties.md)).

Si un escritor incluye alguno de los componentes de un escritor, debe agregar todos sus componentes necesarios. Sin embargo, un solicitante también puede omitir por completo todos los conjuntos de componentes de un escritor. Si ninguno de los componentes de un escritor se selecciona explícitamente, el escritor no está seleccionado y VSS impide que el escritor participe en el resto de la operación de copia de seguridad.

El solicitante inicia el conjunto de instantáneas que contendrá los volúmenes seleccionados mediante una llamada a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si el volumen puede participar en una instantánea (que se puede comprobar con [**ivssbackupcomponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)), el solicitante puede agregar ese volumen al conjunto de instantáneas mediante [**Ivssbackupcomponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Aunque no suele ser útil, un solicitante también puede elegir a veces qué [*proveedor*](vssgloss-p.md) mantendrá la instantánea para un volumen determinado (consulte [selección de proveedores](selecting-providers.md) para obtener más información).

Se debe tener cuidado con el control de un volumen que contenga carpetas montadas o puntos de reanálisis. Una carpeta montada o un punto de análisis puede aparecer en una instantánea y se puede hacer una copia de seguridad de ella. Sin embargo, no se puede atravesar una carpeta montada o un punto de reanálisis en el volumen de la instantánea (vea [trabajar con carpetas montadas y puntos de análisis](working-with-reparse-and-mount-points.md)).

En este punto de la copia de seguridad, se inicializa y rellena el documento componentes de copia de seguridad. En futuras operaciones, los escritores y los solicitantes pueden usar la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para comunicarse entre sí.

Los escritores reciben acceso a la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) al controlar los eventos [*PrepareForBackup*](vssgloss-p.md), [*postsnapshot*](vssgloss-p.md)y [*BackupComplete*](vssgloss-b.md) .

 

 
