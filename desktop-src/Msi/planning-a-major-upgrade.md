---
description: Si Windows instalador se usa para la instalación y configuración de una aplicación, las actualizaciones posteriores de esa aplicación se pueden controlar mediante la instalación de un paquete de actualización.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planear una actualización principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07ece8acf0dbc37ecdfddaa3505e5e54a283a8e8efd7b4eb0dc1a0a365a461e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377376"
---
# <a name="planning-a-major-upgrade"></a>Planear una actualización principal

Si Windows instalador se usa para la instalación y configuración de una aplicación, las actualizaciones posteriores de esa aplicación se pueden controlar mediante la instalación de un paquete de actualización. Los desarrolladores de instalación pueden optar por crear un paquete de actualización modificando el paquete de instalación original. Este enfoque se ilustra en el siguiente ejemplo de actualización.

La instalación del producto original, MNP2000, seguida de la instalación del paquete de actualización proporciona al usuario los siguientes archivos requeridos por el producto MNP2001.



| Archivo          | Descripción                                                    | Ruta de acceso al origen                                    | Ruta de acceso al destino                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Archivo ejecutable del editor de texto. Sin cambios con respecto a los productos anteriores. | C: \\ Ejemplo \\ Bloc de notas \\Redpark.exe                  | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe          |
| Readme.txt    | Un archivo de información. Sin cambios con respecto a los productos anteriores.         | C: \\ Ejemplo \\ Bloc de notas \\Readme.txt                   | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt           |
| Help.txt      | Manual de ayuda. Sin cambios con respecto a los productos anteriores.                 | C: \\ Ejemplo \\ Bloc de notas \\Help.txt                     | No instalado. Ejecutar siempre desde el origen.                  |
| Baseba01.txt  | Programación de juegos de béisbol para el año 2001.                          | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Baseba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseball.txt |
| Footba01.txt  | Programación del partido de fútbol para el año 2001.                          | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Footba01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Football.txt |
| Basket01.txt  | Programación de juegos de calendario para el año 2001.                        | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Basket01.txt         | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basket01.txt |
| Dance01.txt   | Presentaciones de performance para el año 2001.                              | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Dance01.txt          | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Dance.txt \\      |
| Concert01.txt | Música rendimientos del año 2001.                              | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Concer01.txt         | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concert.txt \\    |
| Opera01.txt   | Representaciones de Opera del año 2001.                              | C: \\ Ejemplo de Bloc de notas eventos \\ \\ \\Opera01.txt          | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Opera01.txt \\    |
| Januar01.txt  | Admisiones en enero del año 2001.                            | C: \\ Ejemplo de Bloc de notas puerta \\ \\ \\Januar01.txt           | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\January.txt    |
| NewYea01.txt  | Admisiones el Día de los Nuevos Años del año 2001.                      | C: \\ Ejemplo de Bloc de notas días \\ \\ \\ festivos de \\NewYea01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYears.txt   |
| Memori01.txt  | Admisiones en el Día de la Noche del año 2001.                       | C: \\ Ejemplo de Bloc de notas días \\ \\ \\ festivos de \\Memori01.txt | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt   |



 

La instalación del paquete de actualización quita todas las características instaladas con el producto original que el producto actualizado no está utilizando.

Por ejemplo, al actualizar desde MNP2000, la instalación de la actualización quita los siguientes archivos del equipo del usuario:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

La instalación del paquete de actualización escribe los siguientes valores en el registro del usuario en:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Bloc de notas Sample**



| Nombre             | Valor    |
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



 

La actualización actualiza los accesos directos antiguos a los siguientes accesos directos. Uno de estos accesos directos se puede seleccionar durante la instalación como un acceso directo anunciado para que el usuario pueda instalar a petición la característica Baseball.



| Nombre        | Ubicación del acceso directo                         | Destino de acceso directo                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Redpark.exe            |
| sReadme     | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park \_ \\Readme.txt             |
| sHelp       | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[Ejemplo programFilesFolder \] \\ \\ Bloc de notas \\Help.txt         |
| sBaseball   | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Baseba01.txt   |
| sFootball   | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Footba01.txt   |
| sBasketball | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Sports \_ \\ \\Basketba01.txt |
| sDance      | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Dance01.txt \\      |
| sConcert    | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Concer01.txt \\     |
| sOpera      | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Park \_ \\Opera01.txt \\      |
| sJanuary    | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Januar01.txt     |
| sNewYears   | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\NewYea01.txt     |
| sMemorial   | \[Menú ProgramFilesFolder \] \\ Red \_ Park \\\\ | \[ProgramFilesFolder \] \\ Red Park Gate \_ \\ \\Memori01.txt     |



 

Cuando un usuario desinstala el paquete de actualización, Windows Instalador quita completamente todas las versiones del producto del equipo del usuario. El usuario no se queda con ninguna parte de MNP2000 o MNP2001.

[Continuar](importing-original-installation-database.md)

 

 



