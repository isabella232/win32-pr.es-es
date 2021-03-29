---
description: La tabla de directorios especifica el diseño de una instalación de.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Usar la tabla de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7218fe6f6e2ca36bc0c52e74b564ad07d87053a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277154"
---
# <a name="using-the-directory-table"></a>Usar la tabla de directorio

La [tabla de directorios](directory-table.md) especifica el diseño de una instalación de. Cuando los directorios se resuelven durante la [acción CostFinalize](costfinalize-action.md), las claves de la tabla de directorio se convierten en [propiedades](properties.md) establecidas en rutas de acceso de directorio. Tenga en cuenta que el instalador establece varias propiedades estándar en las rutas de acceso a [las](properties.md) carpetas del sistema. Vea la [referencia](property-reference.md) de propiedades para obtener una lista de las propiedades que se establecen en carpetas del sistema.

La mejor manera de especificar la ubicación de destino para un directorio es crear la [tabla de directorio](directory-table.md) en el paquete de instalación para proporcionar la ubicación correcta, como se describe en esta sección. Si es necesario cambiar la ubicación del directorio en el momento de la instalación, vea también la sección: [cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md) .

El siguiente es un ejemplo de una tabla de directorio.



| Directorio     | Directorio \_ primario | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | Aplicación        |
| DLLDIR        | EXEDIR            | Discretización        |
| DesktopFolder | TARGETDIR         | Escritorio    |



 

Cada fila de la tabla del directorio indica un directorio tanto en el origen como en el destino. Por ejemplo, suponga que el paquete de instalación reside en el \\ \\ origen de las aplicaciones \\ \\ . Dado que el \_ campo principal de directorio de la primera fila es null, este registro indica los directorios raíz para el origen y el destino. En el origen, el campo DefaultDir proporciona el valor de este directorio. La propiedad [**SourceDir**](sourcedir.md) tiene como valor predeterminado la ubicación del paquete de instalación. Por lo tanto, a menos que se invalide la propiedad **SourceDir** , el directorio de origen raíz es el \\ \\ origen de las aplicaciones \\ \\ .

El campo directorio del primer registro indica la ubicación del directorio de destino raíz. En este caso, el valor de la propiedad [**targetDir**](targetdir.md) indica este directorio. Normalmente, el valor de la propiedad **targetDir** se establece en la línea de comandos o a través de una interfaz de usuario. En este caso, supongamos que la propiedad **targetDir** está establecida en C: \\ archivos de programa de \\ destino \\ .

En el segundo registro, el \_ campo principal del directorio no es NULL. Por lo tanto, este registro indica un directorio no raíz para el origen y el destino. Para un directorio de origen no raíz, el directorio de origen indicado por el registro descrito en el \_ campo principal de directorio es el directorio principal. En el segundo registro, el \_ campo principal del directorio es targetdir. Como se mostró anteriormente, el directorio de origen indicado por el registro de TARGETDIR se resolvió en el \\ \\ origen de aplicaciones \\ \\ . Por lo tanto, el directorio de origen indicado por el segundo registro es \\ \\ aplicación de origen de aplicaciones \\ \\ \\ .

Un proceso similar funciona para el directorio de destino. El valor del directorio principal para el directorio de destino descrito en el segundo registro es el directorio de destino que el campo principal de directorio resuelve \_ . De nuevo, el \_ campo principal de directorio contiene el valor targetdir. Esto indica el primer registro que se resuelve en un directorio de destino de C: \\ archivos de programa de \\ destino \\ . El campo directorio contiene una propiedad definida por el autor denominada EXEDIR. Si se establece esta propiedad, su valor proporciona la ruta de acceso completa del directorio. Por lo tanto, si esta propiedad se establece en C: \\ Data \\ Common \\ , el valor del directorio de destino indicado por el segundo registro es C: \\ Data \\ Common \\ . Si no se establece, el directorio de destino toma el nombre dado por el campo DefaultDir. En este caso, el directorio de destino es C: archivos de programa de la \\ \\ aplicación de destino \\ \\ .

El mismo proceso funciona para el tercer registro. Si EXEDIR y DLLDIR no están establecidos, el directorio de destino es C: \\ archivos de programa de \\ destino \\ App \\ bin y el directorio de origen es \\ \\ aplicaciones \\ origen \\ App \\ bin \\ .

El cuarto registro usa la propiedad [**DesktopFolder**](desktopfolder.md) . Si la ubicación del escritorio del usuario es c: \\ WinNT \\ profiles \\ User \\ Desktop \\ , el directorio de destino se resuelve como c: \\ WinNT \\ perfiles \\ usuario \\ escritorio \\ . El directorio de origen se resuelve en \\ \\ aplicaciones \\ escritorio de origen \\ \\ .

Hay dos características de sintaxis adicionales que se pueden usar en la columna DefaultDir de la tabla de directorio. Para un directorio de origen no raíz, un punto (.) especificado en la columna DefaultDir indica que el directorio debe estar ubicado en el directorio primario sin un subdirectorio. Para especificar rutas de acceso de directorio de origen y de destino diferentes, separe las rutas de acceso de origen y de destino en la columna DefaultDir con un signo de dos puntos de la manera siguiente: \[ TargetPath \] : \[ SourcePath \] . Estas características se pueden usar conjuntamente para agregar niveles a las rutas de acceso de origen o de destino para un único directorio. Vea el ejemplo siguiente de una tabla de directorio.



| Directorio   | Directorio \_ primario | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | MyApp      |
| BinDir      | MyAppDir          | Discretización        |
| Binx86Dir   | BinDir            | .: x86      |
| BinAlphaDir | BinDir            | .: Alpha    |



 

Las rutas de acceso de origen y de destino se resuelven para las filas MyAppDir, BinDir, Binx86Dir y BinAlphaDir como se indica a continuación.



| Registro       | Rutas de acceso de destino            | Rutas de acceso de origen                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BinDir:      | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ bin | \[SourceDir \] MyApp \\ bin \\ Alpha |



 

> [!Note]  
> La plataforma Alpha no es compatible con el Windows Installer.

 

 

 



