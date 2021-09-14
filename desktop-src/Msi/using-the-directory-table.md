---
description: La tabla Directory especifica el diseño de una instalación.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Uso de la tabla de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7218fe6f6e2ca36bc0c52e74b564ad07d87053a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074267"
---
# <a name="using-the-directory-table"></a>Uso de la tabla de directorios

La [tabla Directory](directory-table.md) especifica el diseño de una instalación. Cuando los directorios se resuelven durante la acción [CostFinalize](costfinalize-action.md), las claves de la tabla Directory se convierten en propiedades establecidas en rutas de acceso de directorio. [](properties.md) Tenga en cuenta que el instalador establece una serie de propiedades [estándar en](properties.md) las rutas de acceso de carpeta del sistema. Consulte la [Referencia de propiedades](property-reference.md) para obtener una lista de las propiedades que se establecen en carpetas del sistema.

La mejor manera de especificar la ubicación de destino de un directorio es crear la tabla [Directory](directory-table.md) en el paquete de instalación para proporcionar la ubicación correcta, como se describe en esta sección. Si es necesario cambiar la ubicación del directorio en el momento de la instalación, consulte también la sección: Cambio de la ubicación de [destino de un directorio.](changing-the-target-location-for-a-directory.md)

A continuación se muestra un ejemplo de una tabla Directory.



| Directorio     | Elemento primario \_ del directorio | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | Aplicación        |
| DLLDIR        | EXEDIR            | Discretización        |
| DesktopFolder | TARGETDIR         | Escritorio    |



 

Cada fila de la tabla Directory indica un directorio tanto en el origen como en el destino. Por ejemplo, suponga que el paquete de instalación reside en el \\ \\ origen de las \\ \\ aplicaciones. Dado que el campo Directory Parent de la primera fila es Null, este registro indica los directorios raíz para el origen \_ y el destino. Para el origen, el valor de este directorio lo da el campo DefaultDir. La [**propiedad SourceDir**](sourcedir.md) tiene como valor predeterminado la ubicación del paquete de instalación. Por lo tanto, a menos que se invalide la propiedad **SourceDir,** el directorio de origen raíz es \\ \\ el origen de aplicaciones \\ \\ .

El campo Directorio del primer registro indica la ubicación del directorio de destino raíz. En este caso, el valor de la [**propiedad TARGETDIR**](targetdir.md) indica este directorio. Normalmente, el valor de la **propiedad TARGETDIR** se establece en la línea de comandos o a través de una interfaz de usuario. En este caso, suponga que la **propiedad TARGETDIR** está establecida en C: \\ Program Files Target \\ \\ .

Para el segundo registro, el campo Directory \_ Parent (Primario del directorio) no es Null. Por lo tanto, este registro indica un directorio no raíz para el origen y el destino. En el caso de un directorio de origen no raíz, el directorio de origen indicado por el registro descrito en el campo Directory Parent (Primario del \_ directorio) es el directorio primario. Para el segundo registro, el campo Directory \_ Parent es TARGETDIR. Como se ha mostrado anteriormente, el directorio de origen indicado por el registro TARGETDIR se resolvió en el \\ \\ origen de las \\ \\ aplicaciones. Por lo tanto, el directorio de origen indicado por el segundo registro es aplicación \\ \\ de origen de aplicaciones \\ \\ \\ .

Un proceso similar funciona para el directorio de destino. El valor del directorio primario para el directorio de destino descrito en el segundo registro es el directorio de destino resuelto por el campo Primario \_ del directorio. De nuevo, el \_ campo Directory Parent contiene el valor TARGETDIR. Esto indica el primer registro que se resuelve en un directorio de destino de C: \\ Archivos de programa de \\ \\ destino. El campo Directorio contiene una propiedad definida por el autor denominada EXEDIR. Si se establece esta propiedad, su valor proporciona la ruta de acceso completa del directorio. Por lo tanto, si esta propiedad se establece en C: Data Common , el valor del directorio de destino indicado por el segundo registro \\ \\ es \\ C: Data Common \\ \\ \\ . Si no se establece, el directorio de destino toma el nombre especificado por el campo DefaultDir. En este caso, el directorio de destino es C: \\ Program Files Target App \\ \\ \\ .

El mismo proceso funciona para el tercer registro. Si no se establecen EXEDIR y DLLDIR, el directorio de destino es C: Carpeta de aplicaciones de destino de archivos de programa y el directorio de origen es El contenedor de aplicaciones \\ de origen de \\ las \\ \\ \\ \\ \\ \\ \\ \\ aplicaciones.

El cuarto registro usa la [**propiedad DesktopFolder.**](desktopfolder.md) Si la ubicación del escritorio del usuario es C: Winnt Profiles User Desktop , el directorio de destino se resuelve en \\ \\ \\ \\ \\ C: \\ Winnt \\ Profiles \\ User Desktop \\ \\ . El directorio de origen se resuelve en el \\ \\ escritorio de origen de \\ las \\ \\ aplicaciones.

Hay dos características de sintaxis adicionales que se pueden usar en la columna DefaultDir de la tabla Directory. Para un directorio de origen no raíz, un punto (.) especificado en la columna DefaultDir indica que el directorio debe estar ubicado en su directorio primario sin un subdirectorio. Para especificar distintas rutas de acceso de directorio de origen y destino, separe las rutas de acceso de destino y de origen de la columna DefaultDir con dos puntos como se muestra a continuación: \[ targetpath \] : \[ sourcepath \] . Estas características se pueden usar juntas para agregar niveles a las rutas de acceso de origen o de destino para un único directorio. Vea el ejemplo siguiente de una tabla de directorios.



| Directorio   | Elemento primario \_ del directorio | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | Myapp      |
| BinDir      | MyAppDir          | Discretización        |
| Binx86Dir   | BinDir            | .:x86      |
| BinAlphaDir | BinDir            | .:Alpha    |



 

Las rutas de acceso de origen y destino se resuelven para las filas MyAppDir, BinDir, Binx86Dir y BinAlphaDir como se muestra a continuación.



| Registro       | Rutas de acceso de destino            | Rutas de acceso de origen                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BinDir:      | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ Alpha |



 

> [!Note]  
> El instalador de Windows no admite la plataforma Alfa.

 

 

 



