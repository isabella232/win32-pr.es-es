---
description: Existen ciertas circunstancias en las que los archivos de los que se va a hacer una copia de seguridad no son la ubicación predeterminada de esos archivos.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Trabajar con rutas de acceso alternativas durante la copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696433"
---
# <a name="working-with-alternate-paths-during-backup"></a>Trabajar con rutas de acceso alternativas durante la copia de seguridad

Existen ciertas circunstancias en las que los archivos de los que se va a hacer una copia de seguridad no son la ubicación predeterminada de esos archivos.

Por ejemplo, algunos escritores no pueden garantizar que se vacíen sus datos en el período de tiempo entre los eventos [*Freeze*](vssgloss-f.md) y [*reanudar*](vssgloss-t.md) . Estos escritores pueden optar por generar archivos duplicados que contengan la última configuración válida conocida en un directorio de origen no predeterminado o en una [*ruta de acceso alternativa*](vssgloss-a.md).

El término ruta de acceso alternativa, tal y como se usa con VSS, no se debe confundir con el término [*asignación de ubicación alternativa*](vssgloss-a.md). Las rutas de acceso alternativas solo se usan durante las operaciones de copia de seguridad y hacen referencia a un origen alternativo del que se va a realizar la copia de seguridad. Las asignaciones de ubicación alternativas solo se usan durante las operaciones de restauración y hacen referencia a un destino alternativo para las operaciones de restauración.

**Para usar una ruta de acceso alternativa durante la copia de seguridad**

1.  Durante la fase de detección de una operación de copia de seguridad (consulte [información general de la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md)), un solicitante examinaría los datos de los componentes de cada escritor mediante [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) y obtener las instancias de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .
2.  A continuación, un solicitante obtiene el [*conjunto de archivos*](vssgloss-f.md) administrado por cada componente, representado por instancias de la interfaz [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) , llamando al método [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) .
3.  Además de una ruta de acceso ([**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), una especificación de archivo ([**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) y una marca de recursividad ([**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), un objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) puede contener una ubicación alternativa (usada como ruta de acceso alternativa para las operaciones de copia de seguridad y una asignación de ubicación alternativa para las operaciones de restauración) mediante el método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) .
4.  Si el valor devuelto por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no es null, las aplicaciones de copia de seguridad usan ese valor en lugar del valor obtenido de [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) para seleccionar y buscar los archivos de los que se va a realizar la copia de seguridad.
5.  A pesar de usar una ruta de acceso alternativa, los solicitantes deben respetar la especificación de archivo y la configuración recursiva devuelta por [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) y [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Tenga en cuenta que, en la restauración, cualquier ruta alternativa, es decir, una ubicación alternativa devuelta por una instancia de [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) procedente de una instancia de [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), que a su vez se obtuvo de una instancia de [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenida al recuperar un documento de metadatos del escritor almacenado, no se utiliza durante la restauración.

La ruta de acceso predeterminada (devuelta por el método [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) de la misma instancia de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) se usa para definir una ubicación de restauración, o una asignación de ubicación alternativa, que se encuentra mediante el método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) , indica dónde se debe restaurar un archivo (vea [trabajar con ubicaciones alternativas durante la restauración](working-with-alternate-locations-during-restore.md)).

 

 



