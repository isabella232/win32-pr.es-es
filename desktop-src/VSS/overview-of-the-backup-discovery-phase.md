---
description: Después de llamar a IVssBackupComponents::GatherWriterMetadata, un solicitante usa la instancia de la interfaz IVssAsync devuelta por esta llamada para determinar cuándo todos los escritores del sistema han terminado de construir sus documentos de metadatos de escritor.
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Información general de la fase de detección de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3896abae03f9f2e53d353e5c439a5030c44faba943d4b84a04b564c2eef95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937909"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Información general de la fase de detección de copia de seguridad

Después de llamar a [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)un solicitante usa la instancia de la interfaz [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) devuelta por esta llamada para determinar cuándo todos los escritores del sistema han terminado de construir sus documentos de metadatos de escritor. Para obtener más información, vea [Información general sobre el procesamiento de una copia de seguridad en VSS.](overview-of-processing-a-backup-under-vss.md)

En este momento, el solicitante puede comenzar una fase de detección, examinando los metadatos para determinar qué aplicaciones se están ejecutando y qué volúmenes se deben realizar instantáneas para obtener una copia de seguridad completa. En la tabla siguiente se muestra la secuencia de acciones y eventos necesarios para la fase de detección de copia de seguridad.



| Acción del solicitante                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Evento | Acción de escritor                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Recuperar documentos de metadatos de escritor (vea [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**IVssExwriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | Ninguno  | Durante este período, es posible que los escritores puedan continuar con sus operaciones normales. |
| Use la lista de componentes y sus conjuntos de [*archivos,*](vssgloss-f.md)así como los archivos excluidos, para obtener una lista de volúmenes y archivos implicados en la copia de seguridad (vea [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | None  | None                                                                              |
| Elija los componentes del documento de metadatos del escritor del escritor de los que se va a hacer una copia de seguridad. Llame [**a IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para cada componente para agregarlo al documento Componentes de copia de seguridad. (Vea [Trabajar con la capacidad de selección para la copia de seguridad](working-with-selectability-for-backup.md) y trabajar con el documento componentes de copia de [seguridad).](working-with-the-backup-components-document.md)                                                                                                                      | None  | None                                                                              |
| Inicialice el conjunto de instantáneas, el contexto y compruebe los volúmenes admitidos (vea [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents::IsVolumeSupported).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)                                                                                                                                                                                                                                                                                   | None  | None                                                                              |
| Si realiza una copia de seguridad sin componentes, agregue los volúmenes de destino deseados del documento de metadatos del escritor al conjunto de instantáneas llamando a [**IVssBackupComponents::AddToSnapshotSet para**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) cada volumen. De lo contrario, para los componentes del documento de metadatos del escritor que ya se agregaron al documento componentes de copia de seguridad (mediante una llamada a [**AddComponent),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)el solicitante también debe llamar a **IVssBackupComponents::AddToSnapshotSet para** cada volumen afectado. | None  | None                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Acciones de escritor durante la fase de detección

Dado que la fase de detección de una copia de seguridad consta principalmente de un solicitante que procesa la información que ha recuperado de los documentos de metadatos del escritor, hay pocos requisitos en un escritor.

En teoría, un escritor podría seguir funcionando con normalidad en este momento. Sin embargo, puede ser conveniente que los escritores inicien los preparativos para las próximas operaciones de instantáneas y copia de seguridad.

## <a name="requester-actions-during-the-discovery-phase"></a>Acciones del solicitante durante la fase de detección

Un solicitante usa los objetos [**IVssExgvWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenidos a través de [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para recorrer en iteración todos los metadatos de los escritores y seleccionar los escritores cuyos datos pretende hacer una copia de seguridad.

En este punto, el solicitante deberá generar una lista inicial de los candidatos de copia de seguridad de cada escritor mediante la iteración de los componentes del escritor mediante [**IVssExatingWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Esto proporciona al solicitante objetos [**IVssWMComponent,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) desde los que puede obtener las especificaciones de los archivos de los que se va a realizar una copia de seguridad mediante [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)e [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).

Dado que el objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) puede usar caracteres comodín para contener información de ubicación del archivo, puede ser necesario usar funciones como [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)y [**FindNextFile.**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea)

Hasta que se haya completado la instantánea, todavía es posible que los escritores agreguen o quiten archivos del disco en el curso normal de su trabajo, por lo que no debe generar la lista real de archivos de los que se va a realizar una copia de seguridad en este momento.

En su lugar, la lista inicial de archivos y volúmenes de los que se va a realizar una copia de seguridad se encuentra en este punto haciendo lo siguiente:

1.  Al examinar todos los componentes seleccionables para copia de seguridad y no seleccionables en el documento de [](vssgloss-c.md) metadatos del escritor de cada escritor (con [**IVssExgvWriterMetadata)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)y organizarlos en conjuntos de componentes, se usa la ruta de acceso lógica [*(vea*](vssgloss-l.md) Trabajar con la capacidad de selección y las rutas de acceso lógicas). [](working-with-selectability-and-logical-paths.md)
2.  [*Incluir explícitamente todos*](vssgloss-e.md) los componentes necesarios (no seleccionables para los componentes de copia de seguridad sin seleccionar para los antecesores de copia de seguridad) en el documento Componentes de copia de seguridad mediante [ **IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  Elegir incluir explícitamente opcional seleccionable para los componentes de copia de seguridad que no definen un conjunto de componentes (mediante [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Seleccionar [](vssgloss-c.md) conjuntos de componentes para participar en una copia de seguridad agregando explícitamente su definición seleccionable para el componente de copia de seguridad (mediante [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), que incluye implícitamente los [*subcomponentes*](vssgloss-s.md)del conjunto de componentes . [](vssgloss-i.md)
5.  Con [*la*](vssgloss-f.md) información del conjunto de archivos en el documento de metadatos del escritor seleccionado y las funciones de administración de volúmenes, un solicitante determina las rutas de acceso de los archivos de los que se va a realizar una copia de seguridad y los volúmenes que deban copiarse en la sombra.

Tenga en cuenta que solo los componentes incluidos explícitamente (mediante [**IVssBackupComponents::AddComponent)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)en la copia de seguridad y en el documento Componentes de copia de seguridad tendrán instancias de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) agregadas a ese documento. Estas instancias se usarán para examinar y modificar la configuración de componentes para los componentes incluidos explícitamente y cualquiera de sus subcomponentes incluidos implícitamente (vea [Selectability y Working with Component Properties](selectability-and-working-with-component-properties.md)).

Si un escritor incluye cualquiera de los componentes de un escritor, debe agregar todos sus componentes necesarios. Sin embargo, un solicitante también puede omitir completamente todos los conjuntos de componentes de un escritor. Si no se selecciona explícitamente ninguno de los componentes de un sistema de escritura, el escritor no se selecciona y VSS impide que ese escritor participe en el resto de la operación de copia de seguridad.

El solicitante inicia el conjunto de instantáneas que contendrá los volúmenes seleccionados llamando a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Si el volumen puede participar en una instantánea (que se puede comprobar con [**IVssBackupComponents::IsVolumeSupported),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)el solicitante puede agregar ese volumen al conjunto de instantáneas mediante [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Aunque no suele ser útil, a veces un [](vssgloss-p.md) solicitante también puede elegir qué proveedor mantendrá la instantánea de un volumen determinado (consulte [Selección de](selecting-providers.md) proveedores para obtener más información).

Se debe tener cuidado con el control de un volumen que contiene carpetas montadas o puntos de rean aproximado. Puede aparecer una carpeta montada o un punto de reanco en una instantánea y se puede realizar una copia de seguridad. Sin embargo, no se puede atravesar una carpeta montada o un punto de reanual en el volumen copiado en la sombra (vea Trabajar con carpetas montadas y [puntos de reanual).](working-with-reparse-and-mount-points.md)

En este punto de la copia de seguridad, el documento componentes de copia de seguridad se inicializa y rellena. En operaciones futuras, los escritores y solicitantes pueden usar la [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para comunicarse entre sí.

A los escritores se les proporciona acceso a la [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) al controlar los eventos [*PrepareForBackup,*](vssgloss-p.md) [*PostSnapshot*](vssgloss-p.md)y [*BackupComplete.*](vssgloss-b.md)

 

 
