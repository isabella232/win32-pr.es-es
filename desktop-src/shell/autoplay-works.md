---
description: La creación de una aplicación habilitada para AutoRun es un procedimiento sencillo. En este tema se usa un CD-ROM como ejemplo (era el primer medio para implementar esta tecnología), pero hoy en día hay muchos tipos de medios diferentes que pueden utilizarlo.
title: Creación de una aplicación AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153921"
---
# <a name="creating-an-autorun-enabled-application"></a>Creación de una aplicación AutoRun-Enabled

La creación de una aplicación habilitada para AutoRun es un procedimiento sencillo. En este tema se usa un CD-ROM como ejemplo (era el primer medio para implementar esta tecnología), pero hoy en día hay muchos tipos de medios diferentes que pueden utilizarlo.

Para habilitar la ejecución automática en la aplicación, solo tiene que incluir dos archivos esenciales:

-   Un archivo Autorun. inf
-   Una aplicación de inicio

Cuando un usuario inserta un disco en una unidad de CD-ROM en un equipo compatible con AutoRun, el sistema comprueba inmediatamente si el disco tiene un sistema de archivos de equipo personal. Si es así, el sistema busca un archivo denominado [Autorun. inf](#creating-an-autoruninf-file). Este archivo especifica una aplicación de instalación que se ejecutará, junto con una variedad de opciones de configuración opcionales. Normalmente, la aplicación de inicio instala, desinstala, configura y quizás ejecuta la aplicación.

-   [Crear un archivo Autorun. inf](#creating-an-autoruninf-file)
-   [La \[ \] sección DeviceInstall](#the-deviceinstall-section)
-   [Temas relacionados](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Crear un archivo Autorun. inf

Autorun. inf es un archivo de texto que se encuentra en el directorio raíz del CD-ROM que contiene la aplicación. Su función principal es proporcionar al sistema el nombre y la ubicación del programa de inicio de la aplicación que se ejecutará cuando se inserte el disco.

> [!Note]  
> Los archivos Autorun. inf no se admiten en Windows XP para las unidades que devuelven la unidad \_ extraíble desde [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

El archivo Autorun. inf también puede contener información opcional, como:

-   El nombre de un archivo que contiene un icono que representará la unidad de CD-ROM de la aplicación. Este icono se mostrará en el explorador de Windows en lugar del icono de la unidad estándar.
-   Comandos adicionales para el menú contextual que se muestra cuando el usuario hace clic con el botón secundario en el icono de CD-ROM. También puede especificar el comando predeterminado que se ejecuta cuando el usuario hace doble clic en el icono.

Los archivos Autorun. inf son similares a los archivos. ini. Están formados por una o varias secciones, cada una con un nombre entre corchetes. Cada sección contiene una serie de comandos que se ejecutarán en el shell cuando se inserte el disco. Hay dos secciones que están definidas actualmente para los archivos Autorun. inf.

-   La sección **\[ ejecución automática \]** contiene los comandos de ejecución automática predeterminados. Todos los archivos Autorun. inf deben tener una sección de **\[ ejecución automática \]** .
-   Se puede incluir una sección opcional **\[ Autorun. alpha \]** para los sistemas que se ejecutan en equipos basados en RISC. Cuando se inserta un disco en una unidad de CD-ROM en un sistema basado en RISC, el shell ejecutará los comandos de esta sección en lugar de los de la sección **\[ ejecución automática \]** .

> [!Note]  
> El shell comprueba primero una sección específica de la arquitectura. Si no encuentra uno, usa la información de la sección **\[ ejecución automática \]** . Una vez que el shell encuentra una sección, omite todas las demás, por lo que cada sección debe ser independiente.

 

Cada sección contiene una serie de comandos que determinan cómo tiene lugar la operación de ejecución automática. Hay cinco comandos disponibles.



| Get-Help                         | Descripción                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [DefaultIcon](autorun-cmds.md) | Especifica el icono predeterminado para la aplicación.                                        |
| [icono](autorun-cmds.md)        | Especifica la ruta de acceso y el nombre de un icono específico de la aplicación para la unidad de CD-ROM. |
| [open](autorun-cmds.md)        | Especifica la ruta de acceso y el nombre de archivo de la aplicación de inicio.                           |
| [useautorun](autorun-cmds.md)  | Especifica que se deben usar las características de reproducción de reproducción V2 si se admiten.                       |
| [interfaz](autorun-cmds.md)       | Define el comando predeterminado en el menú contextual del CD-ROM.                             |
| [verbo de Shell \_](autorun-cmds.md) | Agrega comandos al menú contextual del CD-ROM.                                           |



 

El siguiente es un ejemplo de un archivo Autorun. inf simple. Especifica Filename.exe como aplicación de inicio. El segundo icono de Filename.exe representará la unidad de CD-ROM en lugar del icono de la unidad estándar.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Este ejemplo Autorun. inf ejecuta diferentes aplicaciones de inicio en función del tipo de equipo.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>La \[ \] sección DeviceInstall

Puede usar la sección **\[ DeviceInstall \]** en cualquier medio extraíble. Solo se admite en Windows XP. Use **DriverPath** para especificar una ruta de acceso de directorio en la que Windows XP busca archivos de controlador, lo que evita una búsqueda larga en todo el contenido.

Use la sección **\[ DeviceInstall \]** con una instalación de controlador para especificar los directorios en los que Windows XP debe buscar los archivos de controlador. En Windows XP, ya no se busca en todo el medio de forma predeterminada, por lo que se requiere **\[ DeviceInstall \]** para especificar ubicaciones de búsqueda. A continuación se muestran los únicos medios extraíbles que Windows XP realiza búsquedas por completo sin una sección **\[ DeviceInstall \]** en un archivo Autorun. inf.

-   Disquetes encontrados en las unidades A o B.
-   Los medios de CD/DVD tienen menos de 1 Gigabyte (GB) de tamaño.

Todos los demás medios deben incluir una sección **\[ DeviceInstall \]** para que Windows XP detecte los controladores almacenados en ese medio.

> [!Note]  
> Al igual que con la sección de **\[ ejecución automática \]** , la sección **\[ DeviceInstall \]** puede ser específica de la arquitectura.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar aplicaciones de inicio de ejecución automática](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Escritura de una aplicación de instalación de dispositivos](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
