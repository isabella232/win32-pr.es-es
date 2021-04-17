---
description: Si se usa Windows Installer para la instalación y la configuración de una aplicación, las actualizaciones posteriores de esa aplicación se pueden administrar mediante la instalación de un paquete de actualización.
ms.assetid: 69ad4928-e750-47c2-8668-c9e3deff8066
title: Planeación de una actualización importante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ca6b82e53a38dde8131525eb885a5f17603ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652789"
---
# <a name="planning-a-major-upgrade"></a>Planeación de una actualización importante

Si se usa Windows Installer para la instalación y la configuración de una aplicación, las actualizaciones posteriores de esa aplicación se pueden administrar mediante la instalación de un paquete de actualización. Los desarrolladores de instalación pueden optar por crear un paquete de actualización modificando el paquete de instalación original. Este enfoque se ilustra en el siguiente ejemplo de actualización.

La instalación del producto original, MNP2000, seguida de la instalación del paquete de actualización proporciona al usuario los siguientes archivos requeridos por el producto MNP2001.



| Archivo          | Descripción                                                    | Ruta de acceso al origen                                    | Ruta de acceso al destino                                          |
|---------------|----------------------------------------------------------------|---------------------------------------------------|---------------------------------------------------------|
| Redpark.exe   | Archivo ejecutable del editor de texto. Sin cambios de productos anteriores. | C: \\Redpark.exe del Bloc de notas de ejemplo \\ \\                  | \[Redpark.exe en el \] \\ \_ estacionamiento rojo \\          |
| Readme.txt    | Un archivo de información. Sin cambios de productos anteriores.         | C: \\Readme.txt del Bloc de notas de ejemplo \\ \\                   | \[Readme.txt en el \] \\ \_ estacionamiento rojo \\           |
| Help.txt      | Manual de ayuda. Sin cambios de productos anteriores.                 | C: \\Help.txt del Bloc de notas de ejemplo \\ \\                     | No instalado. Siempre ejecute desde el origen.                  |
| Baseba01.txt  | Programa de juegos de béisbol del año 2001.                          | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Baseba01.txt         | \[\] \\Baseball.txt para \_ deportes de estacionamiento rojo \\ \\ |
| Footba01.txt  | Programa de juegos de fútbol del año 2001.                          | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Footba01.txt         | \[\] \\Football.txt para \_ deportes de estacionamiento rojo \\ \\ |
| Basket01.txt  | Programa de juegos de baloncesto del año 2001.                        | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Basket01.txt         | \[\] \\Basket01.txt para \_ deportes de estacionamiento rojo \\ \\ |
| Dance01.txt   | Rendimiento de baile del año 2001.                              | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Dance01.txt          | \[\] \\ \_Dance.txt artes de estacionamiento rojo \\ \\      |
| Concert01.txt | Rendimiento de música del año 2001.                              | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Concer01.txt         | \[\] \\ \_Concert.txt artes de estacionamiento rojo \\ \\    |
| Opera01.txt   | Rendimiento de opera para el año 2001.                              | C: \\ eventos del Bloc de notas de ejemplo \\ \\ \\Opera01.txt          | \[\] \\ \_Opera01.txt artes de estacionamiento rojo \\ \\    |
| Januar01.txt  | Admisiones en enero del año 2001.                            | C: \\ \\Januar01.txt puerta de Bloc de notas de ejemplo \\ \\           | \[January.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\    |
| NewYea01.txt  | Admisiones en los nuevos años del año 2001.                      | C: \\ ejemplo de \\ festividad de puerta de Bloc de notas \\ \\ \\NewYea01.txt | \[NewYears.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\   |
| Memori01.txt  | Admisiones en el día del recuerdo del año 2001.                       | C: \\ ejemplo de \\ festividad de puerta de Bloc de notas \\ \\ \\Memori01.txt | \[Memori01.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\   |



 

La instalación del paquete de actualización quita todas las características instaladas con el producto original no utilizadas por el producto actualizado.

Por ejemplo, al actualizar desde MNP2000, la instalación de la actualización quita los siguientes archivos del equipo del usuario:

-   Baseball.txt
-   Football.txt
-   Dance.txt
-   Concert.txt
-   January.txt
-   NewYears.txt

La instalación del paquete de actualización escribe los siguientes valores en el registro del usuario en:

**HKEY \_ SOFTWARE de \_ equipo local** ejemplo de Bloc de \\  \\  \\ **notas** de Microsoft



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



 

La actualización actualiza los accesos directos antiguos a los siguientes métodos abreviados. Se puede seleccionar uno de estos métodos abreviados durante la instalación como un acceso directo anunciado para que el usuario pueda instalar la característica de béisbol a petición.



| Nombre        | Ubicación de acceso directo                         | Destino de acceso directo                                           |
|-------------|-------------------------------------------|-----------------------------------------------------------|
| sNotepad    | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Redpark.exe en el \] \\ \_ estacionamiento rojo \\            |
| sReadme     | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Readme.txt en el \] \\ \_ estacionamiento rojo \\             |
| sHelp       | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[ProgramFilesFolder \] \\ ejemplo del \\ bloc de notas \\Help.txt         |
| sBaseball   | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\Baseba01.txt para \_ deportes de estacionamiento rojo \\ \\   |
| sFootball   | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\Footba01.txt para \_ deportes de estacionamiento rojo \\ \\   |
| sBasketball | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\Basketba01.txt para \_ deportes de estacionamiento rojo \\ \\ |
| sDance      | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\ \_Dance01.txt artes de estacionamiento rojo \\ \\      |
| sConcert    | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\ \_Concer01.txt artes de estacionamiento rojo \\ \\     |
| sOpera      | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[\] \\ \_Opera01.txt artes de estacionamiento rojo \\ \\      |
| sJanuary    | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Januar01.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\     |
| sNewYears   | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[NewYea01.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\     |
| sMemorial   | \[\] \\ Menú de color rojo de \_ ProgramFilesFolder \\\\ | \[Memori01.txt de la \] \\ \_ puerta de estacionamiento rojo \\ \\     |



 

Cuando un usuario desinstala el paquete de actualización, Windows Installer quita por completo todas las versiones del producto del equipo del usuario. El usuario no se queda con ninguna parte de MNP2000 o MNP2001.

[Continuar](importing-original-installation-database.md)

 

 



