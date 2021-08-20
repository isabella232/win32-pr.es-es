---
description: Un conjunto de copia de seguridad es una lista de todos los archivos de los que se va a realizar una copia de seguridad, sus ubicaciones y cómo realizar una copia de seguridad de ellos.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Generar un conjunto de copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120643c827afdabfbb9a2c347fa16290e03969f0e87f913b0c5d9fdb682f2619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122128"
---
# <a name="generating-a-backup-set"></a>Generar un conjunto de copia de seguridad

Un conjunto de copia de seguridad es una lista de todos los archivos de los que se va a realizar una copia de seguridad, sus ubicaciones y cómo realizar una copia de seguridad de ellos.

Un solicitante debe hacer uso de los archivos contenidos en los volúmenes instantáneados después de que [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) devuelva correctamente para generar la lista completa de archivos de los que se va a realizar una copia de seguridad.

Además, un solicitante debe tratar la posibilidad [](vssgloss-a.md) de que algunos archivos tengan rutas de acceso alternativas y que algunos archivos se hayan excluido.

Un algoritmo para seleccionar los archivos de [](vssgloss-w.md) los que se va a realizar una copia de seguridad debe ir en una instancia de escritor por instancia de escritor, componente a componente (como será el caso durante la restauración; vea [Generación](generating-a-restore-set.md)de un conjunto de restauración) y puede continuar haciendo lo siguiente:

1.  Determinar los volúmenes que contienen los archivos del escritor y los objetos de dispositivo correspondientes
2.  Usar [](vssgloss-f.md) la información del conjunto de archivos (contenida en los objetos [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) devueltos por [**IVssExgvWriterMetadata::GetExcludeFile)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)para crear una lista de los archivos excluidos explícitamente, si es necesario mediante **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.
3.  Iteración de todos los componentes de un escritor mediante [**IVssExxiaWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Si se selecciona un componente seleccionable, use la ruta [*de*](vssgloss-l.md) acceso lógica para obtener los componentes no seleccionables asociados a él en un conjunto de componentes. (Vea [Trabajar con la capacidad de selección y las rutas de acceso lógicas).](working-with-selectability-and-logical-paths.md)
4.  Obtener los conjuntos [*de archivos*](vssgloss-f.md) contenidos en cada componente seleccionado mediante la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondiente a cada componente que contiene.
5.  Generación de una lista de archivos a partir de las especificaciones, si es necesario mediante **FindFileFirst**, **FindFileFirstEx** y **FindNextFile**.
6.  Comprobar cada archivo de la lista generado a partir de la información del componente con la lista de archivos excluidos generados anteriormente. Esto debe hacerse mediante la ruta de acceso predeterminada para el archivo (devuelta por [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), no por la ruta de acceso alternativa devuelta por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Si el archivo coincide con la lista excluida, no se realizará una copia de seguridad.
7.  Elección de la ubicación real desde la que se va a hacer una copia de seguridad (mediante la ruta de acceso alternativa si se estableció)
8.  En este momento, hay disponible una lista completa de archivos y sus ubicaciones, y puede comenzar una copia de seguridad.

Después de generar un conjunto de copia de seguridad inicial para todos los escritores que están presentes en el sistema, el solicitante comprueba la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

El solicitante usa las subclaves de esta clave como se muestra a continuación:

-   Si un escritor está presente en el sistema y hay una subclave cuyo nombre coincide con el nombre del escritor, esa subclave debe omitirse.
-   Si un escritor estaba presente en el sistema pero actualmente no está presente en el conjunto de copia de seguridad y hay una subclave correspondiente, los archivos especificados en los datos de subclave se excluyen y deben quitarse del conjunto de copia de seguridad.
-   La aplicación de copia de seguridad agrega archivos a los datos de subclave mediante la creación de un valor MULTI SZ que contiene una lista de especificaciones de archivo para los archivos de los que no se debe realizar una copia \_ de seguridad. Cada cadena del valor MULTI \_ SZ debe contener una especificación de archivo.
-   Las especificaciones de archivo pueden contener ? y \* caracteres comodín. Una especificación se puede hacer recursiva anexando /s al final. Por ejemplo, la especificación de "%TEMP% /s" hace que no se haga una copia de seguridad de todos los archivos del directorio %TEMP% y de todos sus \\ \* subdirectorios.

 

 



