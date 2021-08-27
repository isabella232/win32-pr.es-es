---
description: Hay ciertas circunstancias en las que los archivos de los que se va a realizar una copia de seguridad no son la ubicación predeterminada de esos archivos.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Trabajar con rutas de acceso alternativas durante la copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bc969c96d943b73a8a9d9609f004b4a0f738c46802af20a7dff22e34ebac56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124455"
---
# <a name="working-with-alternate-paths-during-backup"></a>Trabajar con rutas de acceso alternativas durante la copia de seguridad

Hay ciertas circunstancias en las que los archivos de los que se va a realizar una copia de seguridad no son la ubicación predeterminada de esos archivos.

Por ejemplo, algunos escritores no pueden garantizar que se han vaciado sus datos dentro del período de tiempo entre los eventos [*Freeze*](vssgloss-f.md) y [*Thaw.*](vssgloss-t.md) Estos escritores pueden optar por generar archivos duplicados que contengan una última configuración correcta conocida en un directorio de origen no predeterminado o una [*ruta de acceso alternativa.*](vssgloss-a.md)

El término ruta de acceso alternativa, como se usa con VSS, no debe confundirse con el término [*asignación de ubicación alternativa.*](vssgloss-a.md) Las rutas de acceso alternativas solo se usan durante las operaciones de copia de seguridad y hacen referencia a un origen alternativo del que se va a realizar una copia de seguridad. Las asignaciones de ubicación alternativas solo se usan durante las operaciones de restauración y hacen referencia a un destino alternativo para las operaciones de restauración.

**Para usar una ruta de acceso alternativa durante la copia de seguridad**

1.  Durante la fase de detección de una operación de copia de seguridad (vea Información general de la fase de detección de copia de [seguridad),](overview-of-the-backup-discovery-phase.md)un solicitante examinaría los datos de componentes de cada escritor mediante [**IVssExgvWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) y obtenería instancias de la [**interfaz IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
2.  A continuación, un [](vssgloss-f.md) solicitante obtiene el conjunto de archivos administrado por cada componente, representado por instancias de la interfaz [**IVssWMFiledesc,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) llamando al método [**IVssWMComponent::GetFile.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)
3.  Además de una ruta de acceso ([**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), una especificación de archivo ([**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) y una marca de [**recursividad ( IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), un objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) puede contener una ubicación alternativa (que se usa como ruta de acceso alternativa para las operaciones de copia de seguridad y una asignación de ubicación alternativa para las operaciones de restauración) mediante el método [**IVssWMFiledesc::GetAlternateLocation.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)
4.  Si el valor devuelto por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) no es NULL, las aplicaciones de copia de seguridad usan ese valor en lugar del valor obtenido de [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) para seleccionar y buscar archivos de los que se va a realizar una copia de seguridad.
5.  A pesar de usar una ruta de acceso alternativa, los solicitantes deben seguir respetando la especificación de archivo y la configuración recursiva devuelta por [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) e [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Tenga en cuenta que, en la restauración, cualquier ruta de acceso alternativa, es decir, una ubicación alternativa devuelta por una instancia de [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) obtenida de una instancia de [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), que a su vez se obtuvo de una instancia de [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenida al recuperar un documento de metadatos de escritor almacenado, no se usa durante la restauración.

La ruta de acceso predeterminada (devuelta por el método [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) de la misma instancia de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) se usa para definir una ubicación de restauración o una asignación de ubicación alternativa (que se encuentra mediante el método [**IVssWMFiledesc::GetAlternateLocation)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) indica dónde se va a restaurar un archivo (vea Trabajar con ubicaciones alternativas durante la restauración). [](working-with-alternate-locations-during-restore.md)

 

 



