---
description: Cuando la instalación de una aplicación existente se mueve a Windows Installer desde otra tecnología de instalación, el desarrollador del programa de instalación puede empezar a crear un paquete de Windows Installer mediante las imágenes de archivo de origen y de destino de la instalación existente.
ms.assetid: 8b0fb473-e19f-4427-b2a1-d0721cde9d38
title: Planeación de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb98368c5c5c8e13a8f9b03a44805a8cff6e517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910702"
---
# <a name="planning-the-installation"></a>Planeación de la instalación

Cuando la instalación de una aplicación existente se mueve a Windows Installer desde otra tecnología de instalación, el desarrollador del programa de instalación puede empezar a crear un paquete de Windows Installer mediante las imágenes de archivo de origen y de destino de la instalación existente. Un plan detallado de cómo se organizan los archivos y otros recursos en el origen y el destino también es un buen punto de partida para desarrollar un paquete para una nueva aplicación.

El paquete de instalación de ejemplo toma los siguientes archivos que se almacenan en la ubicación de origen de la aplicación y los instala en el destino en el equipo del usuario.



| Archivo         | Descripción                               | Ruta de acceso al origen                                    | Ruta de acceso al destino                                          |
|--------------|-------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe  | Archivo ejecutable del editor de texto.              | C: \\Redpark.exe del Bloc de notas de ejemplo \\ \\                  | \[Redpark.exe en el \] \\ \_ estacionamiento rojo \\          |
| Readme.txt   | Un archivo informativo.                    | C: \\Readme.txt del Bloc de notas de ejemplo \\ \\                   | \[Readme.txt en el \] \\ \_ estacionamiento rojo \\           |
| Help.txt     | Manual de ayuda                               | C: \\Help.txt del Bloc de notas de ejemplo \\ \\                     | No instalado. Siempre ejecute desde el origen.                  |
| Baseball.txt | Programa de juegos de béisbol del año 2000.     | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Baseball.txt         | \[\] \\Baseball.txt para \_ deportes de estacionamiento rojo \\ \\ |
| Football.txt | Programa de juegos de fútbol del año 2000.     | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Football.txt         | \[\] \\Football.txt para \_ deportes de estacionamiento rojo \\ \\ |
| Dance.txt    | Rendimiento de baile del año 2000.         | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Dance.txt            | \[\] \\ \_Dance.txt artes de estacionamiento rojo \\ \\      |
| Concert.txt  | Rendimiento de música del año 2000.         | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Concert.txt          | \[\] \\ \_Concert.txt artes de estacionamiento rojo \\ \\    |
| January.txt  | Admisiones en enero del año 2000.       | C: \\ \\January.txt puerta de Bloc de notas de ejemplo \\ \\            | \[January.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\    |
| NewYears.txt | Admisiones en los nuevos años del año 2000. | C: \\ ejemplo de \\ festividad de puerta de Bloc de notas \\ \\ \\NewYears.txt | \[NewYears.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\   |



 

El ejemplo escribe los siguientes valores en el registro del usuario en **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Notepad Sample**.



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



 

En el ejemplo se instalan los siguientes métodos abreviados. Se puede seleccionar uno de estos métodos abreviados durante la instalación como un acceso directo anunciado para que el usuario pueda instalar la característica de béisbol a petición.



| Nombre      | Ubicación de acceso directo                         | Destino de acceso directo                                         |
|-----------|-------------------------------------------|---------------------------------------------------------|
| sNotepad  | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Redpark.exe en el \] \\ \_ estacionamiento rojo \\          |
| sReadme   | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Readme.txt en el \] \\ \_ estacionamiento rojo \\           |
| sHelp     | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[ProgramFilesFolder \] \\ ejemplo del \\ bloc de notas \\Help.txt       |
| sBaseball | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\Baseball.txt para \_ deportes de estacionamiento rojo \\ \\ |
| sFootball | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\Football.txt para \_ deportes de estacionamiento rojo \\ \\ |
| sDance    | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\ \_Dance.txt artes de estacionamiento rojo \\ \\      |
| sConcert  | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\ \_Concert.txt artes de estacionamiento rojo \\ \\    |
| sJanuary  | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[January.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\    |
| sNewYears | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[NewYears.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\   |



 

Para reproducir el ejemplo, empiece por crear la estructura de directorio de origen que se indica en la primera tabla. Puede hacer una copia del archivo de Notepad.exe del sistema y, a continuación, cambiar el nombre de esta copia Redpark.exe. Use el editor del Bloc de notas para crear los archivos de texto restantes. La estructura de directorios del destino, los valores del registro y los métodos abreviados se agregan mediante la creación de la base de datos de instalación.

[Continuar](importing-a-blank-database.md)

 

 



