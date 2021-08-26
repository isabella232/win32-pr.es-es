---
description: Cuando la instalación de una aplicación existente se mueve a Windows Installer desde otra tecnología de instalación, el desarrollador del programa de instalación puede empezar a crear un paquete de Windows Installer mediante las imágenes de archivo de origen y de destino de la instalación existente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planear la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d406ec97fd5edb34468586eb9f707eff32b289df3dc88b803b8c55d4aad10cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042365"
---
# <a name="planning-the-installation"></a>Planear la instalación

Cuando la instalación de una aplicación existente se mueve a Windows Installer desde otra tecnología de instalación, el desarrollador del programa de instalación puede empezar a crear un paquete de Windows Installer mediante las imágenes de archivo de origen y de destino de la instalación existente. Un plan detallado de cómo se organizan los archivos y otros recursos en el origen y el destino también es un buen punto de partida para desarrollar un paquete para una nueva aplicación.

El paquete de instalación de ejemplo toma los siguientes archivos que se almacenan en la ubicación de origen de la aplicación y los instala en el destino en el equipo del usuario.



| Archivo         | Descripción                               | Ruta de acceso al origen                                    | Ruta de acceso al destino                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Archivo ejecutable del editor de texto.              | C: \\ Ejemplo \\ Bloc de notas \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt   | Un archivo informativo.                    | C: \\ Ejemplo \\ Bloc de notas \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt     | Manual de ayuda                               | C: \\ Ejemplo \\ Bloc de notas \\Help.txt                     | No instalado. Ejecutar siempre desde el origen.                  |
| Baseball.txt | Programación de juegos de béisbol para el año 2000.     | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Baseball.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Football.txt | Programación del partido de fútbol para el año 2000.     | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Football.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Dance.txt    | Rendimientos de la música para el año 2000.         | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Dance.txt            | \[ProgramFilesFolder \] \\ Red Park Park \_ Park \\Dance.txt \\      |
| Concert.txt  | Música rendimientos del año 2000.         | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Concert.txt          | \[ProgramFilesFolder \] \\ Red Park Park \_ Park \\Concert.txt \\    |
| January.txt  | Admisiones en enero del año 2000.       | C: \\ Ejemplo de Bloc de notas puerta \\ \\ \\January.txt            | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYears.txt | Admisiones el día de los años nuevos del año 2000. | C: \\ Ejemplo de Bloc de notas días \\ \\ \\ festivos de \\NewYears.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

El ejemplo escribe los siguientes valores en el registro del usuario en **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Bloc de notas \_ \\ \\ \\ Sample**.



| Nombre             | Value    |
|------------------|----------|
| lfCharSet        | 0        |
| lfClipPrecision  | 2        |
| lfFaceName       | FixedSys |
| lfItalic         | 0        |
| lfOrientation    | 0        |
| lfOutPrecision   | 1        |
| fSavePageSetting | 0        |
| lfPitchAndFamily | 49       |
| iPointSize       | 120      |
| lfQuality        | 2        |
| lfStrikeOut      | 0        |
| lfWeight         | 400      |
| fWrap            | 0        |



 

En el ejemplo se instalan los siguientes accesos directos. Uno de estos accesos directos se puede seleccionar durante la instalación como un acceso directo anunciado para que el usuario pueda instalar a petición la característica Baseball.



| Nombre      | Ubicación del acceso directo                         | Destino de acceso directo                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| sReadme   | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| sHelp     | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[Ejemplo programFilesFolder \] \\ \\ Bloc de notas \\Help.txt       |
| sBaseball | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| sFootball | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| sDance    | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ Park \\Dance.txt \\      |
| sConcert  | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concert.txt \\    |
| sJanuary  | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| sNewYears | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |



 

Para reproducir el ejemplo, empiece por crear la estructura de directorios de origen que se proporciona en la primera tabla. Puede realizar una copia del archivo de Notepad.exe sistema y, a continuación, cambiar el nombre de esta copia Redpark.exe. Use el editor Bloc de notas para crear los archivos de texto restantes. La estructura de directorios del destino, los valores del Registro y los accesos directos se agregan mediante la creación de la base de datos de instalación.

[Continuar](importing-a-blank-database.md)

 

 



