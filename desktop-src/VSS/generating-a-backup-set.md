---
description: Un conjunto de copia de seguridad es una lista de todos los archivos de los que se va a realizar una copia de seguridad, sus ubicaciones y cómo realizar copias de seguridad de los mismos.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Generar un conjunto de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697018"
---
# <a name="generating-a-backup-set"></a>Generar un conjunto de copia de seguridad

Un conjunto de copia de seguridad es una lista de todos los archivos de los que se va a realizar una copia de seguridad, sus ubicaciones y cómo realizar copias de seguridad de los mismos.

Un solicitante debe hacer uso de los archivos contenidos en los volúmenes de copia sombra después de que el [**osnapshotset de IVssBackupComponents::D**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) se devuelva correctamente para generar la lista completa de archivos de los que se va a hacer una copia de seguridad.

Además, un solicitante debe afrontar la posibilidad de que algunos archivos tengan rutas de acceso [*alternativas*](vssgloss-a.md) y que se hayan excluido algunos archivos.

Un algoritmo para seleccionar archivos de los que se va a realizar una copia de seguridad debe estar en una [*instancia de escritor*](vssgloss-w.md) por instancia de escritor, componente por componente (como será el caso durante la restauración; vea [generar un conjunto de restauración](generating-a-restore-set.md)) y puede continuar haciendo lo siguiente:

1.  Determinar los volúmenes que contienen los archivos del escritor y los objetos de dispositivo correspondientes
2.  Usar la información del [*conjunto de archivos*](vssgloss-f.md) (contenida en los objetos [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devueltos por [**IVssExamineWriterMetadata:: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)) para crear una lista de los archivos excluidos explícitamente, si es necesario, mediante **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.
3.  Recorrer en iteración todos los componentes de un escritor mediante [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Si se selecciona un componente seleccionable, utilice la [*ruta de acceso lógica*](vssgloss-l.md) para obtener los componentes no seleccionables asociados a él en un conjunto de componentes. (Vea [trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)).
4.  Obtener los [*conjuntos de archivos*](vssgloss-f.md) contenidos en cada componente seleccionado mediante la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondiente a cada componente que contiene.
5.  Generar una lista de archivos a partir de las especificaciones, si es necesario, mediante **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.
6.  Comprobando cada archivo de la lista que se genera a partir de la información del componente en la lista de archivos excluidos generados anteriormente. Esto se debe hacer mediante la ruta de acceso predeterminada del archivo (devuelta por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), no por la ruta de acceso alternativa devuelta por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Si el archivo coincide con la lista de exclusión, no se incluirá en la copia de seguridad.
7.  Elección de la ubicación real desde la que se realizará la copia de seguridad (mediante la ruta alternativa si se estableció)
8.  En este momento, hay disponible una lista completa de archivos y sus ubicaciones y se puede iniciar una copia de seguridad.

Una vez que se ha generado un conjunto de copia de seguridad inicial para todos los escritores que están presentes en el sistema, el solicitante comprueba la siguiente clave del registro:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ BackupRestore \\ FilesNotToBackup**

El solicitante utiliza las subclaves de esta clave de la siguiente manera:

-   Si hay un escritor presente en el sistema y hay una subclave cuyo nombre coincide con el nombre del sistema de escritura, esa subclave debe omitirse.
-   Si un escritor estaba presente en el sistema pero no está presente en el conjunto de copia de seguridad y hay una subclave coincidente, se excluyen los archivos especificados en los datos de la subclave y se deben quitar del conjunto de copia de seguridad.
-   La aplicación de copia de seguridad agrega archivos a los datos de la subclave creando un \_ valor multisz que contiene una lista de especificaciones de archivo para los archivos de los que no se debe hacer una copia de seguridad. Cada cadena del \_ valor multisz debe contener una especificación de archivo.
-   Las especificaciones de archivo pueden contener el y \* caracteres comodín. Una especificación se puede hacer recursiva anexando/s al final. Por ejemplo, si se especifica "% TEMP% \\ \* /s", no se realizará la copia de seguridad de todos los archivos del directorio% Temp% y de todos sus subdirectorios.

 

 



